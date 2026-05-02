# 🧠 WebIntel: Autonomous Research Automation & Web Intelligence

[![Hackathon Achievement](https://img.shields.io/badge/Hackathon-2nd%20Prize-gold?style=for-the-badge&logo=hackaday)](https://github.com)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)](https://github.com)

**WebIntel** is a real-time research automation and verification system designed to combat misinformation and provide deep, structured insights from the live web. Instead of relying on static model memory, WebIntel autonomously dispatches a swarm of specialized AI agents to search, extract, cross-verify, and resolve factual conflicts in parallel.

> [!IMPORTANT]
> **National Hackathon Winner 🥈**
> This project was developed during a 36-hour National Hackathon where it secured the **2nd Prize** for its innovative use of multi-agent orchestration and real-time streaming architecture.

---

## 🚀 One-Line Identity
**WebIntel automates research, verifies facts, and explains logic — using parallel agents in real time.**

---

## ✨ Key Features

*   **Parallel Multi-Agent Orchestration**: Dispatches specialized agents (News, Official, Academic, Financial) simultaneously to minimize latency.
*   **Real-Time SSE Streaming**: Watch the AI's "thought process" live as agents find, extract, and verify claims.
*   **Fact-Verification & Conflict Resolution**: Automatically detects numeric and factual contradictions between sources and resolves them using a multi-tier trust logic.
*   **Deep Trust Scoring**: Sources are automatically categorized into trust tiers (High, Medium, Low) with scores assigned based on domain authority.
*   **Advanced Query Modes**:
    *   **Quick**: Fast verification (5s).
    *   **Fact Check**: Balanced deep-dive with re-querying logic.
    *   **Deep Dive**: Exhaustive multi-pass verification (45s).
*   **Comparison & Monitoring**: Compare multiple entities side-by-side or schedule monitors to track changes in facts over time.

---

## 🛠️ Tech Stack

| Component | Technology |
| :--- | :--- |
| **Backend** | Python (FastAPI), Asyncio |
| **LLM Engine** | Google Gemini 1.5 Flash |
| **Search Engine** | Tavily AI (Optimized for AI Agents) |
| **Streaming** | Server-Sent Events (SSE) |
| **Database** | Supabase (PostgreSQL) |
| **Scheduler** | APScheduler |
| **Export** | WeasyPrint (PDF), JSON |
| **Frontend** | Vanilla JavaScript, CSS, HTML5 |
| **Charts** | Chart.js |

---

## 🏗️ System Architecture

The system follows a modular agentic pipeline:

1.  **Planner Agent**: Decomposes user queries into focused sub-tasks.
2.  **Search Agents**: Run parallel web searches via Tavily API.
3.  **Extraction Agent**: Pulls atomic, structured claims from raw web content.
4.  **Verification Agent**: Groups similar claims, calculates confidence, and detects conflicts.
5.  **Report Agent**: Synthesizes the final structured report and citation graph.

---

## 📂 Project Structure

```bash
webintel/
├── backend/
│   ├── agents/          # Specialized AI Agent logic
│   ├── services/        # Gemini, Tavily, Supabase wrappers
│   ├── utils/           # Trust scoring & Conflict resolution
│   ├── models/          # Pydantic data structures
│   ├── main.py          # FastAPI Entry Point
│   └── _pipeline.py     # Agent orchestration logic
└── frontend/
    ├── css/             # Modern UI styling
    ├── js/              # SSE & UI Logic
    └── index.html       # Single Page Application
```

---

## 🚦 Getting Started

### Prerequisites
*   Python 3.10+
*   Node.js (for frontend serving, optional)
*   API Keys: Gemini, Tavily, Supabase

### Installation

1. **Clone the repo:**
   ```bash
   git clone https://github.com/yourusername/webintel.git
   cd webintel
   ```

2. **Backend Setup:**
   ```bash
   cd backend
   pip install -r requirements.txt
   cp .env.example .env # Add your API keys
   uvicorn main:app --reload
   ```

3. **Frontend:**
   Simply open `frontend/index.html` in your browser or let FastAPI serve it at `http://localhost:8000`.

---

## 📊 Demo Queries to Try

*   **Verification**: *"What is the current market cap of Reliance Industries?"* (Shows NSE vs BSE conflict resolution)
*   **Comparison**: *"Compare Jio vs Airtel vs Vi — subscribers and 5G coverage"* (Shows parallel entity tracking)
*   **Deep Dive**: *"What are the latest AI regulations being considered in India?"* (Shows multi-pass autonomous re-querying)

---

## 🛡️ License
Distributed under the MIT License. See `LICENSE` for more information.

---

**Team Antigravity** - Building the future of verifiable intelligence.
🥈 *2nd Prize Winners - National Hackathon*
