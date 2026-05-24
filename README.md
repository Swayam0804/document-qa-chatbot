# Document Q&A Chatbot (RAG Pipeline)

A locally-hosted document Q&A system built with Flask, LangChain, FAISS, and Ollama.

## Stack
- **Backend**: Flask REST API
- **RAG Pipeline**: LangChain + FAISS + HuggingFace Embeddings
- **LLM**: Ollama (Llama3, Llama3:8B, Gemma:2B)
- **Supported formats**: PDF, DOCX, CSV

## Run locally
pip install -r requirements.txt
python app.py

## Security
Rate limiting implemented via Flask-Limiter (OWASP).
