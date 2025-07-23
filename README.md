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

# 🤖 Agentic RAG Chatbot with MCP

This is a modular Retrieval-Augmented Generation (RAG) chatbot with ingestion, retrieval, and LLM response agents integrated using MCP messaging.

---

## 📦 Installation Steps

```bash
# 1. Clone the repository
git clone https://github.com/Srinu-2003/Agentic-RAG-Chatbot.git
cd Agentic-RAG-Chatbot

# 2. Create a virtual environment
python -m venv .venv

# 3. Activate the virtual environment
# For Windows
.venv\Scripts\activate
# For Linux/Mac
source .venv/bin/activate

# 4. Install the required dependencies
pip install -r requirements.txt

# 5. Create a `.env` file in the root folder and add your API keys
touch .env
```
## 🔐 API Key Setup Guide (.env File)

Follow these steps to configure your API keys safely using a `.env` file.

### 📁 Step 1: Create the `.env` File

```bash
touch .env
```

### 📝 Step 2: Open the `.env` File with Nano Editor

```bash
nano .env
```

### 🔑 Step 3: Add the Following API Keys to the File

```env
HF_TOKEN=hf_ # put ur
GROQ_API_KEY= # put ur
OPENAI_API_KEY= #pur ur
```

### 💾 Step 4: Save and Exit Nano Editor

- Press `Ctrl + X` to exit.
- Press `Y` to confirm saving.
- Press `Enter` to save the file.

---

✅ Done! Your `.env` file is now configured with all API keys.

🛑 **Important:** Do not upload `.env` to GitHub. Add it to your `.gitignore`:

```bash
echo ".env" >> .gitignore
```


---

## 🚀 Running the App

```bash
# Run the Streamlit app
streamlit run app.py
```

Then open your browser and go to:  
[http://localhost:8502](http://localhost:8502)

---

## 🧠 Project Overview

- **Ingestion Agent**: Parses and chunks documents.
- **Retrieval Agent**: Embeds and fetches relevant chunks.
- **LLM Response Agent**: Uses retrieved context to generate accurate answers using an LLM.

---

## 📁 File Structure

```
Agentic-RAG-Chatbot/
│
├── agents/
│   ├── ingestion_agent.py
│   ├── retrieval_agent.py
│   ├── llm_response_agent.py
│   └── mcp.py
│
├── utils/
│   ├── loaders.py
│   └── text_splitter.py
│
├── .env
├── app.py
├── requirements.txt
└── README.md
```

---

## 💡 Note

Make sure your `.env` file is created and API keys are valid. If `venvlauncher.exe` error occurs during venv creation, ensure:
- Python is added to PATH
- Installed for all users


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

