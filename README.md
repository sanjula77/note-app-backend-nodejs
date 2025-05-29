# 📝 Note App Backend (Node.js + Express + MongoDB)

A clean modular RESTful API for a simple note-taking mobile application. Built with **Node.js**, **Express**, and **MongoDB**, this backend is designed following industry best practices, ready to be integrated with an Android frontend using **Jetpack Compose**.

---

## 📦 Tech Stack

- **Node.js** — JavaScript runtime
- **Express.js** — Web framework for Node
- **MongoDB** — NoSQL database
- **Mongoose** — MongoDB ODM
- **dotenv** — Environment variable management
- **express-validator** — Request validation
- **helmet** — Secures HTTP headers
- **cors** — Cross-origin support
- **morgan** — Request logging
- **nodemon** — Dev auto-reloader
- **eslint + prettier** — Code linting & formatting

---

## 📁 Project Structure

```
note-app-backend/
├── config/              # Database connection
│   └── db.js
├── controllers/         # Route logic
│   └── noteController.js
├── middleware/          # Error handling, etc.
│   └── errorHandler.js
├── models/              # Mongoose schemas
│   └── Note.js
├── routes/              # Express routes
│   └── noteRoutes.js
├── .env                 # Environment variables (not committed)
├── .gitignore
├── package.json
├── server.js            # App entry point
└── README.md
```

---

## 🔧 Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/sanjula77/note-app-backend-nodejs.git
cd note-app-backend-nodejs
```

### 2. Install dependencies
```bash
npm install
```

### 3. Setup environment variables

Create a `.env` file in the root:

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/noteapp
```

> Make sure MongoDB is running locally or update the URI for a remote DB.

---

## 🚀 Running the Server

### Development mode
```bash
npm run dev
```

### Production mode
```bash
npm start
```

Once running, your backend will be available at:
```
http://localhost:5000/api/notes
```

---

## 📡 API Endpoints

| Method | Endpoint            | Description           |
|--------|---------------------|-----------------------|
| GET    | `/api/notes`        | Fetch all notes       |
| GET    | `/api/notes/:id`    | Fetch note by ID      |
| POST   | `/api/notes`        | Create a new note     |
| PUT    | `/api/notes/:id`    | Update a note         |
| DELETE | `/api/notes/:id`    | Delete a note         |

### 📌 Sample Note Schema
```json
{
  "title": "Meeting Notes",
  "content": "Discuss project deliverables..."
}
```

---

## ✅ Features

- Fully RESTful routes
- Validation for input fields
- Robust error handling middleware
- Modular MVC structure
- Designed for mobile frontend integration (e.g., Jetpack Compose, Flutter)

---

## ✍️ Code Quality Tools

- **Prettier** for consistent formatting
- **ESLint** with Node style guide
- Run format + lint using:
  ```bash
  npx prettier --write .
  npx eslint .
  ```

---

## 🧪 Testing the API

Use **Postman**, **Thunder Client** (VS Code), or **curl** to test your endpoints:

```bash
curl -X POST http://localhost:5000/api/notes \
  -H "Content-Type: application/json" \
  -d '{"title":"Test", "content":"This is a test note."}'
```

---

## 📜 License

This project is licensed under the MIT License.

---

## ✨ Author

**Gihan Sanjula**  
Undergraduate IT Student | Horizon Campus  
[GitHub](https://github.com/<your-username>) | [LinkedIn](#)

---

> Ready to move on? Next step is building the frontend using **Jetpack Compose** and integrating this backend. Let me know when you're ready!
