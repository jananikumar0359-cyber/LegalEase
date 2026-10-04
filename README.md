# LegalEase — Clean Rebuilt Project

LegalEase is a FastAPI web application for creating editable AI-assisted drafts of:

- Employment Contracts
- Non-Disclosure Agreements (NDAs)
- Residential Lease Agreements

## Features

- FastAPI backend
- HTML/CSS/JavaScript frontend
- Gemini AI integration (optional)
- Built-in local fallback when no API key is configured
- Editable document preview
- Key-term table
- PDF export
- DOCX export
- TXT export
- Optional company/brand name
- No database required

## Project structure

```text
LegalEase/
├── app.py
├── requirements.txt
├── .env.example
├── .gitignore
├── README.md
├── services/
│   ├── __init__.py
│   ├── ai_service.py
│   └── document_service.py
├── templates/
│   └── index.html
└── static/
    ├── script.js
    └── style.css
```

## Requirements

Recommended: Python 3.12+.

## Windows setup

Open the project folder in VS Code, then run:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

If PowerShell activation is blocked:

```cmd
venv\Scripts\activate
pip install -r requirements.txt
```

## Run

```bash
uvicorn app:app --reload
```

Open:

```text
http://127.0.0.1:8000
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

Health check:

```text
http://127.0.0.1:8000/health
```

## Optional Gemini AI

Copy `.env.example` to `.env` and add your Gemini API key:

```text
GEMINI_API_KEY=YOUR_API_KEY
GEMINI_MODEL=gemini-2.5-flash
```

The application still works without a key by using its local document templates.

## Important

This is an educational/product prototype. Generated text can contain errors, omissions, or jurisdiction-specific issues. A qualified legal professional should review any document before it is used or signed.
