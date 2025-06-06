# 🔐 Authentication App (MERN Stack)

A full-stack authentication system built using **Node.js**, **Express**, **MongoDB**, and **React**. This app provides user registration, login, and protected route handling with JWT-based authentication.

---

## 🚀 Features

- User registration & login
- Password hashing (bcrypt)
- JWT token-based authentication
- Protected backend routes
- Persistent login via localStorage
- Basic React form handling

---

## 🧱 Tech Stack

**Frontend**: React, Axios, React Router  
**Backend**: Node.js, Express, MongoDB, Mongoose, JWT

---

## 📁 Project Structure

auth-app/
├── server/
│ ├── controllers/
│ ├── middleware/
│ ├── models/
│ ├── routes/
│ ├── .env
│ └── index.js
├── client/
│ └── src/
│ ├── pages/
│ ├── App.js
│ └── index.js
└── README.md

yaml
Copy
Edit

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/kiokomutunga/Authentication.git
cd Authentication
2. Backend Setup
bash
Copy
Edit
cd server
npm install
Create .env file in /server:
ini
Copy
Edit
MONGO_URI=mongodb://localhost:27017/authdb
JWT_SECRET=your_jwt_secret_key
Run the backend server:
bash
Copy
Edit
npm start
# Runs on http://localhost:5000
3. Frontend Setup
bash
Copy
Edit
cd ../client
npm install
npm start
# Runs on http://localhost:3000
🔐 API Endpoints
POST /api/auth/register
Registers a new user.

Request Body:
json
Copy
Edit
{
  "username": "John",
  "email": "john@example.com",
  "password": "yourPassword"
}
POST /api/auth/login
Logs in a user and returns a JWT token.

Request Body:
json
Copy
Edit
{
  "email": "john@example.com",
  "password": "yourPassword"
}
🔒 Protected Routes
To protect a route on the backend, use the JWT middleware. Example:

js
Copy
Edit
const jwt = require('jsonwebtoken');
const authMiddleware = (req, res, next) => {
  // logic to verify token
};
✅ Future Improvements
Form validation (client + server)

Password reset feature

OAuth integration (Google, GitHub)

Refresh tokens

🧑‍💻 Author
Kioko Mutunga
GitHub Profile

