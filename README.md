# Task Manager Fullstack App

Simple Task Manager application built with **Node.js + Express + Prisma + React + TypeScript**.

Users can:

* Register account
* Login using JWT authentication
* Create tasks
* Update tasks
* Delete tasks
* Mark tasks as completed

---

# Tech Stack

### Backend

* Node.js
* Express.js
* TypeScript
* Prisma ORM
* SQLite
* JWT Authentication
* Bcrypt

### Frontend

* React
* TypeScript
* Vite
* TailwindCSS
* Axios
* React Router

---

# Installation

## 1. Clone repository

```
git clone https://github.com/username/task-manager-fullstack.git
cd task-manager-fullstack
```

---

# Backend Setup

```
cd task-manager-api-backend
npm install
```

### Setup environment variables

Create `.env`

```
DATABASE_URL="file:./dev.db"
JWT_SECRET="supersecretkey"
PORT=5000
```

### Run migrations

```
npx prisma migrate dev
```

### Run backend

```
npm run dev
```

Server runs at

```
http://localhost:5000
```

---

# Frontend Setup

```
cd task-manager-api-frontend
npm install
```

Create `.env`

```
VITE_API_URL=http://localhost:5000
```

Run frontend

```
npm run dev
```

App runs at

```
http://localhost:5173
```

---

# Database Setup

This project uses **Prisma with SQLite**

Run migration:

```
npx prisma migrate dev
```

To view database:

```
npx prisma studio
```

---

# API Endpoints

## Register

POST

```
/users
```

Body

```
{
 "name": "John Doe",
 "email": "john@gmail.com",
 "password": "123456"
}
```

---

## Login

POST

```
/users/login
```

Body

```
{
 "email": "john@gmail.com",
 "password": "123456"
}
```

Response

```
{
 "message": "Login success",
 "token": "JWT_TOKEN",
 "user": {
   "id": 1,
   "name": "John Doe"
 }
}
```

---

## Get My Tasks

GET

```
/tasks/my-tasks
```

Header

```
Authorization: Bearer TOKEN
```

---

## Create Task

POST

```
/tasks
```

Body

```
{
 "title": "Learn English"
}
```

---

## Update Task

PUT

```
/tasks/:id
```

Body

```
{
 "title": "Learn English",
 "completed": true
}
```

---

## Delete Task

DELETE

```
/tasks/:id
```

---

# Environment Variables

Example `.env.example`

```
DATABASE_URL="file:./dev.db"
JWT_SECRET="your_secret_key"
PORT=5000
```

---

# Live Demo

Frontend (Vercel)

```
https://your-app.vercel.app
```

Backend

```
https://your-api.onrender.com
```
