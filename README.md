# Python Mini AI Agent

**🚀 Live Demo:** [Try the Mini AI Assistant](https://python-mini-ai-agent-rwkwdd7fjvalx56cnohbgq.streamlit.app/)

A Streamlit-based AI assistant prototype that combines a small local language model with news search and PDF question-answering workflows.

## Features

- **Local AI chat:** Runs `HuggingFaceTB/SmolLM2-135M-Instruct` using Transformers and PyTorch.
- **News search mode:** Retrieves recent news results through the DuckDuckGo search library.
- **PDF Q&A mode:** Extracts text from uploaded PDF files with pypdf and adds relevant document text to the model prompt.
- **Conversation context:** Keeps chat messages in Streamlit session state.
- **Simple interface:** Streamlit chat UI with mode selection and clear-chat control.

## Technology

Python · Streamlit · Transformers · PyTorch · Hugging Face · DuckDuckGo search · pypdf

## Run locally

Requirements: Python 3.10+ recommended. A first run downloads the model weights, so allow time and disk space for the model cache.

```bash
git clone https://github.com/sai-manikanta-kadali/mini-ai-agent.git
cd mini-ai-agent
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run app.py
```

Open the local URL printed by Streamlit (normally `http://localhost:8501`).

## How it works

1. Streamlit collects the user's message and selected mode.
2. In chat mode, the local SmolLM2 model generates a response using the available session context.
3. In news mode, the app queries DuckDuckGo and displays returned article titles, sources, dates, summaries, and links.
4. In PDF mode, the app extracts PDF text and includes a bounded text excerpt in the prompt before generating an answer.

## Limitations

- SmolLM2-135M is a compact model; response quality and reasoning capability are limited compared with larger hosted models.
- Model inference can be slow on CPU, and the first launch downloads model files.
- News search depends on the third-party search service and may return incomplete or unavailable results.
- PDF extraction works best with text-based PDFs; scanned/image-only PDFs need OCR.
- Only a limited portion of extracted PDF text is sent to the model.
- This is an educational prototype, not a production assistant. Do not upload confidential documents.

---

Built to explore local LLM inference, Streamlit interfaces, web retrieval, and document-based question answering.