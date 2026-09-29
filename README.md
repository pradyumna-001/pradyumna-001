# Gabriel Pradyumna Alencar Costa

**AI Software Engineer** — multi-agent systems, LLM applications, and backend infrastructure for real financial work.

Brazil · [LinkedIn](https://www.linkedin.com/in/gabriel-pradyumna-alencar-costa-8887a6201/) · gabriel.prady1@gmail.com

---

## Featured: [FinAgent](https://github.com/pradyumna-001/FinAgent) — AI copilot for financial analysts

A multi-agent system that writes the daily pre-market morning note for Brazilian asset managers: macro context, company events, quantitative valuation, and adversarial risk analysis of every B3 holding in a portfolio — synthesized into a buy/sell/keep recommendation delivered at 6 AM BRT.

**Architecture**

- **5-agent LangGraph pipeline** with parallel fan-out/fan-in — Macro, Company, Quant, Risk, and Editor agents over shared typed state (`AgentState` + reducers), each agent failing visibly via typed `DataFlag`s instead of silent degradation
- **Human-in-the-loop approval gate** — LangGraph `interrupt()` suspends the compiled graph inside a Celery worker; analysts approve/reject via Telegram inline keyboards; a long-polling service resumes the exact suspended run with `Command(resume=...)` against Postgres checkpoints
- **Quant done right** — yfinance metrics (P/L, EV/EBITDA, P/VPA, DY, deviation vs Ibovespa) computed in Python, interpreted by the LLM. The model never does arithmetic
- **Long-term semantic memory** with pgvector; the editor consults analyst feedback history before writing, and every decision feeds back into future recommendations
- **Multi-tenant by construction** — PostgreSQL Row-Level Security with per-transaction `SET LOCAL app.manager_id`; every query is tenant-scoped at the database layer, not the application layer

**Engineering discipline** (the part that doesn't fit on a resume)

- Async SQLAlchemy 2.x + Alembic migrations, Celery workers/beat + Redis, FastAPI with SSE streaming
- 90+ unit tests + integration suite against real PostgreSQL in Docker; ruff + mypy + pytest in CI on every push
- Architecture decisions recorded as ADRs (`docs/adrs/`), daily engineering journal, issue-per-branch workflow with conventional commits
- Structured logging with per-run correlation IDs propagating through workers → graph → API

`Python` `LangGraph` `FastAPI` `PostgreSQL + pgvector` `Celery` `Redis` `Docker` `NVIDIA NIM` `Tavily` — frontend in [TypeScript/React](https://github.com/pradyumna-001/FinAgent-Frontend)

---

## Experience

**BTG Pactual — Funds Services** (intern)
Built an LLM-powered document analysis pipeline extracting structured information from investment fund regulations (LangChain, RAG, NLP), cutting manual analysis time for financial specialists.

**Genial Investimentos — Asset Management** (intern)
Portfolio analysis for illiquid investment funds; valuation concepts and investment operations inside a real asset manager — the domain knowledge behind FinAgent's design.

**Hyperlocal — Machine Learning** (intern)
Fraud detection models (Random Forest, Gradient Boosting) with feature engineering over historical transaction data; >99% predictive performance.

**Insper Code — Developer**
LLM pipeline for unstructured data extraction from investment fund regulation PDFs — implementation, testing, and validation in collaboration with the data team.

---

## Other projects

**[BrokerAI](https://github.com/prady001/brokerAI)** — multi-agent AI platform for insurance brokerages
Autonomous agents with persistent relational memory for policy renewals, claims processing, and customer follow-ups, integrated with insurer APIs. Validated through a production landing page and early customer feedback.

**[Hub de Entidades](https://github.com/Mateusbmelzi/hub-entidades)** — production SaaS for university organizations
Membership, events, and org management with authentication and role-based authorization (React + Supabase).

**[GraphMind](https://github.com/prady001/GraphMind)** — graph-based agentic reasoning engine
Structured, traceable, explainable LLM decision workflows built on LangGraph.

---

## Stack

| | |
|---|---|
| **AI** | LangGraph · LangChain · OpenAI API · NVIDIA NIM · RAG · multi-agent systems · pgvector |
| **Backend** | Python · FastAPI · Django · Flask · PostgreSQL · Supabase · REST · SQLAlchemy |
| **Frontend** | TypeScript · React |
| **ML** | scikit-learn · XGBoost · feature engineering |
| **Infra** | Docker · Celery · Redis · AWS · Git/GitHub · CI |

---

*Older work lives on my previous account: [@prady001](https://github.com/prady001).*
