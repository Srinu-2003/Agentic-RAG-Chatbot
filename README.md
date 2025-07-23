# 🧠 Agentic RAG Chatbot – Multi-Format Document QA System 1

This is a complete **Retrieval-Augmented Generation (RAG)** based chatbot built with an **Agentic Architecture**. It can understand documents of different formats and answer user queries using relevant parts of the content. The project focuses on modular design using agents for each task and integrates powerful NLP tools like HuggingFace and FAISS.

---

## 🌟 Main Highlights

- ✅ **Agent-Based Design** – Separate agents for document parsing, chunk retrieval, and LLM response.
- 📂 **Multiple File Formats** – Works with PDFs, Word, CSV, PPT, and text files.
- 🔍 **Embeddings + Vector Search** – Uses HuggingFace sentence-transformers with FAISS for accurate results.
- 🎯 **User Interface** – Simple UI built using Streamlit for easy document uploads and question-answering.
- 🚀 **Modular & Scalable** – Can be extended with custom models or cloud integrations.

---

## 🧰 Tech Stack

- **Python 3.9+**
- **Libraries:**
  - `Streamlit`
  - `LangChain`
  - `sentence-transformers`
  - `FAISS`
- **Model Management:** HuggingFace
- **Communication Protocol:** Model Context Protocol (MCP)

---

## 🧱 Architecture Flow

1. **Ingestion Agent**
   - Detects file format.
   - Extracts text and splits it into meaningful chunks.

2. **Retrieval Agent**
   - Converts chunks into embeddings.
   - Stores them using FAISS for similarity-based search.
   - Retrieves top-matching chunks based on the user's question.

3. **LLM Response Agent**
   - Combines query and retrieved content.
   - Generates answers using an LLM (e.g., OpenAI, HuggingFace models).

4. **Model Context Protocol (MCP)**
   - Standard JSON message objects are passed between agents to maintain modularity.

---

## 📁 Project Directory

```bash
Agentic-RAG-Chatbot/
├── app.py                    # Streamlit frontend
├── agents/
│   ├── ingestion_agent.py    # Handles parsing documents
│   ├── retrieval_agent.py    # Manages embedding & FAISS
│   ├── llm_response_agent.py # Calls LLM and returns answers
│   └── mcp.py                # Message-passing protocol
├── temp/  
    VIDEO                   # Stores temporary uploads
├── requirements.txt          # Required Python libraries
└── README.md                 # Project overview (this file)
```

---

## 🚀 How to Set Up and Run

### 📌 Requirements

- Python 3.9 or above
- HuggingFace account (if embeddings need a token)

### ⚙️ Installation Steps

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/Agentic-RAG-Chatbot.git
cd Agentic-RAG-Chatbot
```

2. **Set up virtual environment**
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
```

3. **Install the libraries**
```bash
pip install -r requirements.txt
```

4. *(Optional)* Install PyTorch (if not already present)
```bash
pip install torch
```

---

### 🔐 Environment Variables

If required, create a `.env` file:
```env
HF_TOKEN=your_huggingface_token
```

---

## 🏃 Run the Application

Start the chatbot UI using:

```bash
streamlit run app.py
```

---

## 💬 How It Works

1. **Upload your documents** (PDF/DOCX/CSV/PPT/TXT).
2. **Embeddings are generated** and stored in FAISS.
3. **Ask a question** in the Streamlit chat box.
4. **Get an accurate answer** based on the file content using LLM!

---

## 🔍 Challenges I Faced & What I Learned

### 💢 Challenges
- Making different document formats work smoothly.
- Embedding large documents without memory issues.
- Structuring agent communication effectively.

### 📘 Learnings
- Understood LangChain’s modular agent system.
- Learned FAISS integration and efficient document chunking.
- Worked with real-world LLM pipelines.

---

## 🚧 Future Work

- Add advanced model selectors (like OpenAI + HuggingFace mix).
- Maintain a chat history and session memory.
- Convert to a Docker container for easier deployment.
- Add modern UI using React or Flask frontend.

---

## 🙏 Acknowledgements

Thanks to these amazing tools and communities:

- [LangChain](https://github.com/langchain-ai/langchain)
- [HuggingFace Transformers](https://huggingface.co/sentence-transformers)
- [FAISS by Facebook](https://github.com/facebookresearch/faiss)
- [Streamlit](https://streamlit.io)

