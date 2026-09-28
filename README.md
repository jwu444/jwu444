## Hi, I'm Justin Wu

**AI-Native Product Builder**
Outcome-driven, human-centric applied AI in machine learning, data science, and data analytics.

I build end-to-end data and machine learning products that solve real-world problems, from the pipeline to the interface people use. I bring listening, communication, empathy, and organization skills built over years of tutoring, coaching, and volunteer leadership.

Cognitive Science student at UC San Diego (Machine Learning and Neural Computation), graduating June 2028. Open to internships in AI/ML engineering, data science, and data analytics.

---

### [Healthcare Revenue Cycle Assistant on Databricks](https://github.com/jwu444/databricks-healthcare-revenue-cycle-assistant)

`Databricks` · `Unity Catalog` · `Delta Lake` · `PySpark` · `SQL` · `Vector Search` · `Genie` · `AI/BI dashboards` · `Asset Bundles` · `Python`

An analytics and AI assistant for a multi-office dental group.

- A medallion data pipeline that transforms raw CSVs into Bronze, Silver, and Gold Delta tables powering an AI/BI dashboard.
- RAG over practice-management documentation, so operational how-to answers are grounded in relevant source content.
- A Databricks Genie agent for natural-language analytics over curated data, with accuracy improved through richer metadata and semantic context.
- A multi-agent supervisor application that orchestrates the RAG and Genie agents to answer real-world questions across structured and unstructured data.

### [ML Experiment Tracker with Continuous Learning](https://github.com/jwu444/ml-experiment-tracker-mlflow-optuna) · [live demo](https://wavepoint-web.onrender.com)

`FastAPI` · `React` · `TypeScript` · `PostgreSQL` · `pgvector` · `MLflow` · `Optuna` · `scikit-learn` · `Claude API` · `OpenTelemetry` · `Docker`

An AI-assisted experimentation platform that continuously learns from model runs and user feedback to improve tuning recommendations.

- An AI-assisted model tuning loop with MLflow, Optuna, and Claude that analyzes prior experiments and recommends the next configurations to test.
- A RAG layer on pgvector over experiment history and human-reviewed run notes and findings, so successful decisions, failed attempts, and human evaluations compound into better recommendations.
- Evaluation guardrails for retrieval: a labeled test set and baseline comparisons, with changes promoted only when they showed measurable improvement.

> The demo sleeps after about 15 minutes idle, so the first request takes about 50 seconds.

### [Data Exploration and Analysis Assistant](https://github.com/jwu444/csv-analysis-assistant-fastapi-react)

`FastAPI` · `React` · `Vite` · `PostgreSQL` · `SQLAlchemy` · `Alembic` · `Claude API with tool calling` · `pandas` · `matplotlib` · `pytest` · `Vitest`

An AI-assisted data exploration and analysis tool that turns uploaded datasets into charts, statistics, and natural-language insights.

- An AI-driven analysis workflow that profiles uploaded CSVs, identifies relevant analytical paths, selects appropriate charts and statistics, and generates plain-English interpretations.
- An analyst-and-judge loop: one agent performs the exploration and analysis, and a second evaluates the output against the rendered results and selects the highest-quality response.
- The AI is restricted to a governed set of analysis tools rather than arbitrary code execution, with versioned prompts, shared UI components, and automated backend and frontend testing.

---

### How I work

All three projects were built in a GitHub-based, AI-native product development lifecycle:

- I own the goals, architecture, design, and verification, and steer coding agents through rapid implementation cycles.
- Every change runs through GitHub issues, pull requests, reviews, automated tests, and CI, with clear acceptance criteria to guide and validate agent-generated changes.
- Project context and design decisions are versioned in GitHub, and a custom Claude Code skill runs the full CI pipeline locally.

### Experience

- **Wave Point (WVPoint LLC)**, AI Engineering & Startup Intern · Jun 2026 – Sep 2026. A 12-week, full-time AI engineering program at an early-stage startup that builds AI automation for small business owners; the three projects above.
- **Neoboard**, AI Researcher & Engineer Intern · Jan 2026 – Jun 2026. AI citation verification for academic writing.
- **Carrette Lab, UC San Diego**, Undergraduate Research Intern · Jan 2025 – Dec 2025. Predicting behavioral outcomes from neuroimaging data.

### Skills

**Machine learning:** Regression (LASSO, Ridge, Elastic Net), classification, PCA, LDA, feature engineering, cross-validation, hyperparameter tuning, model and retrieval evaluation (MRR, precision@k, recall@k), fine-tuning (SciBERT, Hugging Face, PyTorch), NLP (spaCy)

**Data and analytics:** Python (pandas, NumPy, scikit-learn, matplotlib), SQL, R (glmnet, tidyverse, ggplot2), MATLAB, PostgreSQL, Databricks (Unity Catalog, Delta Lake, PySpark, AI/BI dashboards), MLflow, Optuna, Tableau, Power BI

**AI and LLMs:** RAG, vector search (pgvector, Databricks Vector Search), agents and tool use, prompt engineering, Claude, OpenAI, and Gemini APIs, AI-native development with Claude Code

**Product engineering:** FastAPI, REST API design, React, TypeScript, UI design systems, Docker, GitHub Actions CI, pytest, Vitest, OpenTelemetry, Render, Git

---

[LinkedIn](https://www.linkedin.com/in/justin-wu-fairfax-va/)
