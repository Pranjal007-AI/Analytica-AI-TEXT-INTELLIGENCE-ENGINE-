# ANALYTICA — AI Text Intelligence Engine

> Extract every insight. Powered by Mistral Large.

🔗 **Live Demo:** [analytica-ai-text-intelligence-engine.netlify.app](https://analytica-ai-text-intelligence-engine.netlify.app/)

---

## What is ANALYTICA?

ANALYTICA is an AI-powered text analysis tool that takes any text — article, news, research, product copy — and returns structured intelligence instantly.

Drop in any text and get:
- Title & Category detection
- Key Entities extraction
- Key Points & Important Data
- Timeline (if present)
- Insights & Sentiment
- Summary
- AI-generated Visual (Pollinations.ai)
- Voice Summary (Browser TTS)

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, Vanilla JS |
| Backend | FastAPI (Python) |
| AI Model | Mistral Large (via LangChain) |
| Image Generation | Pollinations.ai API |
| Voice | Browser Web Speech API|
| Backend Hosting | Render |
| Frontend Hosting | Netlify |

---

## Features

- **Real-time Genre Detection** — detects 30+ genres as you type
- **Structured Extraction** — title, category, entities, key points, data, timeline, insights, sentiment, summary
- **AI Visual** — generates a cinematic image based on the content
- **Voice Summary** — auto-reads the summary aloud after analysis
- **Raw Output Toggle** — view the raw model response
- **Retry Logic** — handles Render cold starts automatically
- **Keyboard Shortcut** — `Ctrl + Enter` to analyze

---

## Project Structure

```
analytica/
├── main.py          # FastAPI backend
├── index.html       # Frontend (single file)
├── requirements.txt # Python dependencies
└── .env             # API keys (not committed)
```

---

## Setup & Run Locally

### Backend

```bash
# Clone the repo
git clone https://github.com/your-username/analytica.git
cd analytica

# Install dependencies
pip install -r requirements.txt

# Create .env file
echo "MISTRAL_API_KEY=your_key_here" > .env

# Run backend
uvicorn main:app --reload
```

### Frontend

Just open `index.html` in your browser — no build step needed.

Make sure `BACKEND_URL` in `index.html` points to your backend:
```javascript
const BACKEND_URL = "http://localhost:8000"; // for local
```

---

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `MISTRAL_API_KEY` | ✅ Yes | Mistral AI API key |

---

## Deployment

**Backend → Render**
1. Push code to GitHub
2. Create new Web Service on Render
3. Add `MISTRAL_API_KEY` in Environment Variables
4. Deploy

**Frontend → Netlify**
1. Drag and drop `index.html` on Netlify
2. Done ✅

---

## Screenshots

> Coming soon

---

## License

MIT License — free to use and modify.

---

Made with ❤️ by [Pranjal Parashar]
