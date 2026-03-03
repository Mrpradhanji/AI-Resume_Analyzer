# 🚀 AI Resume Analyzer  
### Modern AI-Powered ATS Resume Checker

<p align="center">
  <b>Analyze resumes against job descriptions using AI</b><br/>
  Built with MERN Stack + LLM Integration
</p>

---

## 🌟 Overview

AI Resume Analyzer is a full-stack Applicant Tracking System (ATS) simulator that evaluates resumes against job descriptions using Large Language Models (LLMs).

It extracts resume content, analyzes it against a Job Description, and provides structured insights including:

- 📊 Resume Match Score (0–100)
- ✅ Matching Skills
- ❌ Skill Gaps
- 💡 Actionable Recommendations
- 🧠 AI Summary
- 🔍 Keywords Extraction
- 🙂 Sentiment Analysis
- 🎤 Suggested Interview Questions

Designed with a modern UI and scalable backend architecture.

---

## 🏗️ Tech Stack

### 🔹 Frontend
- React (Vite)
- Tailwind CSS
- shadcn-style components
- Axios
- Socket.io Client

### 🔹 Backend
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT Authentication
- Worker Queue Architecture
- LLM Integration (OpenAI / Gemini / Anthropic supported)

---

## 📂 Project Structure

```bash
ai-resume-analyzer/
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── jobs/
│   ├── utils/
│   └── server.js
│
└── frontend/
    ├── src/
    └── vite.config.js
```

---

## ⚙️ How It Works

1. User uploads resume (PDF/Text) + optional Job Description.
2. Backend extracts resume text.
3. An Analysis record is created with status: `processing`.
4. Worker job builds structured AI prompt.
5. LLM returns structured JSON output.
6. Parsed fields are saved in MongoDB.
7. Frontend displays insights with live status updates.

---

## 📡 Core API Endpoints

| Method | Endpoint | Description |
|--------|----------|------------|
| POST | `/api/docs/upload` | Upload resume |
| GET | `/api/docs` | List documents |
| GET | `/api/docs/:id/preview` | View analysis |
| POST | `/api/docs/:id/analyze` | Trigger analysis |
| DELETE | `/api/docs/:id` | Delete document |
| GET | `/api/docs/:id/download` | Download original file |

---

## 🧠 AI Analysis Fields

- `resumeScore`
- `summary`
- `matchingSkills`
- `skillGaps`
- `recommendations`
- `keywords`
- `questions`
- `sentiment`
- `keyPoints`

---

## 🛠️ Installation & Setup

### 🔹 Prerequisites
- Node.js ≥ 18
- MongoDB (Local or Cloud)
- Optional: LLM API Key

---

### 🔹 Backend Setup

```bash
cd backend
npm install
```

Create `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
OPENAI_API_KEY=optional_key
```

Start backend:

```bash
npm run dev
```

---

### 🔹 Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Create `.env` file:

```env
VITE_BACKEND_URL=http://localhost:5000
```

---

## 🚀 Running Locally

Backend → http://localhost:5000  
Frontend → http://localhost:5173  

Make sure `VITE_BACKEND_URL` matches backend port.

---

## 💼 Why This Project Stands Out

✔ Real-world ATS simulation  
✔ Clean full-stack architecture  
✔ Worker-based async processing  
✔ Structured LLM JSON parsing  
✔ Production-style API design  
✔ Modern UI/UX  

Demonstrates strong skills in:

- MERN Stack Development
- API Design
- MongoDB Schema Modeling
- AI Prompt Engineering
- Asynchronous Processing
- Full Stack Deployment

---

## 📈 Future Enhancements

- DOCX parsing support
- Resume PDF export with AI suggestions
- User dashboard with analytics
- Resume score history tracking
- Recruiter-mode comparison tool
- Deployment (Vercel + Render)

---

## 👨‍💻 Author

**Rohit Singh**  
Full Stack Developer | MERN | AI Integration  

---

## 📄 License

This project is open-source for learning and demonstration purposes.  
You may add an MIT License if needed.

---

<p align="center">
  ⭐ If you found this project helpful, consider giving it a star!
</p>
