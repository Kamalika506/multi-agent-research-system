# ResearchMind: Multi-Agent AI Research System

An intelligent multi-agent research system that leverages specialized AI agents to autonomously research any topic, synthesize findings, and produce polished research reports with critical evaluation.

**ResearchMind** orchestrates four specialized LangChain agents — Search, Reader, Writer, and Critic — to collaborate on research tasks. It combines web search, web scraping, structured report generation, and quality review into a seamless pipeline.

## Stack

- **Language:** Python 3.8+
- **Framework / Runtime:** LangChain + Streamlit (web UI)
- **LLM:** OpenAI (GPT-4o-mini)
- **Notable Libraries:**
  - **LangChain** (0.2+) — multi-agent orchestration, tool binding, prompt templates
  - **Streamlit** — interactive web interface with real-time pipeline visualization
  - **Tavily** — semantic web search API
  - **BeautifulSoup4** — HTML parsing and text extraction
  - **OpenAI Python client** — LLM inference

## How It's Organized
