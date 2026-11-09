
# ✈️ TripMate AI
### A Multi-Agent AI Travel Planner powered by LangGraph

🚀 <strong>Live Deployment:</strong> <a href="https://tripmate-ai-a-multi-agent-travel-planner-rs5s.onrender.com/" target="_blank" rel="noopener noreferrer">Try TripMate AI</a>

TripMate AI is an AI-powered travel planning application that transforms natural-language travel requests into structured trip plans using a multi-agent workflow.


## 🎥 Project Demo

Watch TripMate AI generate a complete travel plan using its multi-agent LangGraph workflow.

https://github.com/user-attachments/assets/cf575151-6b27-4515-af3b-ea10a84bef8e


## ✨ Features

- **AI Travel Planning:** Generate personalized travel plans from natural-language requests.
- **Flight Search:** Retrieve flight information using AviationStack.
- **Hotel & Destination Research:** Gather travel information using Tavily Search.
- **Multi-Agent Workflow:** Coordinate specialized AI tasks using LangGraph.
- **Interactive Interface:** Submit travel requests and view generated results through a web interface.
- **Conversation Context:** Maintain conversations using thread IDs.

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Language | Python 3.11 |
| AI & Orchestration | LangGraph, LangChain, Groq |
| APIs & Search | AviationStack, Tavily |
| Backend | FastAPI, Uvicorn |
| Frontend | HTML, CSS, JavaScript |
| Database | PostgreSQL |
| Containerization | Docker |

## 🏗️ Architecture

```text
              User
                |
                v
         Web Interface
                |
                v
             FastAPI
                |
                v
       LangGraph Workflow
                |
          +-----+-----+
          |           |
          v           v
     Flight Agent  Research Agent
          |           |
          v           v
     AviationStack  Tavily
          |           |
          +-----+-----+
                |
                v
          AI Processing
                |
                v
       Generated Travel Plan
                |
                v
          Web Interface
```

## 🚀 Run Locally

**1. Clone the repository**

```bash
git clone https://github.com/LakshyaPandey3/TripMate-AI-A-Multi-Agent-Travel-Planner-with-LangGraph.git

cd TripMate-AI-A-Multi-Agent-Travel-Planner-with-LangGraph
```

**2. Create and activate a virtual environment**

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

**4. Configure environment variables**

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key
AVIATIONSTACK_API_KEY=your_aviationstack_api_key
TAVILY_API_KEY=your_tavily_api_key
DATABASE_URL=your_postgresql_connection_string
```

**5. Start the application**

```bash
uvicorn app:app --reload
```

Open **http://127.0.0.1:8000** in your browser.

## 🐳 Run with Docker

```bash
docker build -t tripmate-ai .
docker run --env-file .env -p 8000:8000 tripmate-ai
```

Open **http://localhost:8000**.

---

**Developed by [Lakshya Pandey](https://github.com/LakshyaPandey3)**
