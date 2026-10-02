# my-react-mysql-app
# My React + MySQL App

## Концепция
Веб-приложение на React, которое взаимодействует с REST API на Node.js/Express, а данные хранятся в MySQL. MySQL Workbench используется для проектирования схемы и администрирования БД.

## Технологический стек
- **Фронтенд**: React 18, Vite, React Router, Axios
- **Бэкенд**: Node.js 20, Express 4
- **СУБД**: MySQL 8
- **Инструмент для БД**: MySQL Workbench
- **Развёртывание**: Docker, Docker Compose (опционально)

## Структура папок
my-react-mysql-app/
├── client/ # React-приложение
│ ├── public/
│ ├── src/
│ │ ├── components/
│ │ ├── pages/
│ │ ├── api/
│ │ └── App.jsx
│ ├── package.json
│ └── .env.example
├── server/ # Node.js/Express API
│ ├── src/
│ │ ├── routes/
│ │ ├── controllers/
│ │ ├── models/
│ │ └── app.js
│ ├── package.json
│ └── .env.example
├── database/ # SQL-скрипты для MySQL
│ ├── schema.sql # CREATE TABLE ...
│ ├── seed.sql # INSERT ...
│ └── er_diagram.png # ER-диаграмма из MySQL Workbench
├── .gitignore
├── .env.example
└── README.md


## Инструкция по развёртыванию
1. Клонировать репозиторий: `git clone <URL>`
2. Установить зависимости:
   - `cd client && npm install`
   - `cd ../server && npm install`
3. Создать базу данных в MySQL Workbench и выполнить `database/schema.sql`, затем `database/seed.sql`.
4. Создать `.env` в `server/` на основе `server/.env.example`.
5. Запустить сервер: `cd server && npm run dev`
6. Запустить клиент: `cd client && npm run dev`
7. Открыть `http://localhost:5173`
