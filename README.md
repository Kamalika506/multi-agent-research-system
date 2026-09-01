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

**How it fits together:**

1. **Search Agent** (`tools.web_search`) queries the web via Tavily API and returns top results with titles, URLs, and snippets.
2. **Reader Agent** (`tools.scrape_url`) extracts deep content from the most relevant URL using BeautifulSoup, removing boilerplate (scripts, styles, nav, footer).
3. **Writer Chain** uses a LangChain prompt template to synthesize search results and scraped content into a structured research report (Introduction, Key Findings, Conclusion, Sources).
4. **Critic Chain** evaluates the report with a score (X/10), strengths, areas for improvement, and a verdict.

The **app.py** UI (Streamlit) visualizes progress through step cards and displays results in collapsible panels. The **pipeline.py** CLI runs the same flow for headless/script execution.

## How to Run It

### Prerequisites

- Python 3.8+
- OpenAI API key (`OPENAI_API_KEY`)
- Tavily API key (`TAVILY_API_KEY`)

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Kamalika506/multi-agent-research-system.git
   cd multi-agent-research-system


python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

pip install -r requirements.txt

streamlit run app.py

python pipeline.py
