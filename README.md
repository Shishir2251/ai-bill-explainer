# AI Bill Explanation Assistant (MVP)


**What it does**: Upload a PDF or image of a bill; backend extracts text (Tesseract OCR), sends the extracted text to an LLM to analyze and explain charges, and returns a friendly JSON summary + human-readable explanation.


**Features**:
- PDF / image upload
- OCR (pytesseract + pdf2image)
- LLM call (OpenAI / compatible). If no key provided, a local heuristic fallback runs.
- Frontend: simple upload UI and results display


## Quickstart (Linux / macOS / Windows WSL)


1. Install system deps:
- Tesseract OCR:
- macOS: `brew install tesseract`
- Ubuntu: `sudo apt update && sudo apt install -y tesseract-ocr poppler-utils`
- Windows: install from https://github.com/tesseract-ocr/tesseract/releases and add to PATH


2. Clone files into a folder `ai-bill-explainer/` preserving structure.


3. Create virtualenv and install Python deps:
```bash
python -m venv venv
source venv/bin/activate # or venv\Scripts\activate on Windows
pip install -r backend/requirements.txt
