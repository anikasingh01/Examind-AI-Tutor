# Examind AI Tutor

Hi! I'm Anika. Examind is an AI-powered tutor I built to help JEE aspirants
practice and get doubts cleared. The idea was to make a personal-tutor style
chatbot that understands the JEE syllabus, can answer questions from a
dataset of past problems, and tracks how a student is doing over time.

It has a Python/Flask backend that powers the chatbot, a dataset of JEE
questions, and a frontend with login, dashboard, performance tracking, and
the chatbot interface.

## What it does

- **Chatbot tutor** — students can ask doubts in natural language and get
  explanations back. The backend uses an LLM with the JEE dataset as
  context so answers stay relevant to the syllabus.
- **Login / signup** — basic auth flow so each student has their own
  account.
- **Dashboard** — landing screen after login showing the main options.
- **Performance page** — tracks how the student is doing across topics.
- **Landing page** — a public marketing page introducing the tool.

## Folder structure

```text
Examind-AI-Tutor/
│
├── jee tutor backend/
│   ├── app.py              # Flask backend (chatbot + API endpoints)
│   ├── dataset_jee.csv     # JEE questions dataset used by the tutor
│   └── .env                # API keys / config (not committed in real use)
│
└── landingpage/landingpage/
    ├── index.html          # public landing page
    ├── login.html          # login screen
    ├── signup.html         # signup screen
    ├── dashboard.html      # post-login dashboard
    ├── chatbot.html        # chatbot UI
    ├── performance.html    # performance tracking page
    ├── index.js            # frontend logic
    ├── assets/             # images / static files
    ├── scripts/            # additional JS
    ├── styles/             # CSS
    ├── tailwind.config.js  # Tailwind setup
    ├── package.json        # frontend dependencies
    └── license.txt
```

## Tech stack

- **Backend:** Python, Flask
- **AI:** LLM API (configured in `.env`)
- **Data:** CSV dataset of JEE questions (`dataset_jee.csv`)
- **Frontend:** HTML, JavaScript, Tailwind CSS

## How to run

### Backend

```bash
cd "jee tutor backend"
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install flask flask-cors python-dotenv pandas requests
```

Create a `.env` file inside `jee tutor backend/` with your API key:

Then start the server:

```bash
python app.py
```

### Frontend

Open `landingpage/landingpage/index.html` in a browser, or serve the folder
with a simple local server:

```bash
cd landingpage/landingpage
python -m http.server 5500
```

Then go to `http://localhost:5500`.
