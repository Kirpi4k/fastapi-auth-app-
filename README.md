📝 FastAPI Регистрация и Вход

Простое веб-приложение на FastAPI с формами регистрации и входа, сохранением данных в SQLite и подключением CSS.

🚀 Возможности

Регистрация пользователя с email и паролем

Хранение паролей в зашифрованном виде (bcrypt)

Стилизация через CSS

📂 Структура проекта
project/
│── backend/
│     ├── main.py          # Основное приложение FastAPI
│     ├── database.py      # Подключение к базе данных (SQLite)
│     └── users.db         # База данных (создаётся автоматически)
│
│── static/
│     ├── style.css        # Стили
│     └── image/           # Папка для картинок (опционально)
│
│── templates/
│     ├── index.html       # Главная страница
│     ├── login.html       # Страница входа
│     └── register.html    # Страница регистрации
│
│── README.md              # Документация проекта

🔧 Установка и запуск

Склонируй проект или скачай архив:

git clone https://github.com/your-repo/fastapi-auth-app.git
cd fastapi-auth-app


Установи зависимости:

pip install fastapi uvicorn sqlalchemy passlib[bcrypt] aiosqlite


Запусти сервер:

uvicorn backend.main:app --reload


Открой в браузере:

http://127.0.0.1:8000/register
 → Регистрация

http://127.0.0.1:8000/login
 → Вход

http://127.0.0.1:8000/
 → Главная страница (для вошедших)

⚙️ Технологии

FastAPI
 — фреймворк для backend

Uvicorn
 — ASGI-сервер

SQLite
 — база данных

SQLAlchemy
 — ORM

Passlib (bcrypt)
 — хеширование паролей

🔒 Безопасность

Пароли хранятся в базе в хешированном виде (bcrypt).
