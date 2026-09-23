# Smart Travel Planner

An intelligent multi-agent travel planning system built with **LangGraph**, **MCP (Model Context Protocol)**, a **Supervisor agent**, **Input Guardrails**, and **Human-in-the-Loop (HITL)** approval flows.

The platform helps users plan complete trips — flights, hotels, weather, budget — all orchestrated by AI agents, with a human review step before the final itinerary is generated.

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-latest-green)
![LangGraph](https://img.shields.io/badge/LangGraph-Agent%20Framework-orange)

---

## Features

- **Multi-Agent Architecture** — Separate agents for flights, hotels, weather, and budget, coordinated by a supervisor
- **MCP Integration** — Custom MCP server for weather data with extensible adapter pattern
- **Supervisor Agent** — Orchestrates which agents to invoke based on user intent
- **Input Guardrails** — Validates and filters user requests before processing
- **Human-in-the-Loop** — Draft plans are presented for user approval/revision before finalizing
- **Interactive Web UI** — Clean FastAPI-powered frontend with quick prompts and PDF export

---

## Project Structure

```
├── app.py                        # FastAPI web server and API endpoints
├── backend.py                    # Core agent orchestration and travel-planner logic
├── mcp_client.py                 # Client helpers for MCP server interaction
├── custom_weather_mcp_server.py  # Custom MCP server for weather data
├── templates/
│   └── index.html                # Frontend UI template
├── static/
│   ├── style.css                 # Styling
│   └── script.js                 # Frontend logic
├── requirements.txt              # Python dependencies
├── Dockerfile                    # Docker support
└── .env                          # API keys and secrets (not committed)
```

---

## Tech Stack

| Component        | Technology                          |
|------------------|-------------------------------------|
| Backend          | FastAPI, Python                     |
| Agent Framework  | LangGraph, LangChain                |
| LLM              | Groq (Llama models)                 |
| Search           | Tavily API                          |
| Flights          | AviationStack API                   |
| Weather          | OpenWeatherMap API (via MCP)        |
| Database         | PostgreSQL (Render)                 |
| Tracing          | LangSmith                           |
| Frontend         | HTML, CSS, JavaScript               |

---

## Getting Started

### Prerequisites

- Python 3.10+
- Git

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd Smart-Travel-Planner
   ```

2. **Create a virtual environment**
   ```powershell
   python -m venv .venv
   .venv\Scripts\Activate.ps1    # PowerShell
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**

   Create a `.env` file in the root directory with the following keys:
   ```env
   DATABASE_URL=<your-postgresql-url>
   GROQ_API_KEY=<your-groq-api-key>
   AVIATIONSTACK_API_KEY=<your-aviationstack-key>
   TAVILY_API_KEY=<your-tavily-api-key>
   OPENWEATHER_API_KEY=<your-openweather-key>
   LANGSMITH_API_KEY=<your-langsmith-key>
   LANGSMITH_TRACING=true
   LANGSMITH_ENDPOINT=https://api.smith.langchain.com
   LANGSMITH_PROJECT=travel-agent
   ```

5. **Run the application**
   ```bash
   python app.py
   ```
   Or with uvicorn:
   ```bash
   uvicorn app:app --reload --host 127.0.0.1 --port 8000
   ```

6. **Open the UI** — Visit `http://127.0.0.1:8000`

---

## Running the MCP Weather Server

If you want to use the custom weather MCP server, start it in a separate terminal:

```bash
python custom_weather_mcp_server.py
```

---

## API Endpoints

| Method | Endpoint              | Description                                    |
|--------|-----------------------|------------------------------------------------|
| GET    | `/`                   | Web UI                                         |
| POST   | `/api/travel`         | Create or resume a travel planning thread      |
| POST   | `/api/travel/approve` | Approve or revise a draft itinerary            |
| GET    | `/health`             | Health check and features list                 |

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
