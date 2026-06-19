# 🚀 Career Copilot AI

An intelligent, production-ready AI career assistant built with **Python, Streamlit, and the Groq API**.

---

## ✨ Features

| Module | Description |
|---|---|
| 📄 Resume Analyzer | Upload PDF/DOCX, extract skills, ATS score, strengths & suggestions |
| 🎯 Job Matcher | Match resume to target roles, salary ranges, missing skills |
| 🧠 Skill Gap Analysis | Visual gap chart, priority learning order |
| 📚 Learning Roadmap | 30/90/180-day personalized roadmaps with resources |
| 🎤 Interview Coach | Question bank + live mock interview with scoring |
| ✉️ Cover Letter | AI-generated, ATS-friendly, PDF export |
| 📊 ATS Score | Deep ATS compatibility scan with quick fixes |
| 🏠 Dashboard | Radar chart, gauges, performance trends |
| ⚙️ Settings | API key, model selection, session management |

---

## 🛠️ Tech Stack

- **Frontend:** Streamlit + Custom CSS (Glassmorphism dark theme)
- **AI:** Groq API — LLaMA 3.3 70B Versatile
- **Database:** SQLite (auth, sessions, interview logs)
- **PDF:** pdfplumber (read) + ReportLab (write)
- **Charts:** Plotly (radar, gauge, bar, pie, line)
- **Auth:** bcrypt password hashing

---

## ⚡ Quick Start

### 1. Clone & install

```bash
git clone <your-repo>
cd career_copilot_ai
pip install -r requirements.txt
```

### 2. Get your Groq API key

Visit [console.groq.com](https://console.groq.com) and create a free API key.

### 3. Run the app

```bash
streamlit run app.py
```

### 4. Login

- Create an account via the Sign Up tab
- Enter your Groq API key on the login screen
- Start analyzing!

---

## 📁 Project Structure

```
career_copilot_ai/
├── app.py                    # Entry point, auth, routing
├── pages/
│   ├── dashboard.py          # Overview charts and metrics
│   ├── resume_analyzer.py    # PDF upload + AI analysis
│   ├── job_matcher.py        # Role compatibility scoring
│   ├── skill_gap.py          # Gap analysis with bar charts
│   ├── learning_roadmap.py   # AI roadmap generator (streaming)
│   ├── interview_coach.py    # Question bank + mock interview
│   ├── cover_letter.py       # Cover letter + PDF export
│   ├── ats_score.py          # ATS deep scan
│   └── settings.py           # API key, profile, data
├── utils/
│   ├── groq_client.py        # Groq API wrapper (stream + sync)
│   ├── pdf_parser.py         # PDF/DOCX text extraction
│   ├── resume_parser.py      # Structured resume extraction
│   ├── prompts.py            # All LLM prompt templates
│   ├── database.py           # SQLite models and queries
│   └── helpers.py            # CSS, UI components
├── database/                 # SQLite DB (auto-created)
├── reports/                  # Generated PDFs
└── requirements.txt
```

---

## 🔧 Configuration

Set these environment variables (optional — key can also be entered at login):

```bash
export GROQ_API_KEY="gsk_your_key_here"
```

Or create a `.env` file:
```
GROQ_API_KEY=gsk_your_key_here
```

---

## 📦 Dependencies

```
streamlit>=1.32.0
groq>=0.5.0
langchain>=0.1.0
pandas>=2.0.0
plotly>=5.18.0
pdfplumber>=0.10.0
python-docx>=1.1.0
reportlab>=4.1.0
SQLAlchemy>=2.0.0
bcrypt>=4.1.0
python-dotenv>=1.0.0
```

---

## 🎨 UI Design

- **Dark Glassmorphism** theme with purple/blue gradient
- Responsive sidebar navigation
- Animated progress bars and hover effects
- Plotly interactive charts (radar, gauge, bar, pie, line)
- Streaming AI responses for roadmap generation

---

## 🤝 Contributing

PRs welcome! Add new pages under `pages/` and prompts under `utils/prompts.py`.

---

**Made with ❤️ using Groq's ultra-fast LLaMA 3.3 70B**
