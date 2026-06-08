# 💬 Chatify — Real-Time Chat App

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=for-the-badge&logo=socket.io&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)

> A full-stack real-time chat application with JWT auth, Socket.io messaging, image sharing via Cloudinary, email notifications via Resend, and rate limiting via Arcjet.

---

## ✨ Features

- 💬 **Real-time messaging** — instant delivery via Socket.io
- 🟢 **Online presence** — live online/offline status per user
- 🖼️ **Image sharing** — upload and send images (Cloudinary)
- 🔐 **JWT authentication** — HttpOnly cookie sessions with socket auth middleware
- 📧 **Email notifications** — transactional emails via Resend
- 🛡️ **Rate limiting & bot protection** — Arcjet security layer
- 📜 **Message history** — MongoDB-persisted message store

---

## 🗂️ Project Structure

```
Chatify/
├── backend/
│   └── src/
│       ├── server.js
│       ├── controllers/
│       │   ├── auth.controller.js
│       │   └── message.controller.js
│       ├── models/
│       │   ├── User.js
│       │   └── Message.js
│       ├── routes/
│       │   ├── auth.route.js
│       │   └── message.route.js
│       ├── middleware/
│       │   └── socket.auth.middleware.js
│       └── lib/
│           ├── db.js           # MongoDB connect
│           ├── socket.js       # Socket.io server
│           ├── cloudinary.js   # Image upload
│           ├── resend.js       # Email client
│           ├── arcjet.js       # Rate limiting
│           ├── env.js          # Env config
│           └── utils.js
└── frontend/
    └── src/                    # React + Tailwind UI
```

---

## 🚀 Getting Started

### Backend

```bash
cd backend
npm install
cp .env.example .env  # fill in all values
npm run dev
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

---

## ⚙️ Environment Variables (`/backend/.env`)

```env
PORT=3000
MONGO_URI=mongodb://localhost:27017/chatify
JWT_SECRET=your_jwt_secret
NODE_ENV=development
CLIENT_URL=http://localhost:5173

# Cloudinary (image uploads)
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Resend (email)
RESEND_API_KEY=your_resend_api_key
EMAIL_FROM=noreply@yourdomain.com
EMAIL_FROM_NAME=Chatify

# Arcjet (rate limiting)
ARCJET_KEY=your_arcjet_key
ARCJET_ENV=development
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React, TailwindCSS |
| Backend | Node.js, Express.js |
| Real-time | Socket.io |
| Database | MongoDB + Mongoose |
| Auth | JWT + HttpOnly cookies |
| Images | Cloudinary |
| Email | Resend |
| Security | Arcjet |

---

## 👨‍💻 Author

**Jeetu Pal**
[![GitHub](https://img.shields.io/badge/GitHub-jeetupal31-181717?style=flat&logo=github)](https://github.com/jeetupal31)

---

## 📄 License

MIT
