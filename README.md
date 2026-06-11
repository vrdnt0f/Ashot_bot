#Ашот — Telegram-бот шашлычника

Чат-бот с персонажем Ашота — колоритного владельца кавказской шашлычной «У Ашота». Построен на базе локальной LLM через [LM Studio](https://lmstudio.ai/) и фреймворке [aiogram 3](https://docs.aiogram.dev/).

## Возможности

- Диалог с запоминанием истории (последние 20 сообщений)
- Команда `/start` — начать общение с Ашотом
- Команда `/help` — список всех команд
- Команда `/reset` — сбросить историю диалога
- Команда `/menu` — меню шашлычной с ценами
- Команда `/recipe` — рецепт шашлыка от Ашота
- Команда `/wisdom` — мудрость дня от Ашота
- Команда `/joke` — кавказский анекдот
- Команда `/roast` — Ашот тебя подкалывает
- Обработка ошибок подключения к LM Studio

## Требования

- Python 3.10+
- [LM Studio](https://lmstudio.ai/) с запущенным Local Server
- Telegram-бот (токен от [@BotFather](https://t.me/BotFather))

## Установка

```bash
# 1. Клонировать репозиторий
git clone https://github.com/vrdnt0f/Ashot_bot.git
cd Ashot_bot

# 2. Создать виртуальное окружение
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows

# 3. Установить зависимости
pip install -r requirements.txt

# 4. Настроить переменные окружения
cp .env.example .env
# Открыть .env и вставить токен бота и название модели

# 5. Запустить LM Studio → Local Server → выбрать модель → Start Server

# 6. Запустить бота
python Ashot.py
```

## Структура проекта

```
Ashot_bot/
├── Ashot.py         # Основной файл бота
├── requirements.txt # Зависимости
├── .env             # Локальные настройки (не в git!)
├── .gitignore
└── README.md
```
