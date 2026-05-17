# Task Management API

A robust RESTful API for task management built with Node.js, Express, and MongoDB. This project includes user authentication (JWT) and full CRUD capabilities for tasks.

## 🚀 Live Demo
- **Live API URL:** `https://udrlight-task-management-api.onrender.com/`

## ✨ Features
- **User Authentication:** Secure signup and login using `bcrypt` for password hashing and `jsonwebtoken` for session management.
- **Task Management:** Create, read, update, and delete tasks. Users can only access and modify their own tasks.
- **Validation:** Input validation and sanitization using `express-validator`.
- **Security:** Protected routes using custom authentication middleware.
- **CORS Enabled:** Ready to be consumed by any frontend application.

## 🛠️ Tech Stack
- **Runtime:** Node.js
- **Framework:** Express.js
- **Database:** MongoDB Atlas (Mongoose ORM)

## 🚦 Endpoints
### Auth
- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/login` - Authenticate and get JWT token

### Tasks (Protected - Requires Bearer Token)
- `GET /api/tasks` - Get all tasks for the logged-in user
- `POST /api/tasks` - Create a new task
- `PUT /api/tasks/:id` - Update a task
- `DELETE /api/tasks/:id` - Delete a task

## 🧪 How to Test
1. **Postman Collection:** A `Task_Manager_API.postman_collection.json` file is included in the repository.
2. Import this file directly into Postman.
3. Update the `baseUrl` collection variable to the Live API URL (or `http://localhost:5000/api` for local testing).
4. The collection automatically handles JWT token injection after you run the Login request!

## 💻 Local Setup
1. Clone the repository: `git clone <repo-url>`
2. Install dependencies: `npm install`
3. Create a `.env` file in the root directory with the following variables:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   ```
4. Start the development server: `npm run dev`
