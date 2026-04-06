Here is a **clean, production-style README.md** for your LangGraph Research Agent project using **Bright Data + SERP API**.

You can paste this directly into your GitHub repo.

---

# 🧠 LangGraph Research Agent

An autonomous research agent built using **LangGraph + LangChain** that performs multi-source web research (Google, Bing, Reddit) and returns a unified, context-aware summary.

The agent orchestrates:

* Multi-engine search
* Result aggregation
* Structured reasoning
* Final synthesized response

---

## 🚀 Features

* 🔎 Multi-source search (Google, Bing, Reddit)
* 🧠 LangGraph-based reasoning workflow
* 🧩 Modular tool architecture
* 🌐 SERP API + Bright Data integration
* 🦙 Local LLM support via Ollama
* 📄 Structured, research-grade outputs

---

## 🛠 Tech Stack

* `langchain>=1.2.0`
* `langgraph>=1.0.5`
* `langchain-ollama>=0.1.0`
* `python-dotenv>=1.2.1`
* Bright Data SERP API
* Ollama (local LLM)

---

# 📦 Installation

```bash
git clone https://github.com/Prasadguru07/LangGraph_research_agent.git
cd Advanced-langflow-Web-Agent-main
pip install -r requirements.txt
```

---

# 🔐 Environment Setup

Create a `.env` file:

```env
# Bright Data
BRIGHTDATA_API_KEY=your_brightdata_api_key

# Ollama model
OLLAMA_MODEL=llama3
```

---

# 🔍 How It Works

1. User query received
2. LangGraph orchestrates:

   * Google search
   * Bing search
   * Reddit search
3. Results collected via Bright Data / SERP API
4. Context aggregated
5. LLM synthesizes final structured response

Graph Flow:

User Query
→ Search Tools
→ Aggregate Results
→ Reasoning Node
→ Final Answer

---

# 🌐 Using Bright Data SERP API

Example request:

```python
import requests
import os

url = "https://api.brightdata.com/serp"

headers = {
    "Authorization": f"Bearer {os.getenv('BRIGHTDATA_API_KEY')}"
}

params = {
    "query": "Latest advancements in AI agents",
    "engine": "google"
}

response = requests.get(url, headers=headers, params=params)
print(response.json())
```

Supported engines:

* google
* bing
* reddit

---

# ▶️ Run the Agent

```bash
python main.py
```

Example:

```bash
Enter your query: Impact of AI in education
```

Output:

* Consolidated insights
* Source synthesis
* Structured explanation

---

# 🧩 Project Structure

```
.
├── main.py
├── prompts.py
├── snapshot_operations.py
├── web_operations.py
├── requirements.txt
├── .env
└── README.md
```

