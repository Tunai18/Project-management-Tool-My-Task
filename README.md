# Project Management Tool

A full-stack internship project built with React, Vite, Node.js, Express, MongoDB, and JWT authentication.

## Features
- Register and log in with JWT authentication
- Dashboard with project/task counts and completion rate
- Create, edit, and delete projects
- Create, edit, and delete tasks
- Task priorities, statuses, and deadlines
- Search and filter tasks
- Responsive dashboard UI
- MongoDB persistence

## Requirements
- Node.js 18+
- MongoDB local instance or MongoDB Atlas connection string

## 1. Configure the backend
```bash
cd server
copy .env.example .env
```
Edit `server/.env` and set `MONGO_URI` and `JWT_SECRET`.

## 2. Install and run the backend
```bash
cd server
npm install
npm run dev
```
Backend runs on `http://localhost:5000`.

## 3. Install and run the frontend
Open another terminal:
```bash
cd client
npm install
npm run dev
```
Frontend runs on `http://localhost:5173`.

## Demo mode
The UI can be explored using the built-in demo data without a backend. To use real authentication and persistence, start the backend and use the app's register/login screens. The frontend expects the API at `http://localhost:5000/api`.

## API routes
- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/auth/me`
- `GET/POST /api/projects`
- `GET/PUT/DELETE /api/projects/:id`
- `GET/POST /api/tasks`
- `PUT/DELETE /api/tasks/:id`

## Deployment
- Frontend: Vercel or Netlify
- Backend: Render
- Database: MongoDB Atlas
- Set `VITE_API_URL` in the frontend hosting environment to your deployed API URL plus `/api`.
- Set `MONGO_URI`, `JWT_SECRET`, and `CLIENT_URL` on the backend hosting service.

This is a starter project. Before production use, add rate limiting, email verification, password reset, and more extensive tests.
