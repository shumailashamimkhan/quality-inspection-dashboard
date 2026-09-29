# 👖 Denim Quality Control AI

An AI-powered quality control dashboard for denim manufacturing.

## Features
- 📊 **Live Dashboard** — KPIs, charts, trend analysis
- 🔍 **Defect Tracking** — 8 defect types across 5 production lines
- 🤖 **AI Assistant** — Ask questions in plain English (Gemini AI)
- 📋 **Detailed Reports** — Line heatmaps, inspector performance
- 📁 **Raw Data View** — Filter & export inspection records

## Project Structure

```
Drnium_quality_control_ai/
├── data/
│   ├── quality_data.csv    ← 520 rows of realistic factory data
│   └── quality.db          ← SQLite database (auto-generated)
├── backend/
│   ├── database.py         ← SQLite helpers
│   ├── analytics.py        ← Pandas analytics
│   └── api.py              ← FastAPI REST API
├── frontend/
│   └── app.py              ← Streamlit dashboard
├── .env                    ← API keys
└── requirements.txt
```

## Setup

```powershell
# 1. Create virtual environment
python -m venv venv
venv\Scripts\activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add your Gemini API key to .env
# GEMINI_API_KEY=your_key_here

# 4. Run the dashboard
streamlit run frontend/app.py

# 5. (Optional) Run the API backend
cd backend
uvicorn api:app --reload --port 8000
```

## AI Assistant
The AI Assistant works in two modes:
- **Demo Mode** (no API key): Rule-based smart answers using real data
- **Live Mode** (with Gemini API key): Full AI answers powered by Google Gemini

## Dashboard Pages
1. **Dashboard** — KPIs + charts
2. **Defect Details** — Tables + heatmap
3. **AI Assistant** — Chat interface
4. **Raw Data** — Filter & export

## Tech Stack
Python · Pandas · SQLite · Streamlit · Plotly · FastAPI · Gemini AI
