# LangChain Chatbot (Educational Purposes)

This codebase contains educational examples of building powerful Chatbot applications using LangChain, Streamlit, and different LLM integrations.

## Features
- **Local AI Chatbot (`app.py`)**: A Streamlit application powered by LangChain and a local Ollama model (`llama3.2:1b`), ensuring 100% data privacy.
- **OpenAI Chatbot (`openai.py`)**: A Streamlit application demonstrating how to integrate cloud-based models via the OpenAI API (`gpt-3.5-turbo`).
- **Tracing**: Built-in integration with LangSmith for logging, tracing, and prompt analytics.

## Prerequisites
1. **Python 3.9+**
2. **Ollama**: If using the local model, you must have [Ollama](https://ollama.com/) installed on your machine.
   - Pull the required model by running: `ollama pull llama3.2:1b`
3. **API Keys** (For OpenAI and LangSmith tracing features)

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YASASHWI70/LangChain-Ollama-Chat.git
   cd LangChain-Ollama-Chat
   ```

2. **Create a Virtual Environment (Optional but recommended):**
   ```bash
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   Create a `.env` file in the root directory (this file is git-ignored for your security) and add the following keys:
   ```env
   # LangChain Studio (LangSmith) tracking
   LANGCHAIN_TRACING_V2=true
   LANGCHAIN_API_KEY=your_langchain_api_key_here
   LANGCHAIN_PROJECT=ollama-chatbot

   # Required if running openai.py
   OPENAI_API_KEY=your_openai_api_key_here
   ```

## How to Run

### 1. Run the Local Ollama Model (100% Free & Private)
```bash
streamlit run app.py
```

### 2. Run the OpenAI Model
```bash
streamlit run openai.py
```

## Security Warning ⚠️
Never commit your `.env` file or hardcode your `LANGCHAIN_API_KEY` or `OPENAI_API_KEY` into your Python files! Always use `python-dotenv` to safely load secrets in your environments.
