# Hi, I'm Sajid Manzoor 👋
### 3. Helpdesk KPI Dashboard [LIVE - Production Engineering]
**Live:** https://hedesk-dashboard.streamlit.app/ | **Code:** helpdesk-kpi-dashboard
- **Caching:** Redis Cache-Aside @st.cache_data TTL 3600s + LRU O(1), Single-Flight, Write-Through
- **Backpressure:** Bounded queues ArrayBlockingQueue, p-limit, Kafka DLQ breach_review
- **Locks:** ReentrantLock(true) fairness, tryLock(500ms), Redlock via Redis
- **Auth:** OPA/Casbin policy engine, JWT 15m + refresh, CSRF
- **Docs:** STRIDE threat model, OWASP Top 10, ADR via log4brains, C4, Swagger, sql_analysis.sql
### ML Engineer | Building Production AI at Scale

I build low-latency, high-availability LLM systems - RAG pipelines & multi-agent orchestration.

### 🚀 Featured Systems (Coinbase-Scale)

**1. Unified Chat Orchestrator** | `LangGraph + Vertex AI + FastAPI`
- Multi-agent orchestration with 650ms p95 latency
- 32% improvement in query resolution
- Designed for 10k+ concurrent sessions

**2. Help Center RAG Pipeline** | `FAISS + sentence-transformers + Gemini`
- Domain-specific retrieval reducing hallucination by 40%
- 340ms retrieval latency at scale
- Automated evaluation framework

### 🛠️ Core Stack
`Python` `Vertex AI` `Gemini` `LangGraph` `FAISS` `LangChain` `FastAPI` `GCP` `Docker`

### 📊 Impact
- Built AI infrastructure handling production traffic
- Focus: Latency, Reliability, Evaluation
- Currently exploring: Advanced RAG, Agent reliability, LLM eval

### 📫 Let's Connect
- Open to ML Engineer / AI Engineer roles (Remote)
- Jammu, India | GMT+5:30

---
⚡ *Building AI that ships to production, not just notebooks*
