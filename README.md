# Gabriel Pradyumna Alencar Costa

**AI Software Engineer** building multi-agent systems and LLM backends for real financial work.

Brazil · [LinkedIn](https://www.linkedin.com/in/gabriel-pradyumna-alencar-costa-8887a6201/) · gabriel.prady1@gmail.com

---

## What I'm building

### [FinAgent](https://github.com/pradyumna-001/FinAgent) — AI copilot for financial analysts

A multi-agent system that generates daily pre-market morning notes and buy/sell/keep recommendations for B3 equities, delivered at 6 AM BRT.

- **5-agent LangGraph pipeline** with parallel fan-out/fan-in: macro context, company events, quantitative valuation, adversarial risk analysis, and an editor agent that writes the final note in Portuguese
- **Human-in-the-loop approval gate** — analysts approve/reject recommendations via Telegram before delivery, with checkpointed graph resume (LangGraph interrupts + Postgres checkpointer)
- **Long-term semantic memory** with pgvector; personalized learning from analyst feedback
- **Production discipline**: RLS-isolated multi-tenant PostgreSQL, Celery workers/beat, Redis, structured logging with correlation IDs, typed state with reducers, CI with unit + integration tests

`Python` `LangGraph` `FastAPI` `PostgreSQL + pgvector` `Celery` `Redis` `NVIDIA NIM` `Tavily` · [Frontend](https://github.com/pradyumna-001/FinAgent-Frontend) in TypeScript/React

## Elsewhere

- **[BrokerAI](https://github.com/prady001/brokerAI)** — multi-agent AI platform for insurance brokerages: policy renewals, claims processing, and CRM with persistent relational memory
- **[Hub de Entidades](https://github.com/Mateusbmelzi/hub-entidades)** — production SaaS for managing university organizations, events, and memberships (React + Supabase, auth + RBAC)
- **[GraphMind](https://github.com/prady001/GraphMind)** — graph-based agentic reasoning engine with structured, traceable decision workflows

## Experience

- **BTG Pactual** — Funds Services: LLM-powered document analysis pipeline extracting structured data from investment fund regulations (LangChain, RAG, NLP)
- **Genial Investimentos** — Asset Management: portfolio analysis for illiquid investment funds
- **Hyperlocal** — Fraud detection models (Random Forest, Gradient Boosting) on transaction data
- **Insper Code** — LLM pipeline for unstructured data extraction from fund regulation PDFs

## Stack

**AI:** LangGraph · LangChain · OpenAI / NVIDIA NIM · RAG · multi-agent systems
**Backend:** Python · FastAPI · Django · PostgreSQL · Supabase · REST
**Infra:** Docker · Celery · AWS · Git
**Also:** TypeScript · React · scikit-learn · XGBoost
