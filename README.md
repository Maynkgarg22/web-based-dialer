# Web-Based SIP Dialer

This project is a full-featured web-based dialer application built with:

- React (Frontend)
- Node.js + Express (Backend)
- JWT Authentication
- JSSIP + WebRTC (SIP/WebSocket/Media)
- Asterisk (SIP server)
- Coturn (TURN/STUN server)
- Docker Compose for easy deployment

## 🔧 Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/web-dialer.git
cd web-dialer
```

### 2. Create a `.env` file in `/backend`
```bash
cp backend/.env.example backend/.env
```

Edit values as needed.

### 3. Build and run with Docker Compose
```bash
docker-compose up -d --build
```

### 4. Access
- Frontend: http://localhost:3000
- Backend: http://localhost:3001
- SIP over WebSocket: wss://yourdomain.com:8089/ws

## 🧪 Test Users

You can modify `backend/server.js` to add test users:
```js
const users = [{ username: '1001', password: 'testpass' }];
```

## 📦 Folder Structure
```
frontend/      # React app
backend/       # Node API + JWT auth
docker-compose.yml
```

## 🔐 Security Suggestions
- Use HTTPS + Let's Encrypt
- Use strong JWT secrets
- Use bcrypt for passwords
- Enable fail2ban for SIP port protection
