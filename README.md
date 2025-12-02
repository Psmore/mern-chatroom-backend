# MERN Chat App Backend

A real-time chat application backend built using the **MERN stack** (MongoDB, Express, React, Node.js). This project powers user authentication and secure messaging functionality for a chatroom-style application.

---

## 🚀 Features

* User authentication (Register / Login)
* JWT-based authorization
* Protected routes
* CRUD operations for chat goals/messages
* MongoDB persistence with Mongoose
* Centralized error handling
* Async middleware utility

---

## 📁 Project Structure

```
mern_chatApp/
│
├── src/
│   ├── config/
│   │   └── db.js
│   ├── controllers/
│   │   ├── goalController.js
│   │   └── userController.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── errorMiddleware.js
│   ├── models/
│   │   ├── goalModel.js
│   │   └── userModel.js
│   ├── routes/
│   │   ├── goalRoutes.js
│   │   └── userRoutes.js
│   ├── utils/
│   │   └── asyncHandler.js
│   └── server.js
│
└── package.json
```

---

## 🛠 Installation & Setup

### **1. Clone the repository**

```bash
git clone <your-repo-url>
cd mern_chatApp
```

### **2. Install dependencies**

```bash
npm install
```

### **3. Configure environment variables**

Create a `.env` file in the root directory and add:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000
```

### **4. Start the backend server**

```bash
npm start
# or
npm run server   # with nodemon
```

Server will start on:

```
http://localhost:5000
```

---

## 🌐 API Routes

### **Goals Routes** (`/api/goals`)

| Method | Endpoint | Description             |
| ------ | -------- | ----------------------- |
| GET    | `/`      | Get user goals/messages |
| POST   | `/`      | Create a new message    |
| PUT    | `/:id`   | Update a message        |
| DELETE | `/:id`   | Delete a message        |

### **User Routes** (`/api/users`)

| Method | Endpoint | Description      |
| ------ | -------- | ---------------- |
| POST   | `/`      | Register user    |
| POST   | `/login` | Login user       |
| GET    | `/me`    | Get profile data |

---

## 🔐 Authentication

All protected endpoints require an `Authorization` header in this format:

```
Bearer <your_jwt_token>
```

---

## 📦 Dependencies

| Package               | Purpose               |
| --------------------- | --------------------- |
| express               | Web server            |
| mongoose              | MongoDB ORM           |
| bcryptjs              | Password hashing      |
| jsonwebtoken          | JWT authentication    |
| dotenv                | Environment variables |
| express-async-handler | Async wrapper         |
| nodemon               | Dev hot reload        |

---

## 🧪 Testing with Postman / Thunder Client

1. Register a new user at `POST /api/users`
2. Copy returned token
3. Add Authorization header to chat message requests

---

## 📄 License

MIT License

---

## 🤝 Contributing

Contributions welcome! Open issues or PRs to improve functionality.

---

## ⭐ Support

If you found this project useful, consider giving it a star!
