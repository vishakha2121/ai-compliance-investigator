<div align="center">

# 🛡️ AI Compliance Investigator

### An Autonomous AI Agent that Investigates Compliance Incidents — End to End

*From incident report intake to final investigation report — fully automated.*

[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![Gemini](https://img.shields.io/badge/Gemini-API-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)]()

</div>

---

## 🎯 What Is This?

**AI Compliance Investigator** is an autonomous AI agent designed to handle corporate compliance incidents (data breaches, policy violations, regulatory breaches, insider threats, etc.) **without manual intervention**.

When a compliance incident is reported, the agent:

1. 📥 **Ingests** the incident report and gathers context
2. 📚 **Retrieves** relevant policies & regulations using **RAG**
3. 🕸️ **Maps** entities (people, departments, policies) via **Knowledge Graph**
4. 💬 **Interviews** stakeholders through **conversational AI workflows**
5. 🔍 **Analyzes** evidence and cross-references findings
6. 📄 **Generates** a structured investigation report with recommendations

The entire workflow is **state-machine driven**, **explainable at every step**, and streams **live updates** to the UI.

---

## 💡 Why This Project?

Traditional compliance investigations are:

| Problem | Impact |
|---------|--------|
| ⏳ **Slow** | Days to weeks per case |
| 👥 **Manual** | Heavy human involvement |
| 📉 **Inconsistent** | No standardized process |
| 🕳️ **Opaque** | Hard to audit decisions |

**AI Compliance Investigator** solves this with autonomous agents that follow a **structured, auditable workflow** while keeping humans in the loop for final approval.

---

## 🏗️ Architecture



---

## 🧠 Core Technologies

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **LLM** | Google Gemini API | Reasoning, chat, report generation |
| **RAG** | ChromaDB + Gemini Embeddings | Policy & regulation retrieval |
| **Knowledge Graph** | NetworkX | Entity-relationship mapping |
| **Workflow Engine** | Custom State Machine | Investigation orchestration |
| **Backend** | FastAPI + SQLAlchemy | REST API + business logic |
| **Database** | SQLite | Incident, evidence, report storage |
| **Frontend** | React + Vite + TailwindCSS | Interactive investigation UI |
| **Real-time** | WebSockets | Live workflow streaming |
| **Visualization** | react-force-graph | Interactive knowledge graph |

> ⚡ **CPU-Friendly**: Runs on any standard laptop — no GPU required.

---

## 🤖 Multi-Agent Design

AI Compliance Investigator uses **4 specialized agents** collaborating:



1. **Investigator Agent** — Orchestrator, drives the workflow
2. **Interviewer Agent** — Conducts stakeholder conversations
3. **Analyst Agent** — Analyzes evidence, cross-references data
4. **Report Agent** — Synthesizes findings into final reports

---

## ✨ Key Features

- 🔄 **Fully Autonomous** — Trigger once, runs end-to-end
- 🧭 **Explainable** — Every decision logged with reasoning
- 💬 **Conversational Interviews** — Natural language stakeholder Q&A
- 🕸️ **Graph-Powered Insights** — Discover hidden relationships
- 📚 **RAG-Grounded** — Answers backed by actual policies
- 📡 **Live Streaming** — Watch investigation progress in real-time
- 📄 **Auto Reports** — Structured findings + recommendations
- 🎨 **Modern UI** — Clean, intuitive investigation dashboard
- 🧩 **CPU-Friendly** — Runs on any laptop, no GPU needed
- 🧪 **Seed Data Included** — Demo incidents ready to try

---

## 📁 Project Structure



---

## 🚀 Quick Start

### Prerequisites
- Python 3.11+
- Node.js 18+
- Gemini API Key ([Get one free](https://aistudio.google.com/app/apikey))

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/vishakha2121/ai-compliance-investigator.git
cd ai-compliance-investigator

cd backend
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate

pip install -r requirements.txt


GEMINI_API_KEY=your_gemini_api_key_here
DATABASE_URL=sqlite:///./compliance.db
CHROMA_DB_PATH=./data/chroma_db

python scripts/init_db.py
python scripts/ingest_documents.py
python scripts/run_demo.py