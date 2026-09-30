# FitBuddy AI 💪🤖

## AI-Powered Personalized Fitness Plan Generator

FitBuddy AI is a Generative AI-powered fitness planning web application that creates personalized workout plans based on a user's age, weight, fitness goal, and workout intensity.

The application also provides nutrition tips and allows users to submit feedback to generate an updated workout plan.

## ✨ Features

- 🏋️ Personalized 7-day workout plans
- 🤖 AI-powered workout plan generation
- 🥗 Personalized nutrition tips
- 🔄 Feedback-based workout plan updates
- 👤 User information management
- 💾 SQLite database for storing user and workout data
- 📊 View registered users and workout plans
- 🌐 FastAPI-based web application
- 🎨 HTML/CSS frontend
- 📚 Swagger API documentation

## 🛠️ Technologies Used

- Python
- FastAPI
- Jinja2
- SQLAlchemy
- SQLite
- Google Gemini API
- HTML5
- CSS3
- Pydantic
- Uvicorn

## 📁 Project Structure

```text
FitBuddy-AI/
│
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── config.py
│   ├── database.py
│   ├── schemas.py
│   ├── routes.py
│   ├── gemini_generator.py
│   ├── gemini_flash_generator.py
│   └── updated_plan.py
│
├── static/
│   ├── css/
│   │   └── style.css
│   └── images/
│
├── templates/
│   ├── index.html
│   ├── result.html
│   └── all_users.html
│
├── tests/
│   └── test_app.py
│
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/FitBuddy-AI.git
cd FitBuddy-AI
```

### 2. Create a virtual environment

For Windows:

```powershell
py -3.13 -m venv .venv
```

### 3. Activate the virtual environment

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```powershell
python -m pip install -r requirements.txt
```

## 🔑 Gemini API Configuration

Create a `.env` file in the project root.

Example:

```env
GEMINI_API_KEY=your_api_key_here
GEMINI_MODEL=gemini-2.5-pro
GEMINI_FLASH_MODEL=gemini-2.5-flash
AI_DEMO_MODE=false
DATABASE_URL=sqlite:///./fitbuddy.db
```

> ⚠️ Never upload your real `.env` file or API key to GitHub.

Use `.env.example` as the template for environment variables.

## ▶️ Run the Application

Start the FastAPI development server:

```powershell
python -m uvicorn app.main:app --reload
```

Then open:

```text
http://127.0.0.1:8000
```

## 📚 API Documentation

Once the application is running, open Swagger UI:

```text
http://127.0.0.1:8000/docs
```

Health-check endpoint:

```text
http://127.0.0.1:8000/api/health
```

## 🔄 Application Workflow

1. User enters their personal fitness details.
2. FitBuddy AI processes the submitted information.
3. A personalized 7-day workout plan is generated.
4. A nutrition tip is generated.
5. User and workout information is stored in SQLite.
6. The user can submit feedback about the workout plan.
7. FitBuddy AI generates an updated plan based on the feedback.

## 🤖 AI Integration

FitBuddy AI is designed to use Google Gemini models for generative fitness content.

- Gemini Pro model: workout plan generation and workout plan updates
- Gemini Flash model: nutrition tip generation

The project can also be configured to run in demo mode without an API key.

## 🔐 Security

- API keys are stored in environment variables.
- The `.env` file should never be committed to GitHub.
- `.venv/`, `venv/`, database files, and Python cache files should be excluded using `.gitignore`.

## 📌 Important Files

| File | Purpose |
|---|---|
| `app/main.py` | Starts and configures the FastAPI application |
| `app/routes.py` | Web and API routes |
| `app/database.py` | SQLite and SQLAlchemy database operations |
| `app/schemas.py` | Pydantic request/response models |
| `app/gemini_generator.py` | Workout plan generation |
| `app/gemini_flash_generator.py` | Nutrition tip generation |
| `app/updated_plan.py` | Feedback-based workout plan updates |
| `templates/` | HTML pages |
| `static/` | CSS and static assets |
| `requirements.txt` | Python dependencies |

## 🎯 Project Objective

The main objective of FitBuddy AI is to demonstrate how Generative AI can be integrated with a web application to provide personalized fitness planning and interactive workout recommendations.

## 👩‍💻 Project

**Project Name:** FitBuddy AI  
**Project Type:** Generative AI Fitness Planner  
**Backend:** FastAPI  
**Database:** SQLite  
**AI Technology:** Google Gemini

## 📄 License

This project is developed for educational and project demonstration purposes.
