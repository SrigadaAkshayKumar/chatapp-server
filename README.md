# CipherThread Backend

CipherThread is a secure messaging application with real-time, end-to-end encryption. The backend is built with Node.js and uses **Express, Socket.io, and Firebase** to facilitate encrypted communication between users.

## Features
- **Real-time messaging:** Uses WebSockets (Socket.io) for instant message delivery.
- **End-to-end encryption:** Messages are encrypted before sending and decrypted only by the recipient.
- **Message storage:** Unread messages are stored in Firebase for offline users.
- **Delivery tracking:** Messages are marked as *seen* when the recipient reads them.

## How It Works
1. **User Connection:** When a user connects, they register their user ID with the backend.
2. **Sending Messages:** The sender sends an encrypted message via WebSocket.
3. **Message Storage:** If the recipient is offline, the message is stored in Firebase.
4. **Real-time Delivery:** If the recipient is online, the message is delivered instantly.
5. **Unread Messages Retrieval:** When a user comes online, they receive any unseen messages.

## API & WebSocket Events
| Event Name             | Type   | Description |
|------------------------|--------|-------------|
| `register`            | Socket | Registers a user with their unique user ID |
| `sendMessage`         | Socket | Sends an encrypted message to another user |
| `receiveMessage`      | Socket | Listens for incoming messages |
| `loadUnseenMessages`  | Socket | Fetches unread messages for a user |
| `markMessagesAsSeen`  | Socket | Marks messages as read when opened |

## Tech Stack
- **Backend:** Node.js, Express
- **Real-time Communication:** Socket.io
- **Database:** Firebase Realtime Database
- **Security:** End-to-end encryption

## Setup Instructions
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/cipherthread-backend.git

2. Navigate to the project directory:

   ```bash
   cd cipherthread-backend
3. Install dependencies:

   ```bash
   npm install
4. Set up your .env file with Firebase credentials:

   ```bash
   PORT=5000
   FIREBASE_PROJECT_ID=your_project_id
   FIREBASE_PRIVATE_KEY_ID=your_private_key_id
   FIREBASE_PRIVATE_KEY=your_private_key
   FIREBASE_CLIENT_EMAIL=your_client_email
   DATABASE_URL=your_firebase_database_url
5. Start the server:

   ```bash
   npm start 

