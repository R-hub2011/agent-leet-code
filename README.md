# Local AI Coding Helper

A powerful desktop application that allows you to interact with Google's Gemini AI model for solving coding problems. Supports text, speech, and screenshot input, all within a sleek and stealthy GUI built using Python and CustomTkinter.

---

## Features

- **Text Input**: Type your coding questions directly into the app.
- **Gemini AI**: Uses Google’s Gemini 2.0 Flash model to generate Python or Java solutions with explanations.
- **Screenshot OCR**: Take a screenshot (`Ctrl + H`) and extract coding text using Tesseract OCR.
- **Voice Input**: Hold `F2` to dictate your question, transcribed live via Google Speech Recognition.

---

## Requirements

- Python 3.7+
- Tesseract OCR installed (e.g. in `C:\Program Files\Tesseract-OCR\tesseract.exe`)

### Python Packages

Install required packages with pip:

```bash
pip install customtkinter python-dotenv google-generativeai pytesseract pillow keyboard pywin32 SpeechRecognition
```

## Setup
1. Download and install Tesseract OCR.
2. Create a .env file in your project folder:
```
GOOGLE_API_KEY=your_google_gemini_api_key
```
3. Verify Tesseract path in the code:
```
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```
4. Run the Python file:
```
python your_script_name.py
```
## How It Works
- Detects coding language (Python or Java) automatically.
- Builds a prompt with instructions for Gemini AI.
- Fetches AI response and displays it with full explanation.
- Integrates Tesseract for OCR and SpeechRecognition for voice input.

## Notes
- Designed for Windows OS. 
- To use on other platforms, modify win32gui, win32con, and ctypes sections.
- Internet is required to use Gemini API.