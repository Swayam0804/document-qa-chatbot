# Document Q&A Chatbot (RAG Pipeline)

A locally-hosted document Q&A system built with Flask, LangChain, FAISS, and Ollama.
Upload a PDF, DOCX, or CSV — then ask questions about it. Answers come strictly from your document, not the LLM's training data.

## Stack
- **Backend**: Flask REST API
- **RAG Pipeline**: LangChain + FAISS + HuggingFace Embeddings
- **LLM**: Ollama (Llama3, Llama3:8B, Gemma:2B) — runs fully locally
- **Supported formats**: PDF, DOCX, CSV

## Prerequisites
- Python 3.9+
- [Ollama](https://ollama.ai) installed on your machine

## Run Locally

**1. Clone the repo**
```bash
git clone https://github.com/Swayam0804/document-qa-chatbot.git
cd document-qa-chatbot
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Pull an LLM via Ollama**
```bash
ollama pull llama3
```

**4. Run the app**
```bash
python app.py
```

**5. Open in browser**
```bash
http://127.0.0.1:5000
```

## Usage
1. Upload a PDF, DOCX, or CSV file
2. Type your question in the chat
3. Switch models using the dropdown (Llama3, Llama3:8B, Gemma:2B)
4. Click Reset to clear and upload a new document

## Security
- Rate limiting on `/chat` (30/min) and `/upload` (20/hr) via Flask-Limiter
- Debug mode disabled for production hardening
- OWASP API Security risks identified and partially mitigated
