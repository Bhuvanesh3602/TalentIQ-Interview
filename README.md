# 🚀 TalentIQ - Full-Stack Interview Platform

<div align="center">




**A modern, real-time coding interview platform built for seamless technical assessments**

[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6+-green.svg)](https://mongodb.com/)
[![Stream](https://img.shields.io/badge/Stream-Video%20%26%20Chat-orange.svg)](https://getstream.io/)

</div>

----

## ✨ **What is TalentIQ?**

TalentIQ is a comprehensive interview platform that revolutionizes technical hiring by providing a seamless, real-time coding environment where interviewers and candidates can collaborate effectively. Think of it as "Google Meet + LeetCode + VS Code" all rolled into one powerful platform.

---

## 🎯 **Key Features**

### 🧑‍💻 **Real-Time Code Collaboration**
- **VSCode-Powered Editor**: Full-featured code editor with syntax highlighting
- **Multi-Language Support**: JavaScript, Python, Java with instant execution
- **Live Code Sharing**: Real-time code synchronization between participants
- **Instant Execution**: Run code with immediate feedback and error handling

### 🎥 **Advanced Video Conferencing**
- **HD Video Calls**: Crystal clear 1-on-1 video interviews
- **Screen Sharing**: Share screens for better code review and explanation
- **Audio Controls**: Mute/unmute with professional call controls
- **Recording Capability**: Record sessions for later review

### 💬 **Integrated Communication**
- **Real-Time Chat**: In-session messaging for quick clarifications
- **Participant Management**: See who's online and their status
- **Session Notifications**: Get notified about session events

### 🏢 **Session Management**
- **Create Sessions**: Host can create coding challenges instantly
- **Join Sessions**: Participants can join with a simple link
- **Room Locking**: Secure 2-participant limit per session
- **Session History**: Track completed interviews and performance

### 🧩 **Problem Library**
- **Curated Problems**: Hand-picked coding challenges
- **Difficulty Levels**: Easy, Medium, Hard categorization
- **Multiple Examples**: Clear input/output examples for each problem
- **Starter Code**: Pre-written templates for faster coding

### 🔐 **Enterprise-Grade Security**
- **Authentication**: Secure login via Clerk
- **User Management**: Automated user sync and management
- **Session Security**: Protected interview rooms
- **Data Privacy**: Secure data handling and storage

---

## 🛠️ **Technology Stack**

### **Frontend**
```
⚛️  React 18          - Modern UI framework
🎨  Tailwind CSS      - Utility-first styling
🎭  DaisyUI           - Beautiful component library
📝  Monaco Editor     - VSCode-powered code editor
🎥  Stream Video SDK  - Video calling infrastructure
💬  Stream Chat SDK   - Real-time messaging
🔐  Clerk React       - Authentication & user management
🔄  TanStack Query    - Data fetching & caching
🧩  React Router      - Client-side routing
📱  Vite              - Lightning-fast build tool
```

### **Backend**
```
🟢  Node.js           - JavaScript runtime
⚡  Express.js        - Web application framework
🍃  MongoDB           - NoSQL database
🔗  Mongoose          - MongoDB object modeling
🎥  Stream Node SDK   - Video & chat backend
🔐  Clerk Express     - Server-side authentication
⚙️   Inngest          - Background job processing
🌐  CORS              - Cross-origin resource sharing
```

### **External Services**
```
🎥  Stream.io         - Video calling & chat infrastructure
🔐  Clerk             - Authentication & user management
⚙️   Inngest          - Serverless background jobs
🖥️   Piston API       - Secure code execution environment
🍃  MongoDB Atlas     - Cloud database hosting
```

---

## 🏗️ **Architecture Overview**

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │  External APIs  │
│   (React)       │◄──►│   (Node.js)     │◄──►│                 │
│                 │    │                 │    │  • Stream.io    │
│ • Video Calls   │    │ • REST API      │    │  • Clerk Auth   │
│ • Code Editor   │    │ • Session Mgmt  │    │  • Piston API   │
│ • Real-time UI  │    │ • User Auth     │    │  • MongoDB      │
│ • Chat System   │    │ • WebSockets    │    │  • Inngest      │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

---

## 🚀 **Getting Started**

### **Prerequisites**
- Node.js 18+ installed
- MongoDB running locally or MongoDB Atlas account
- Stream.io account for video/chat
- Clerk account for authentication

### **Installation**

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/talent-iq.git
   cd talent-iq
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   
   # Create .env file
   cp .env.example .env
   # Fill in your environment variables
   
   npm run dev
   ```

3. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   
   # Create .env file
   cp .env.example .env
   # Fill in your environment variables
   
   npm run dev
   ```

### **Environment Variables**

**Backend (.env)**
```env
PORT=3000
NODE_ENV=development
DB_URL=mongodb://127.0.0.1:27017/Interview
INNGEST_EVENT_KEY=your_inngest_event_key
INNGEST_SIGNING_KEY=your_inngest_signing_key
STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret
CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key
CLIENT_URL=http://localhost:5173
```

**Frontend (.env)**
```env
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_API_URL=http://localhost:3000/api
VITE_STREAM_API_KEY=your_stream_api_key
```

---

## 📋 **API Endpoints**

### **Sessions**
```
POST   /api/sessions          - Create new interview session
GET    /api/sessions/active   - Get all active sessions
GET    /api/sessions/:id      - Get session by ID
POST   /api/sessions/:id/join - Join existing session
POST   /api/sessions/:id/end  - End session (host only)
GET    /api/sessions/my-recent - Get user's recent sessions
```

### **Authentication**
```
GET    /api/chat/token        - Get Stream authentication token
```

### **Health Checks**
```
GET    /health               - API health check
GET    /test-db              - Database connectivity test
GET    /test-stream          - Stream API connectivity test
```

---

## 🎨 **User Interface**

### **Dashboard**
- **Active Sessions**: Browse and join ongoing interviews
- **Recent Sessions**: View your interview history
- **Create Session**: Start new coding challenges
- **Statistics**: Track your interview performance

### **Interview Room**
- **Split Layout**: Problem description + code editor + video call
- **Resizable Panels**: Customize your workspace
- **Language Selector**: Switch between JavaScript, Python, Java
- **Run Code**: Execute code with instant feedback
- **Chat Integration**: Communicate without interrupting the flow

---

## 🔧 **Development Features**

### **Code Quality**
- ESLint configuration for consistent code style
- Error boundaries for graceful error handling
- Comprehensive logging for debugging
- Type checking with PropTypes

### **Performance**
- Code splitting for faster load times
- Lazy loading of components
- Optimized bundle size with Vite
- Efficient state management with TanStack Query

### **Developer Experience**
- Hot module replacement for instant updates
- Detailed error messages and stack traces
- Development tools integration
- Comprehensive documentation

---

## 🚀 **Deployment**

### **Production Build**
```bash
# Frontend
cd frontend
npm run build

# Backend
cd backend
npm run start
```

### **Environment Setup**
- Configure production environment variables
- Set up MongoDB Atlas for database
- Configure Stream.io for production
- Set up Clerk for authentication
- Deploy to your preferred hosting platform

---

## 🤝 **Contributing**

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---
## 🙏 **Acknowledgments**

- **Stream.io** for providing excellent video and chat infrastructure.
- **Clerk** for seamless authentication solutions.
- **Piston API** for secure code execution environment.
- **MongoDB** for reliable data storage.
- **Vercel** for hosting and deployment solutions.

---

## 📞 **Support**

- 📧 Email: bhuvanesh.s2024aids@sece.ac.in

---
