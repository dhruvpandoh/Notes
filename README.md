# Notes App (MERN + JWT Auth)

A full-stack notes application where users can sign up, log in, and manage personal notes.  
Notes are private per user and stored in MongoDB, secured via JWT middleware.

## Features
### Auth
- User signup/login
- Password hashing using bcrypt
- JWT-based protected routes

### Notes
- Create, read, update, delete notes
- User-scoped notes (each user sees only their own)
- React Context state management

## Tech Stack
- React (CRA)
- React Context API
- Node.js + Express
- MongoDB + Mongoose
- JWT Authentication
- bcryptjs, express-validator

## Folder Structure
```
Notes-main/
  backend/     # Express + Mongo + Auth + Notes APIs
  notes/       # React frontend
```

## Setup Instructions

### 1. Backend
```bash
cd Notes-main/backend
npm install
```

Create `.env` (recommended):
```env
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret
PORT=5000
```

Run backend:
```bash
nodemon index.js
```
Runs on `http://localhost:5000`

### 2. Frontend
```bash
cd ../notes
npm install
npm start
```
Runs on `http://localhost:3000`

## Backend Routes

### Auth
- `POST /api/auth/createuser`
- `POST /api/auth/login`
- `POST /api/auth/getuser` (protected)

### Notes (protected)
- `GET /api/notes/fetchallnotes`
- `POST /api/notes/addnote`
- `PUT /api/notes/updatenote/:id`
- `DELETE /api/notes/deletenote/:id`

## Future Improvements
- Better form validation UI.
- Add tags, pinning, and reminders.
- Deploy with a hosted MongoDB + production JWT secrets.
