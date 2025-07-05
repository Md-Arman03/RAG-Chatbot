#  RAG-Based Document Chatbot using Streamlit + Gemini API

This is a Retrieval-Augmented Generation (RAG) based chatbot built using **Streamlit**, **Gemini API**, and **ChromaDB**. It allows users to upload documents, automatically summarize and ingest them, and then ask questions based on the content.

---

##  Features

- Upload documents (`PDF`, `DOCX`, `TXT`, etc.)
- Extract and summarize text using Gemini (Google AI Studio)
- Split documents into chunks and store in `ChromaDB`
- Ask questions — chatbot uses context to answer accurately

---

##  Tech Stack

- [Streamlit](https://streamlit.io/)
- [ChromaDB](https://www.trychroma.com/)
- [Gemini API](https://aistudio.google.com/)
- [markitdown](https://pypi.org/project/markitdown/)
- [tiktoken](https://github.com/openai/tiktoken)

---

##  Project Structure

(RAG-Chatbot/
main.py → Streamlit navigation controller
genai_services.py → Summary & QnA with Gemini API
chroma_services.py → Document ingestion & retrieval
( pages/
   ingest_page.py → Upload & ingest documents
   chatbot_page.py → Ask questions to chatbot)
.env → API keys & config
requirements.txt)

---

##  Setup Instructions

### 1. Clone Repo & Set Up Environment

git clone https://github.com/yourname/RAG-Chatbot.git
cd RAG-Chatbot
then open terminal and right side of terminal at + icon there is a arrow click it chane it powershell to commond prompt
type(python -m venv .venv)after
activate it type(.venv/Scripts/activate  # or .venv\Scripts\activate.bat (Windows))

pip install -r requirements.txt
## create .env file
write inside the .env file(
MODEL_BASE_URL="write here your api key wich is created by goole ai studio/"
MODEL_API_KEY=C
MODEL_NAME="gemini-2.0-flash"
CHROMA_COLLECTION_NAME="rag_collection")
## create YOUR_GEMINI_API_KEY
from Google Ai Studio
and paste 

## Run the App
streamlit run main.py
