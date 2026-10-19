# PulseFit 💪

A full-stack fitness web application for planning and tracking workouts. Users can create an account, build workout plans from an exercise library and schedule their training sessions in a calendar.

## Features

- **User accounts** – registration and login with hashed passwords (bcrypt) and JWT-based authentication stored in HTTP-only cookies
- **Workout plans** – create and manage personal training plans
- **Exercise library** – exercises that can be added to workout plans
- **Training calendar** – schedule workouts in an interactive calendar view (FullCalendar)
- **REST API** – Express backend with MongoDB for persistent storage

## Tech Stack

| Layer    | Technologies |
|----------|--------------|
| Frontend | React 19, TypeScript, Vite, Tailwind CSS, React Router, FullCalendar, Axios, React Auth Kit, Day.js |
| Backend  | Node.js, Express 5, MongoDB, Mongoose, JSON Web Tokens, bcrypt, cookie-parser, CORS |

## Project Structure

```
PulseFit/
├── frontend/          React + TypeScript client (Vite)
└── backend/
    ├── app.js         Express server and route setup
    ├── controllers/   Request handlers (users, workout plans, exercises, calendar)
    ├── models/        Mongoose schemas (User, WorkoutPlan, Exercise, Calendar)
    ├── routes/        API route definitions
    └── middleware/    Auth and error handling
```

## API Overview

| Route            | Description                          |
|------------------|--------------------------------------|
| `/api/users`     | Register, login, logout, current user |
| `/api/workoutP`  | Workout plans                         |
| `/api/exercise`  | Exercises                             |
| `/api/calendar`  | Calendar entries                      |

## Getting Started

### Prerequisites

- Node.js 18+
- A MongoDB database (local or MongoDB Atlas)

### Backend

```bash
cd backend
npm install
```

Create a `.env` file in the `backend` folder:

```env
DATABASE=<your MongoDB connection string>
PORT=5000
JWT_SECRET=<a long random secret>
JWT_EXPIRE=<token lifetime>
```

Start the server:

```bash
npm run dev      # development with nodemon
# or
npm start
```

The API runs on `http://localhost:5000`.

### Frontend

```bash
cd frontend
npm install
npm run dev
```

The app runs on `http://localhost:5173`.

## Team

This project was developed as a team project by:

- [@SacidSen](https://github.com/SacidSen)
- [@Maximkingim9](https://github.com/Maximkingim9) – [describe your contribution here]
