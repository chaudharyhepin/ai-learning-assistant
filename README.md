# AI Learning Assistant

An intelligent learning platform that combines AI-powered features with interactive learning tools to enhance the educational experience.

## 🌟 Features

- **AI Chat Interface**: Real-time conversation with AI assistant powered by Google Gemini
- **Document Management**: Upload and manage PDF/text documents for learning
- **Flashcard System**: Create and practice with digital flashcards for memorization
- **Quiz Management**: Generate and take quizzes based on learning materials
- **Progress Tracking**: Monitor learning progress and performance metrics
- **User Authentication**: Secure user accounts with JWT-based authentication
- **PDF Processing**: Automatic PDF parsing and text extraction

## 🛠️ Tech Stack

### Backend

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB (via Mongoose)
- **Authentication**: JWT
- **AI Integration**: Google Gemini API
- **File Upload**: Multer
- **PDF Processing**: PDF parsing utilities

### Frontend

- **Framework**: React 18
- **Build Tool**: Vite
- **Styling**: CSS
- **HTTP Client**: Axios
- **Markdown Support**: React Markdown components

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB instance (local or cloud)
- Google Gemini API key

## 🚀 Installation

### Backend Setup

1. Navigate to the backend directory:

```bash
cd backend
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the backend directory with the following variables:

```
MONGODB_URI=your_mongodb_connection_string
GEMINI_API_KEY=your_gemini_api_key
JWT_SECRET=your_jwt_secret_key
PORT=5000
FRONTEND_URL=http://localhost:5173
```

4. Start the backend server:

```bash
npm start
```

The backend will run on `http://localhost:5000`

### Frontend Setup

1. Navigate to the frontend directory:

```bash
cd frontend/AI-Learning-Assistant
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file in the frontend directory:

```
VITE_API_URL=http://localhost:5000/api
```

4. Start the development server:

```bash
npm run dev
```

The frontend will run on `http://localhost:5173`

## 📁 Project Structure

```
AI-LEARNING-ASSISTANT/
├── backend/                    # Node.js/Express backend
│   ├── config/                # Configuration files (database, uploads)
│   ├── controllers/           # Route handlers for different features
│   ├── middleware/            # Custom middleware (auth, error handling)
│   ├── models/               # MongoDB schemas (User, Document, Flashcard, etc.)
│   ├── routes/               # API route definitions
│   ├── utils/                # Utility functions (Gemini, PDF parsing, text chunking)
│   ├── uploads/              # User-uploaded files (documents)
│   └── server.js             # Express server entry point
│
└── frontend/                  # React/Vite frontend
    └── AI-Learning-Assistant/
        ├── src/
        │   ├── components/   # Reusable React components
        │   ├── pages/       # Page components for different routes
        │   ├── context/     # React Context for state management
        │   ├── services/    # API service layer
        │   ├── utils/       # Utility functions and configurations
        │   ├── App.jsx      # Main App component
        │   └── main.jsx     # React entry point
        ├── public/          # Static assets
        └── vite.config.js   # Vite configuration
```

## 🔑 Key Features Detail

### Authentication

- User registration and login
- JWT token-based authentication
- Protected routes and controller methods

### AI Chat

- Real-time chat interface
- Integration with Google Gemini API
- Chat history tracking and persistence

### Document Management

- Upload PDF and text documents
- Automatic text extraction from PDFs
- Document listing and detail views
- Text chunking for better AI processing

### Flashcards

- Create flashcard sets
- Study mode with progress tracking
- Multi-choice and text-based flashcards

### Quizzes

- Create custom quizzes
- Multiple-choice questions
- Score calculation and tracking
- Quiz results history

### Progress Analytics

- Track learning sessions
- Monitor quiz performance
- View study statistics

## 🔌 API Endpoints

### Authentication

- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### AI

- `POST /api/ai/chat` - Send message to AI

### Documents

- `GET /api/documents` - List user documents
- `POST /api/documents/upload` - Upload document
- `GET /api/documents/:id` - Get document details
- `DELETE /api/documents/:id` - Delete document

### Flashcards

- `GET /api/flashcards` - List flashcard sets
- `POST /api/flashcards` - Create flashcard set
- `PUT /api/flashcards/:id` - Update flashcard set
- `DELETE /api/flashcards/:id` - Delete flashcard set

### Quizzes

- `GET /api/quizzes` - List quizzes
- `POST /api/quizzes` - Create quiz
- `POST /api/quizzes/:id/submit` - Submit quiz answers

### Progress

- `GET /api/progress` - Get user progress

## 🔒 Environment Variables

### Backend (.env)

```
MONGODB_URI          # MongoDB connection string
GEMINI_API_KEY       # Google Gemini API key
JWT_SECRET           # Secret key for JWT tokens
PORT                 # Server port (default: 5000)
FRONTEND_URL         # Frontend URL for CORS
```

### Frontend (.env)

```
VITE_API_URL         # Backend API URL
```

## 📝 Development

### Available Scripts

**Backend:**

```bash
npm start          # Start the server
npm run dev        # Start with nodemon (auto-reload)
```

**Frontend:**

```bash
npm run dev        # Start Vite dev server
npm run build      # Build for production
npm run preview    # Preview production build
npm run lint       # Run ESLint
```

## 🐛 Troubleshooting

- **MongoDB Connection Error**: Verify your MongoDB URI and that the database is running
- **Gemini API Error**: Ensure your API key is valid and has appropriate permissions
- **CORS Issues**: Check that FRONTEND_URL in backend .env matches your frontend URL
- **Port Already in Use**: Change the PORT in backend .env or use a different port

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Support

For support, please create an issue in the repository or contact the development team.

---

**Happy Learning! 🎓**
