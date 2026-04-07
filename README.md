
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
cd SummarAIze
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

👉 [Watch the full demo on YouTube](https://youtu.be/kzRCwWFEZGk)

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
  
  <<img width="1198" height="798" alt="image" src="https://github.com/user-attachments/assets/b2c55029-9da2-483c-8ea5-38546330c9b1" />

  **Summary**
  
<img width="1119" height="718" alt="image" src="https://github.com/user-attachments/assets/41a6da75-9f06-421d-af97-c39e88274a74" />


  
  **Ask Question**
  
<img width="1450" height="833" alt="image" src="https://github.com/user-attachments/assets/fc358366-4e88-4352-aa4d-07436fc03ee5" />

  
  **Self Evaluation Quiz**
  
  <img width="959" height="452" alt="SelfEvalQues" src="https://github.com/user-attachments/assets/93292ddb-6a4a-4467-8983-5c89440ae4db" />

  
  **Evaluation of Quiz Reasoning**

  <img width="1406" height="697" alt="image" src="https://github.com/user-attachments/assets/25616208-6b3d-4f3b-b483-c416cb580a12" />

  
  **Self Evaluation Score**

  <img width="1396" height="797" alt="image" src="https://github.com/user-attachments/assets/607ff44d-c4e1-443b-b9e4-7a8cca8430c2" />




**👨‍💻 Sangam Kumar**  

 Email: [info.sangamgupta@gmail.com](mailto:info.sangamgupta@gmail.com)  
 
GitHub: [sangam962895](https://github.com/sangam962895)

© 2025 — Smart Assistant Project

SmartDoc-AI smarter. Learn deeper. 🚀
