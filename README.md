# Meeting Minutes AI – Automated Transcription and Summarization

This project implements an AI-powered pipeline to automatically generate structured meeting minutes from audio files. It combines speech-to-text and large language models to transform raw meeting recordings into concise, actionable summaries through an interactive web interface.

---

## Project Overview

The system performs the following end-to-end workflow:

1. Accepts a Google Drive link containing a meeting audio file  
2. Downloads and compresses the audio to meet inference API constraints  
3. Transcribes speech to text using a Whisper-based speech recognition model  
4. Generates structured meeting minutes using a LLaMA-based large language model  
5. Presents results through an interactive Gradio web application  

The output includes both the full transcription and a summarized version containing an overview, key discussion points, and action items.

---

## Architecture Flow

Google Drive Audio  
→ Audio Compression & Preprocessing  
→ Speech-to-Text (Whisper)  
→ Text Summarization (LLaMA)  
→ Gradio Web Interface  

---

## Technology Stack

- **Python**
- **Hugging Face Inference API**
  - Whisper (Speech-to-Text)
  - LLaMA 3 Instruct (Text Summarization)
- **Gradio** – Web-based user interface
- **Requests** – API communication
- **python-dotenv** – Secure environment variable management
- **pydub** – Audio processing and compression
- **Regular Expressions (re)** – Google Drive file ID extraction
- **Google Drive** – Audio file hosting

---

## Key Features

- Secure API authentication using environment variables
- Automatic handling of large Google Drive file downloads
- Audio compression optimized for inference API limits
- Robust error handling for API and file-processing failures
- Streaming progress updates during processing
- Clean, user-friendly web interface for non-technical users

---

## Notebook Contents

The `week3_practice.ipynb` notebook contains:
- Environment setup and dependency imports
- Google Drive file handling logic
- Audio preprocessing and compression pipeline
- Whisper-based transcription implementation
- LLaMA-based structured summarization logic
- Gradio UI definition and application launch

---

## Usage

1. Set the `HF_API_TOKEN` in a `.env` file
2. Run the notebook cells sequentially
3. Launch the Gradio interface
4. Paste a Google Drive audio link with sharing enabled
5. Receive transcription and summarized meeting minutes

---

## Use Cases

- Automated meeting documentation
- Enterprise meeting summaries
- Remote team collaboration
- Knowledge capture from recorded discussions

---

## License

MIT License
