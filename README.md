# Hi, I'm Theepan Kumar Gandhi

I build **GenAI and machine learning systems that run in production** — not just models in notebooks.

I'm currently finishing my **Master's in Data Science at Illinois Institute of Technology**, and my work is centered around building end-to-end AI systems across:

- **Retrieval-augmented generation (RAG)**
- **Multi-agent LLM systems**
- **LLM evaluation and quality pipelines**
- **Recommender systems and ranking**
- **MLOps, deployment, and observability**
- **Real-time inference APIs**

What I enjoy most is building the full system around the model:
**retrieval, routing, evaluation, serving, monitoring, and iteration.**

---

## What I Focus On

I'm especially interested in problems where:

- LLMs need strong retrieval, grounding, and routing
- models are part of a larger production system
- latency, reliability, and monitoring matter
- evaluation is treated as a first-class part of the stack
- engineering decisions matter as much as model choice

---

## Featured Projects

### Multi-Agent Orchestration Platform
`LangGraph` `FastAPI` `ChromaDB` `PostgreSQL` `Redis` `Prometheus` `Grafana` `Kubernetes` `MCP`

A production-oriented 12-agent LangGraph system built around a supervisor routing pattern, hybrid RAG retrieval, and full observability from day one.

The routing layer uses deterministic rules first — only falling back to an LLM classifier for low-signal queries. Retrieval combines ChromaDB vector search, BM25 lexical ranking, and Reciprocal Rank Fusion with an LLM reranker on top. A knowledge graph agent handles relationship-style local queries via NetworkX. Human-in-the-loop gating is graph-native — Streamlit surfaces Approve/Reject buttons for web and recency queries before they execute. MCP bridges web search and calculator tools with local fallback if unavailable. Caching runs on Redis with automatic in-memory fallback. Persistence is dual-layer: LangGraph PostgreSQL checkpointer for graph state, plus a separate conversation store. Per-user auth, CI/CD via GitHub Actions, and Kubernetes manifests are all included.

[View Repository](https://github.com/Theepankumargandhi/Multi-Agent-Orchestration)

---

### Autonomous CI Failure Fixer
`LangGraph` `FastAPI` `OpenAI` `PostgreSQL` `GitHub Actions API` `Prometheus` `Docker`

An autonomous agent that watches failed GitHub Actions runs, diagnoses the failure, generates a minimal code fix, validates it in an isolated workspace, and opens a pull request — without human intervention.

The system supports two modes: automatic via a GitHub webhook on workflow_run events, and manual via a Streamlit operator console. The LangGraph state machine moves through eight explicit stages — ingest, triage, diagnose, reproduce, patch, validate, evaluate, and PR or escalate. Patch generation uses OpenAI with a heuristic fallback. Every fix must pass lint and tests in a disposable workspace before a PR is opened. Guardrails enforce allowlisted paths only, block secret-like files, and cap patch size. Low-confidence or exhausted retries escalate to a human. Six Prometheus metrics track success rate, MTTR, escalation rate, and false-positive PR rate.

[View Repository](https://github.com/Theepankumargandhi/autonomous-agent-github-actions-ci-fixer)

---

### Finance Document Assistant
`LangChain` `Elasticsearch` `FAISS` `BERT` `MLflow` `DVC` `PostgreSQL` `Docker` `AWS EKS`

A hybrid RAG pipeline for financial documents built around dense and lexical retrieval, LangChain agent workflows, and a full evaluation layer — deployed on AWS EKS.

Retrieval combines BM25 and SentenceTransformer embeddings fused with Reciprocal Rank Fusion over Elasticsearch. A distilBERT extractive QA model handles direct answer extraction. The evaluation pipeline runs automatically — logging Hit Rate, MRR, and latency per query to MLflow. PostgreSQL captures user interactions and satisfaction signals for downstream analysis. The system is containerized with Docker, deployed via GitHub Actions CI/CD to AWS EKS with Kubernetes manifests for namespace, secrets, deployment, and service.

[View Repository](https://github.com/Theepankumargandhi/Finance-Document-Assistant-RAG-Agents)

---

### LLM Annotation Quality Pipeline
`OpenAI` `Cohen's Kappa` `Fleiss' Kappa` `SQLite` `AWS S3` `Streamlit`

A production-grade pipeline for validating annotation consistency and evaluating LLM output quality on QA datasets — treating evaluation as a first-class engineering concern, not an afterthought.

The pipeline ingests raw QA annotations, runs inter-annotator agreement scoring using both Cohen's Kappa and Fleiss' Kappa, validates schema correctness, and scores LLM outputs using an LLM-as-judge approach via the OpenAI API. All results are logged to SQLite with AWS S3 for artifact storage. A Streamlit dashboard surfaces agreement metrics, judge scores, dataset quality summaries, and evaluation trends across runs.

[View Repository](https://github.com/Theepankumargandhi/llm-annotation-quality-pipeline)

---

### QLoRA Notebook Assistant — Mistral-7B Fine-Tuning
`QLoRA` `PEFT` `Mistral-7B` `Hugging Face` `Dual Adapters` `Instruction Tuning`

A fine-tuned assistant for data science notebooks, built to switch between theory explanation and code generation modes — trained under real resource constraints on limited GPU memory.

The core challenge was fitting a 7B model into a constrained training environment. QLoRA handles this via 4-bit quantization combined with LoRA adapters. Two separate adapter sets are trained — one tuned for conceptual explanation, one for code generation — with a routing layer that selects the right adapter based on query intent at inference time. The focus throughout was on practical model behavior: consistent, reliable outputs for technical workflows rather than benchmark-optimized results.

[View Repository](https://github.com/Theepankumargandhi/Data-Science-Notebook-Assistant-Theory-Code-Hybrid-QLoRA-)

---

## Also Worked On

**Multi-Stage Two-Tower Recommender**
`TensorFlow Recommenders` `FAISS` `FastAPI` `MLflow` `DVC` `Airflow` `A/B Testing` `Prometheus`

**AutoML LangGraph Assistant**
`LangGraph` `ChromaDB` `OpenAI GPT-4o` `MLflow` `DVC` `AWS EC2/S3` `MCP` `Docker`

**ECG Anomaly Detection — LSTM AutoEncoder**
`TensorFlow` `Keras` `LSTM AutoEncoder` `Unsupervised` `97.93% accuracy`

**Brain Tumor Segmentation**
`PyTorch` `ResNeXt50-UNet` `Streamlit` `LGG MRI`

---

## Tech I Work With

**LLM / GenAI**
`LangGraph` `LangChain` `LlamaIndex` `RAG` `Agentic AI` `QLoRA` `PEFT` `MCP` `LlamaGuard` `Vector Search` `Hybrid Retrieval` `Reranking`

**ML / Retrieval / Ranking**
`PyTorch` `TensorFlow` `scikit-learn` `FAISS` `BM25` `XGBoost` `MLflow` `DVC`

**Backend / Infra**
`FastAPI` `Streamlit` `PostgreSQL` `Redis` `Docker` `Kubernetes` `AWS` `Azure`

**Monitoring / Ops**
`Prometheus` `Grafana` `GitHub Actions`

---

## Currently Looking For

I'm looking for entry-level roles in:

- Machine Learning Engineering
- Applied AI / GenAI
- Data Science with strong ML systems focus

I'm authorized to work in the U.S. on **F-1 OPT**.

---

## Contact

- Email: [tgandhi1107@gmail.com](mailto:tgandhi1107@gmail.com)
- LinkedIn: [linkedin.com/in/theepankumar](https://www.linkedin.com/in/theepankumar)
- Portfolio: [theepan-portfolio.netlify.app](https://theepan-portfolio.netlify.app)

---

Outside of work, I like trekking and baking.
One clears the head, the other feeds it.

# 💻 Tech Stack:
![R](https://img.shields.io/badge/r-%23276DC3.svg?style=for-the-badge&logo=r&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Windows Terminal](https://img.shields.io/badge/Windows%20Terminal-%234D4D4D.svg?style=for-the-badge&logo=windows-terminal&logoColor=white) ![LaTeX](https://img.shields.io/badge/latex-%23008080.svg?style=for-the-badge&logo=latex&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white) ![Netlify](https://img.shields.io/badge/netlify-%23000000.svg?style=for-the-badge&logo=netlify&logoColor=#00C7B7) ![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white) ![Elasticsearch](https://img.shields.io/badge/elasticsearch-%230377CC.svg?style=for-the-badge&logo=elasticsearch&logoColor=white) ![nVIDIA](https://img.shields.io/badge/cuda-000000.svg?style=for-the-badge&logo=nVIDIA&logoColor=green) ![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi) ![Jinja](https://img.shields.io/badge/jinja-white.svg?style=for-the-badge&logo=jinja&logoColor=black) ![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white) ![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=Apache%20Airflow&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white) ![Neo4J](https://img.shields.io/badge/Neo4j-008CC1?style=for-the-badge&logo=neo4j&logoColor=white) ![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white) ![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white) ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) ![mlflow](https://img.shields.io/badge/mlflow-%23d9ead3.svg?style=for-the-badge&logo=numpy&logoColor=blue) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![Scipy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white) ![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![GitLab CI](https://img.shields.io/badge/gitlab%20CI-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white) ![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white) ![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white) ![ElasticSearch](https://img.shields.io/badge/-ElasticSearch-005571?style=for-the-badge&logo=elasticsearch) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white) ![Riot Games](https://img.shields.io/badge/riotgames-D32936.svg?style=for-the-badge&logo=riotgames&logoColor=white) ![nVIDIA](https://img.shields.io/badge/nVIDIA-%2376B900.svg?style=for-the-badge&logo=nVIDIA&logoColor=white)

