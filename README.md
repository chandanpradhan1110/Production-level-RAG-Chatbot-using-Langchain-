
# 🩺 Build-a-Complete-Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Flask](https://img.shields.io/badge/Framework-Flask-black)
![LangChain](https://img.shields.io/badge/LangChain-RAG-green)
![Pinecone](https://img.shields.io/badge/VectorDB-Pinecone-purple)
![Google Gemini](https://img.shields.io/badge/LLM-Google%20Gemini-orange)

---

## 🚀 Overview

This project is a **Production-Ready Medical AI Chatbot** built using:

- 🔹 Google Gemini API (Google Generative AI)
- 🔹 Pinecone Vector Database
- 🔹 LangChain Framework
- 🔹 Flask Backend
- 🔹 Retrieval-Augmented Generation (RAG)

The chatbot retrieves relevant medical knowledge using vector search and generates intelligent responses using a Large Language Model (LLM).

⚠️ **Disclaimer:** This chatbot is for educational purposes only and does not replace professional medical advice.

---

## 🏗️ Architecture

User Query

↓

Flask Backend

↓

LangChain RAG Pipeline

↓

Pinecone Vector Search

↓

Google Gemini LLM

↓

Final Response



---
## 🧠 How It Works

1. Medical documents are loaded and split into smaller chunks.
2. Each chunk is converted into embeddings.
3. Embeddings are stored inside Pinecone.
4. When a user asks a question:
   - Similar chunks are retrieved from Pinecone.
   - Retrieved context + question are passed to Google Gemini.
   - Gemini generates a context-aware response.
---
## 🛠️ Tech Stack

| Technology        | Purpose               |
| ----------------- | --------------------- |
| Python            | Programming Language  |
| Flask             | Backend Framework     |
| LangChain         | RAG Orchestration     |
| Google Gemini API | Large Language Model  |
| Pinecone          | Cloud Vector Database |
| HTML/CSS          | Frontend UI           |

---

## 📁 Project Structure


Build-a-Complete-Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask/

│

├── app.py

├── ingest.py

├── templates/

│   └── index.html

├── static/

│   └── style.css

├── requirements.txt

├── .env

└── README.md


---
## 🔐 Environment Variables

Create a `.env` file in the root directory:
---

GOOGLE_API_KEY=your_google_api_key_here

PINECONE_API_KEY=your_pinecone_api_key_here

PINECONE_ENV=your_pinecone_environment

PINECONE_INDEX_NAME=medical-chatbot-index


---
## 📦 Installation Guide

### 1️⃣ Clone Repository
---

git clone [https://github.com/yourusername/Build-a-Complete-Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask.git]()

cd Build-a-Complete-Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask


### 2️⃣ Create Virtual Environment

**Windows**

python -m venv venv

venv\Scripts\activate

### 3️⃣ Install Dependencies

pip install -r requirements.txt

## ▶️ Run the Application

Open your browser:

http://127.0.0.1:5000


---
## 🧩 Key Code Snippets

### 🔹 Google Gemini Integration

```python
from langchain_google_genai import ChatGoogleGenerativeAI
import os

llm = ChatGoogleGenerativeAI(
    model="gemini-pro",
    google_api_key=os.getenv("GOOGLE_API_KEY"),
    temperature=0.3
)
---

from langchain.vectorstores import Pinecone
from langchain_google_genai import GoogleGenerativeAIEmbeddings

embeddings = GoogleGenerativeAIEmbeddings(
    google_api_key=os.getenv("GOOGLE_API_KEY")
)

docsearch = Pinecone.from_existing_index(
    index_name=os.getenv("PINECONE_INDEX_NAME"),
    embedding=embeddings
)


---
If you want, I can now:

- Add a professional **architecture diagram (PNG for GitHub)**  
- Add **live demo section**  
- Add **LinkedIn-ready project description**  
- Make a **resume bullet version** for AI Engineer roles  

Tell me what you need 🚀
---
