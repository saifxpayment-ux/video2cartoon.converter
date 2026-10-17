# Toonify AI — Starter Project

A beginner-friendly starter for a video-to-3D-cartoon website.

## What works now
- Responsive upload page
- Video file validation and preview
- Cartoon-style selection
- Backend health endpoint
- Safe API-key configuration pattern

## What is not connected yet
The AI conversion endpoint is intentionally a placeholder. A real video-to-video model/API must be selected and connected before it can return a cartoon video. Hosted AI video APIs may charge per generation; free hosting does not mean unlimited free GPU inference.

## Run locally

Requirements: Python 3.10+

```bash
cd backend
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload
```

Then open `frontend/index.html` in your browser. The backend runs at http://127.0.0.1:8000.

For local browser-to-backend calls, serve the frontend over a local web server if your browser blocks file:// requests:
```bash
cd frontend
python -m http.server 5500
```
Open http://127.0.0.1:5500.

## Next step
Choose a video-to-video provider/model, add its API key to backend environment variables, then replace the placeholder in `backend/main.py`. Never put secret API keys in frontend JavaScript.
