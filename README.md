# 💬 Real-Time Chat Application

A real-time web chat application built using **React.js, Node.js, Express.js, and Socket.IO**.

The application allows multiple users to join chat rooms and communicate instantly. It supports real-time messaging, active-user tracking, and automatic join/leave notifications.

🌐 **Live Demo:**  
https://jayasri-real-time-chat.netlify.app

---

## ✨ Features

- 💬 Real-time messaging using Socket.IO
- 🚪 Join chat rooms using a name and room name
- 👥 Multiple users can communicate in the same room
- 🟢 Displays users currently active in the room
- 📢 Automatic user join notifications
- 👋 Automatic user leave notifications
- ⚡ Instant bidirectional client-server communication
- 🌐 Fully deployed frontend and backend
- 📱 Simple and responsive user interface

---

## 🛠️ Tech Stack

### Frontend

- React.js
- JavaScript
- HTML5
- CSS3
- React Router
- Socket.IO Client

### Backend

- Node.js
- Express.js
- Socket.IO
- CORS

### Development & Deployment

- Git
- GitHub
- Netlify — Frontend Deployment
- Render — Backend Deployment

---

## 🏗️ Application Architecture

```text
              User
                │
                ▼
        ┌─────────────────┐
        │ React Frontend  │
        │    Netlify      │
        └────────┬────────┘
                 │
                 │ Socket.IO
                 ▼
        ┌─────────────────┐
        │ Node.js Server  │
        │ Express.js      │
        │    Render       │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Socket.IO Rooms │
        └─────────────────┘
                 │
        ┌────────┼─────────┐
        ▼        ▼         ▼
     Messages   Users   Notifications
```

---

## ⚙️ How It Works

1. The user enters their **name** and a **room name**.

2. React redirects the user to the chat interface.

3. Socket.IO establishes a real-time connection between the React frontend and Node.js backend.

4. The server adds the user to the requested chat room.

5. When a message is sent, the frontend emits a Socket.IO event to the server.

6. The server broadcasts the message to all connected users in the same room.

7. The application updates and displays the users currently active in the room.

8. When a user disconnects, other users in the room receive a notification.

---

## 📂 Project Structure

```text
Real-time-chat-application/
│
├── client/
│   │
│   ├── public/
│   │   ├── favicon.ico
│   │   └── index.html
│   │
│   ├── src/
│   │   ├── components/
│   │   │   ├── Chat/
│   │   │   ├── InfoBar/
│   │   │   ├── Input/
│   │   │   ├── Join/
│   │   │   ├── Messages/
│   │   │   └── TextContainer/
│   │   │
│   │   ├── icons/
│   │   ├── App.js
│   │   └── index.js
│   │
│   ├── package.json
│   └── package-lock.json
│
├── server/
│   ├── index.js
│   ├── router.js
│   ├── users.js
│   ├── package.json
│   └── package-lock.json
│
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Make sure **Node.js**, **npm**, and **Git** are installed on your system.

### 1. Clone the Repository

```bash
git clone https://github.com/jayasri07-tech/Real-time-chat-application.git
cd Real-time-chat-application
```

### 2. Install Backend Dependencies

```bash
cd server
npm install
```

Start the backend server:

```bash
node index.js
```

The backend runs locally on:

```text
http://localhost:5000
```

### 3. Install Frontend Dependencies

Open another terminal and navigate to the client folder:

```bash
cd client
npm install
```

Start the React application.

For PowerShell:

```powershell
$env:NODE_OPTIONS="--openssl-legacy-provider"
$env:PORT="3001"
node .\node_modules\react-scripts\bin\react-scripts.js start
```

The frontend runs locally on:

```text
http://localhost:3001
```

---

## 🧪 Testing

The application was tested using multiple browser sessions with different usernames joining the same chat room.

### Verified Functionality

- ✅ User can join a chat room
- ✅ Welcome message is displayed
- ✅ Multiple users can join the same room
- ✅ Messages are delivered in real time
- ✅ Active users are displayed
- ✅ Join notifications work correctly
- ✅ Leave notifications work correctly
- ✅ Frontend successfully communicates with the deployed backend

---

## 🌐 Deployment

### Frontend — Netlify

The React frontend is deployed using **Netlify**.

🚀 **Live Application:**  
https://jayasri-real-time-chat.netlify.app

### Backend — Render

The **Node.js + Express.js + Socket.IO** backend is deployed using **Render**.

The deployed frontend establishes a Socket.IO connection with the backend to provide real-time communication.

> **Note:** The backend is hosted on a free Render instance. After a period of inactivity, the server may need a short time to start when the application is opened again.

---

## 🔮 Future Improvements

- 🔐 User authentication and authorization
- 💾 Database integration for persistent messages
- 🕒 Chat history
- ✍️ Typing indicators
- 🔒 Private messaging
- 🟢 Enhanced online/offline status
- 📎 Image and file sharing
- 😀 Emoji support
- 🎨 Improved UI/UX
- 📱 Enhanced mobile responsiveness

---

## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

- Building frontend interfaces using React.js
- Creating backend services with Node.js and Express.js
- Implementing real-time communication using Socket.IO
- Managing chat rooms and connected users
- Handling client-server events
- Debugging frontend and backend integration issues
- Using Git and GitHub for version control
- Deploying a React frontend with Netlify
- Deploying a Node.js backend with Render
- Connecting independently deployed frontend and backend services

---

## 👩‍💻 Author

**Jaya Sri Pilli**  
B.Tech — Computer Science & Engineering

GitHub:  
https://github.com/jayasri07-tech

---

## 📚 Acknowledgements

This project was developed as a **learning and academic project** to gain hands-on experience with real-time web communication and full-stack application deployment.

The development process provided practical experience with **React.js, Node.js, Express.js, Socket.IO, Git, GitHub, Netlify, and Render**, including application configuration, debugging, testing, integration, and deployment.

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐.
