
# 🧠 SmartDoc-AI: Smart Assistant for Research Documents

**SmartDoc-AI** is an AI-powered assistant that reads and reasons through your uploaded PDF or TXT documents. It delivers concise summaries, answers deep contextual questions, and challenges your understanding with logic-based evaluations. Designed for researchers, students, and professionals, SmartDoc AI bridges the gap between traditional summarizers and true comprehension — powered by **LangChain**, **FastAPI**, **Streamlit**, and **Groq API**.

---

## 🚀 Key Features

- 📄 **Document Upload**: Supports `.pdf` and `.txt` formats
- ✨ **Auto Summary**: Instantly generates a concise summary (≤ 150 words)
- 🤖 **Ask Anything Mode**: Natural language Q&A with grounded, source-based responses
- 🧠 **Challenge Me Mode**: Auto-generates logic-based questions and evaluates your answers
- 🔍 **Justified Answers**: Every response includes a citation or snippet from the document
- ⚡ **RAG Architecture**: Combines semantic search (FAISS) and fast inference (Groq API)
- 💡 **Bonus Capabilities**:
  - 🔁 Context memory for follow-up queries
  - 🎯 Highlighted text spans in answers for clarity

---
## 📁 Project Structure

```text
SmartDoc-AI/
├── backend/
│   ├── vector_database.py
│   └── rag_pipeline.py
├── frontend/
│   ├── streamlit_app.py
│   ├── summary.py
│   ├── ask_questions.py
│   └── self_eval.py
├── requirements.txt
└── .env
```
## 🧰 Tech Stack

| Technology       | Role                                             |
|------------------|--------------------------------------------------|
| **Streamlit**    | Web-based frontend UI                            |
| **LangChain**    | Orchestration of retrieval and LLM prompting     |
| **Groq API**     | High-speed inference using Mixtral or LLaMA      |
| **PyMuPDF**      | PDF parsing and text extraction                  |
| **FAISS**        | Vector similarity search for document chunks     |

---




## 🧠 Architecture Overview

```mermaid
graph TD
    A[User Uploads Document] --> B[Text Extraction using PyMuPDF]
    B --> C[Chunking via LangChain]
    C --> D[Embedding and Indexing in FAISS]
    D --> E[User Question or Challenge Request]
    E --> F[Prompt Generation via LangChain]
    F --> G[LLM Response via Groq API]
    G --> H[Answer with Justification and Snippet]
```


---


## 🛠️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/sangam962895/SummarAIze.git
cd SmartDoc-AI
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
```

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

### 4. Configure Environment

Create a `.env` file and add your API key:

```env
GROQ_API_KEY=your_groq_api_key
```

### 5. Run the Application

```bash

# Start Streamlit frontend (in separate terminal)
streamlit run frontend/streamlit_app.py
```

---

## 📽 Demo Video

👉 [Watch the full demo on YouTube](https://www.youtube.com/watch?v=73hCgYMFIDY)

---

## 🌟 What Makes SmartDoc-AI Unique?

- ✅ Built specifically for long research and technical documents
- ✅ Uses RAG for accurate, reference-backed answers
- ✅ Provides comprehension-level challenge questions
- ✅ Fast response with Groq’s cutting-edge LLM support
- ✅ Modular architecture for easy customization and extension

---

## 🚧 Future Roadmap

- 📄 Support `.docx`, scanned OCR PDFs
- 🗣️ Voice input and multi-language summaries
- 💬 Conversation memory across sessions
- 📤 Export summaries and Q&A logs to PDF or Markdown

---

## 📝 Evaluation Alignment

| Criteria                          | Implementation Highlights                               |
|-----------------------------------|----------------------------------------------------------|
| ✔️ Accuracy + Justification       | Answers grounded in doc with citation                   |
| ✔️ Reasoning Mode                 | Auto Q&A + logic evaluation in "Challenge Me" mode      |
| ✔️ Clean UI/UX                    | Streamlit interface with minimal friction               |
| ✔️ Code Quality                   | Modular FastAPI + frontend/backend separation           |
| ✔️ Bonus Features                 | Memory + snippet highlighting support                   |
| ✔️ Contextual Awareness           | Uses FAISS and LangChain to maintain document context   |

## 📸 Screenshots
  **Landing Page**
  
  <img width="1389" height="677" alt="image" src="https://github.com/user-attachments/assets/24392d07-4cd0-4e46-acdc-e2c3c724cbe4" />

  **Summary**
  
<img width="1164" height="507" alt="image" src="https://github.com/user-attachments/assets/2392dda3-158b-4d50-987f-f485a29d4990" />

  
  **Ask Question**
  
 <img width="1443" height="684" alt="image" src="https://github.com/user-attachments/assets/9c698ab1-f970-4e20-a0e5-827c19bde0b2" />

  
  **Self Evaluation Quiz**
  
  <img width="959" height="452" alt="SelfEvalQues" src="https://github.com/user-attachments/assets/93292ddb-6a4a-4467-8983-5c89440ae4db" />

  
  **Evaluation of Quiz Reasoning**

  <img width="746" height="452" alt="EvaluationOFQuizwithReasoning" src="https://github.com/user-attachments/assets/12e202df-642e-4639-86e9-9cb70270b197" />
  
  **Self Evaluation Score**

  <img width="1478" height="784" alt="image" src="https://github.com/user-attachments/assets/a247953e-6854-4d80-a605-35b6d6804810" />



**👨‍💻 Sangam Kumar**  

 Email: [info.sangamgupta@gmail.com](mailto:info.sangamgupta@gmail.com)  
 
GitHub: [sangam962895](https://github.com/sangam962895)

© 2025 — Smart Assistant Project

SmartDoc-AI smarter. Learn deeper. 🚀
