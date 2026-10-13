# Real-Time Chat Application 💬

A real-time chat application built using React.js, Node.js, Express.js, and Socket.IO.

This project allows multiple users to join a chat room and communicate with each other instantly. Users can enter their name and a room name, join the same room, send messages, and receive messages from other users in real time.

## Features

- Join a chat room using a name and room name
- Real-time messaging between multiple users
- Create and join different chat rooms
- Welcome message when a user joins
- Notification when another user joins the room
- Notification when a user leaves the room
- Display users currently available in the room
- Simple and responsive chat interface
- Real-time client-server communication using Socket.IO

## Technologies Used

### Frontend
- React.js
- JavaScript
- HTML
- CSS
- React Router
- Socket.IO Client

### Backend
- Node.js
- Express.js
- Socket.IO
- CORS

## Project Structure

    chat-application/
    │
    ├── client/
    │   ├── public/
    │   ├── src/
    │   │   ├── components/
    │   │   │   ├── Chat/
    │   │   │   ├── InfoBar/
    │   │   │   ├── Input/
    │   │   │   ├── Join/
    │   │   │   ├── Messages/
    │   │   │   └── TextContainer/
    │   │   ├── App.js
    │   │   └── index.js
    │   └── package.json
    │
    ├── server/
    │   ├── index.js
    │   ├── router.js
    │   ├── users.js
    │   └── package.json
    │
    └── README.md

## How It Works

1. The user enters their name and room name.
2. The user clicks the **SIGN IN** button.
3. The React frontend connects to the Node.js server using Socket.IO.
4. The server adds the user to the selected chat room.
5. Users in the same room can send and receive messages instantly.
6. When a user joins or leaves, the other users in the room receive a notification.

## Running the Project Locally

### 1. Start the Server

Open a terminal and navigate to the server folder:

    cd server
    npm install
    node index.js

The backend server runs on:

    http://localhost:5000

### 2. Start the Client

Open another terminal and navigate to the client folder:

    cd client
    npm install

For this project's current dependency setup, start the client with:

    $env:NODE_OPTIONS="--openssl-legacy-provider"
    $env:PORT="3001"
    node .\node_modules\react-scripts\bin\react-scripts.js start

Open the application in the browser:

    http://localhost:3001

## Real-Time Communication

Socket.IO is used to establish real-time, bidirectional communication between the client and server.

When a user sends a message, the client sends a `sendMessage` event to the server. The server then broadcasts the message to all users connected to the same room.

The application also handles `join` and `disconnect` events to manage users entering and leaving chat rooms.

## Testing

The application can be tested by opening it in two browser tabs.

For example:

    User 1: Jaya Sri
    Room: test

    User 2: Test User
    Room: test

Both users join the same room and can communicate with each other in real time. When one user closes the tab, the other user receives a notification that the user has left the room.

## Future Enhancements

- User authentication
- Private messaging
- Message timestamps
- Emoji support
- MongoDB integration for storing chat history
- Profile pictures
- Online/offline user status

## Author

**Jaya Sri Pilli**

B.Tech Computer Science and Engineering

---

This project was developed as a mini project to demonstrate real-time web communication using React.js, Node.js, Express.js, and Socket.IO.