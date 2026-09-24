
# ✈️ Smart Trip Planner
### Multi-Agent Travel Planning System using MCP & Supervisor Architecture

An intelligent travel planning platform that leverages a Supervisor Agent, specialized AI agents, and the Model Context Protocol (MCP) to generate personalized, end-to-end travel itineraries.

The system coordinates multiple autonomous agents to research destinations, optimize schedules, suggest accommodations, estimate budgets, and provide a complete travel plan through a centralized orchestration layer.

---

## 🚀 Overview

Traditional travel planning requires users to manually search across multiple platforms, compare options, and organize information.

This project solves that problem using a Multi-Agent AI architecture where specialized agents collaborate under the guidance of a Supervisor Agent to create comprehensive travel plans.

The Supervisor dynamically routes tasks, manages agent communication, aggregates results, and delivers a final itinerary to the user.

---

## 🏗️ Architecture

```text
                            User Request
                                   │
                                   ▼

                    ┌────────────────────────┐
                    │   Supervisor Agent     │
                    │   Task Orchestrator    │
                    └────────────┬───────────┘
                                 │
          ┌──────────────────────┼──────────────────────┐
          │                      │                      │
          ▼                      ▼                      ▼

 ┌────────────────┐   ┌────────────────┐   ┌────────────────┐
 │ Destination    │   │ Hotel Agent    │   │ Budget Agent   │
 │ Research Agent │   │ Accommodation  │   │ Cost Analysis  │
 └────────┬───────┘   └────────┬───────┘   └────────┬───────┘
          │                    │                    │
          └───────────┬────────┴───────────┬────────┘
                      │                    │
                      ▼                    ▼

              ┌─────────────────────────────┐
              │ Itinerary Planning Agent    │
              └──────────────┬──────────────┘
                             │
                             ▼

              ┌─────────────────────────────┐
              │  Final Travel Plan          │
              └─────────────────────────────┘
```

---

## ✨ Key Features

### 🤖 Multi-Agent Collaboration

Multiple AI agents work together to solve complex travel-planning tasks.

### 🎯 Supervisor-Based Orchestration

A central Supervisor Agent manages workflows, task delegation, and result aggregation.

### 🔗 Model Context Protocol (MCP)

Agents communicate through a standardized context-sharing mechanism for consistent decision-making.

### 🌍 Destination Research

- Tourist attractions
- Local recommendations
- Travel insights
- Regional information

### 🏨 Accommodation Planning

- Hotel recommendations
- Budget-friendly options
- Stay optimization

### 💰 Budget Optimization

- Cost estimation
- Expense breakdown
- Budget-conscious recommendations

### 📅 Smart Itinerary Generation

- Day-wise itinerary planning
- Activity scheduling
- Travel optimization

---

## 💡 Problem Statement

Travel planning often involves:

- Multiple websites
- Scattered information
- Time-consuming research
- Manual itinerary creation

This system automates the entire planning process through collaborative AI agents, providing users with a personalized travel experience.

---

## 🛠️ Technology Stack

### AI & Agent Frameworks

- LangGraph
- LangChain
- MCP (Model Context Protocol)

### Backend

- Python
- FastAPI

### AI Models

- OpenAI Models
- Generative AI Workflows

### Development Tools

- Git
- GitHub
- VS Code

---

## 📂 Project Structure

```text
Smart-Trip-Planner/

│
├── supervisor/
│   ├── supervisor_agent.py
│   └── routing_logic.py
│
├── agents/
│   ├── destination_agent.py
│   ├── hotel_agent.py
│   ├── budget_agent.py
│   └── itinerary_agent.py
│
├── mcp/
│   ├── context_manager.py
│   └── communication_protocol.py
│
├── api/
│   └── app.py
│
├── utils/
│
├── requirements.txt
│
└── README.md
```

---

## 🔄 Workflow

```text
Step 1
User submits travel requirements

        ↓

Step 2
Supervisor analyzes request

        ↓

Step 3
Tasks distributed to specialized agents

        ↓

Step 4
Agents gather and process information

        ↓

Step 5
Results aggregated through MCP

        ↓

Step 6
Supervisor validates outputs

        ↓

Step 7
Final travel itinerary generated
```

---

## 🎯 Example Query

### User Input

```text
Plan a 5-day trip to Paris for two people with a budget of $2000.
```

### System Processing

```text
Supervisor Agent
    ├── Destination Agent
    ├── Hotel Agent
    ├── Budget Agent
    └── Itinerary Agent
```

### Output

```text
✅ Day-wise itinerary

✅ Hotel recommendations

✅ Expected budget breakdown

✅ Tourist attractions

✅ Travel tips

✅ Optimized schedule
```

---

## 🔥 Why Multi-Agent Architecture?

Single-agent systems struggle with:

- Complex reasoning
- Task specialization
- Scalability
- Workflow orchestration

Multi-Agent Systems solve these challenges by assigning specialized responsibilities to dedicated agents, enabling more accurate and scalable solutions.

---

## 📈 Future Enhancements

- Flight Booking Agent
- Weather Agent
- Restaurant Recommendation Agent
- Event Discovery Agent
- Real-Time Pricing Agent
- Voice-Based Travel Assistant
- Memory & Personalization Layer
- Multi-Language Support

---

## 🎓 Key Learnings

Through this project, I gained hands-on experience with:

- Multi-Agent Systems
- Agent Orchestration
- MCP Integration
- Workflow Automation
- AI Application Architecture
- Context Management
- Prompt Engineering
- LLM-Based Decision Making

---

## 📸 Screenshots

Add the following:

### Home Page

```text
Screenshot Here
```

### Multi-Agent Workflow

```text
Architecture Diagram Here
```

### Generated Travel Plan

```text
Output Screenshot Here
```

---

## 👨‍💻 Author

### Koushik

Software Engineer | AI Engineer | GenAI Developer

**Core Skills Demonstrated**

- Multi-Agent Systems
- LangGraph
- LangChain
- MCP
- FastAPI
- Python
- AI Workflow Orchestration
- Generative AI

GitHub:
https://github.com/koushik12122000

---

## ⭐ Support

If you found this project useful, please give it a star ⭐

Contributions, ideas, and feedback are always welcome.
