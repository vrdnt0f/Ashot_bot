# 🥩 Ашот — Telegram-бот шашлычника

Чат-бот с персонажем Ашота — колоритного владельца кавказской шашлычной. Построен на базе локальной LLM через [LM Studio](https://lmstudio.ai/) и фреймворке [aiogram 3](https://docs.aiogram.dev/).

## Возможности

- Диалог с запоминанием истории (последние 20 сообщений)
- Команда `/start` — начать общение
- Команда `/reset` — сбросить историю диалога
- Обработка ошибок подключения к LM Studio

## Требования

- Python 3.10+
- [LM Studio](https://lmstudio.ai/) с запущенным Local Server
- Telegram-бот (токен от [@BotFather](https://t.me/BotFather))

## Установка

```bash
# 1. Клонировать репозиторий
git clone https://github.com/your-username/ashot-bot.git
cd ashot-bot

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

## Настройка LM Studio

1. Открыть LM Studio → вкладка **Developer** → **Local Server**
2. Выбрать модель из выпадающего списка
3. Нажать переключатель **Status: Stopped** → сервер запустится на `http://localhost:1234`
4. Скопировать **API Model Identifier** из правой панели в `.env` → `MODEL_NAME`

## Выбор модели

| Модель | VRAM | Качество русского | Рекомендация |
|--------|------|-------------------|--------------|
| `qwen2.5:7b-instruct` | ~4 GB | ⭐⭐⭐⭐ | ✅ Оптимально |
| `gemma3:4b` | ~3 GB | ⭐⭐⭐⭐ | Быстрая альтернатива |
| `llama3.1:8b` | ~5 GB | ⭐⭐⭐ | Если есть запас памяти |

## Структура проекта

```
ashot-bot/
├── Ashot.py         # Основной файл бота
├── requirements.txt # Зависимости
├── .env.example     # Шаблон переменных окружения
├── .env             # Локальные настройки (не в git!)
├── .gitignore
└── README.md
```
