<div align="center">

# 🧠 SmartDoc-AI
### Smart Assistant for Research Documents

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-RAG-1C3C3C?style=flat&logo=chainlink&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-Frontend-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-LLM%20Inference-F55036?style=flat)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20Search-009688?style=flat)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

**SmartDoc-AI** goes beyond traditional summarizers — it reads, reasons, and challenges your understanding of any research document.

[🎥 Watch Demo](https://youtu.be/kzRCwWFEZGk) · [🐛 Report Bug](https://github.com/sangam962895/SummarAIze/issues) · [✨ Request Feature](https://github.com/sangam962895/SummarAIze/issues)

</div>

---

## 📌 Table of Contents

- [About](#-about)
- [Key Features](#-key-features)
- [Architecture](#-architecture)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Screenshots](#-screenshots)
- [Roadmap](#-roadmap)
- [Author](#-author)

---

## 🎯 About

Most document tools just search for keywords. **SmartDoc-AI** actually understands your content.

Built for researchers, students, and professionals who work with dense technical documents — it combines **Retrieval-Augmented Generation (RAG)**, semantic search, and fast LLM inference to deliver accurate, reference-backed answers with zero hallucinations.

> Every response is grounded in your document. No guessing. No made-up facts.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 📄 **Auto Summary** | Instant concise summary (≤ 150 words) of any uploaded document |
| 💬 **Ask Anything** | Natural language Q&A with answers cited directly from the document |
| 🧠 **Challenge Me** | AI generates logic-based questions and evaluates your reasoning — not just right/wrong, but *why* |
| 🔍 **Justified Answers** | Every response includes a source snippet or citation from the document |
| 🔁 **Context Memory** | Follow-up queries maintain conversation context |
| ⚡ **Fast Inference** | Powered by Groq API for near-instant responses |

---

## 🏗 Architecture

```mermaid
graph TD
    A([User Uploads Document]) --> B[Text Extraction\nPyMuPDF]
    B --> C[Chunking\nLangChain]
    C --> D[(FAISS\nVector Index)]
    D --> E{User Action}
    E -->|Ask question| F[Semantic Search]
    E -->|Challenge Me| G[Question Generation]
    F --> H[Prompt Builder\nLangChain]
    G --> H
    H --> I[LLM Inference\nGroq API]
    I --> J([Answer + Justification\nwith Document Snippet])
```

---

## 🧰 Tech Stack

| Technology | Role |
|---|---|
| **Streamlit** | Web-based frontend UI |
| **LangChain** | RAG orchestration and prompt engineering |
| **Groq API** | High-speed LLM inference — Mixtral / LLaMA |
| **FAISS** | Vector similarity search for document chunks |
| **PyMuPDF** | PDF parsing and text extraction |
| **FastAPI** | Backend API layer |

---

## 📁 Project Structure

```
SmartDoc-AI/
├── backend/
│   ├── vector_database.py      # FAISS indexing and embedding logic
│   └── rag_pipeline.py         # RAG chain setup and retrieval
├── frontend/
│   ├── streamlit_app.py        # Main app entry point
│   ├── summary.py              # Auto summary module
│   ├── ask_questions.py        # Ask Anything mode
│   └── self_eval.py            # Challenge Me mode
├── requirements.txt
└── .env                        # API keys (not committed)
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- A [Groq API key](https://console.groq.com/) (free tier available)

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/sangam962895/SummarAIze.git
cd SummarAIze
```

**2. Create and activate a virtual environment**
```bash
python -m venv venv

# On macOS/Linux
source venv/bin/activate

# On Windows
venv\Scripts\activate
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Set up environment variables**

Create a `.env` file in the root directory:
```env
GROQ_API_KEY=your_groq_api_key_here
```

**5. Run the app**
```bash
streamlit run frontend/streamlit_app.py
```

Open your browser at `http://localhost:8501` 🎉

---

## 📸 Screenshots

<details>
<summary>Click to expand</summary>

### Landing Page
![Landing Page](https://github.com/user-attachments/assets/b2c55029-9da2-483c-8ea5-38546330c9b1)

### Auto Summary
![Summary](https://github.com/user-attachments/assets/41a6da75-9f06-421d-af97-c39e88274a74)

### Ask Anything Mode
![Ask Question](https://github.com/user-attachments/assets/fc358366-4e88-4352-aa4d-07436fc03ee5)

### Challenge Me — Questions
![Self Eval Questions](https://github.com/user-attachments/assets/93292ddb-6a4a-4467-8983-5c89440ae4db)

### Challenge Me — Reasoning Evaluation
![Evaluation Reasoning](https://github.com/user-attachments/assets/25616208-6b3d-4f3b-b483-c416cb580a12)

### Challenge Me — Final Score
![Evaluation Score](https://github.com/user-attachments/assets/607ff44d-c4e1-443b-b9e4-7a8cca8430c2)

</details>

---

## 🗺 Roadmap

- [x] PDF and TXT document support
- [x] Auto summary generation
- [x] Natural language Q&A with citations
- [x] Challenge Me mode with reasoning evaluation
- [x] Context memory for follow-up queries
- [ ] Support for `.docx` and scanned OCR PDFs
- [ ] Voice input support
- [ ] Multi-language summaries
- [ ] Export Q&A logs to PDF or Markdown
- [ ] Conversation memory across sessions

---

## 👨‍💻 Author

**Sangam Kumar**

[![Gmail](https://img.shields.io/badge/Gmail-info.sangamgupta%40gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:info.sangamgupta@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-sangam962895-181717?style=flat&logo=github&logoColor=white)](https://github.com/sangam962895)

---

<div align="center">
  <sub>© 2025 SmartDoc-AI — Read smarter. Learn deeper. 🚀</sub>
</div>
