# Chatify — Real-Time Chat App

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socket.io&logoColor=white)

> A real-time chat application with rooms, live messaging, and presence indicators — built with Node.js and WebSockets from scratch (no Socket.io wrapper).

## Features

- 💬 **Instant messaging** — messages delivered in < 50ms via WebSocket
- 🏠 **Chat rooms** — create or join named rooms
- 🟢 **Online presence** — see who is currently active in the room
- 📜 **Message history** — recent messages loaded on join
- 🔒 **Username-based identity** — no account needed, just pick a name

## Tech Stack

| Layer | Tech |
|-------|------|
| Backend | Node.js, `ws` library |
| Frontend | Vanilla JS / React |
| Protocol | Raw WebSocket (no Socket.io) |
| Storage | In-memory message store |

## How It Works

```
User A ──WS──► Server ──broadcast──► User B
                  │
              Room Manager
              (tracks users per room)
```

## Local Setup

```bash
git clone https://github.com/jeetupal31/Chatify.git
cd Chatify
npm install
npm run dev
```

Open http://localhost:3000, pick a username, join a room.

---

Made by [Jeetu Pal](https://github.com/jeetupal31)
