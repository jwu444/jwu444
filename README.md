## Hi, I'm <!-- TODO: your name -->

<!-- TODO: adjust the wording if you want, but this is the agreed positioning. -->
Applied AI engineer working across data science and machine learning, from the pipeline through to the application. Open to internships in AI/ML engineering, data engineering, and data science.

I work in **applied AI across data science and machine learning**, and I ship it two ways: as **end-to-end data pipelines** and as **full-stack applications** people actually use. Three projects below, in the order I would want them read. Each one is a complete working system rather than a notebook.

---

### [Healthcare Revenue Cycle Assistant](https://github.com/jwu444/databricks-healthcare-revenue-cycle-assistant)

`Databricks` · `Unity Catalog` · `Delta Lake` · `Vector Search` · `Genie` · `Asset Bundles`

A six-part build on Databricks for a multi-location dental practice, organized around one split: **structured data answers _"what happened in our practice?"_, documents answer _"how is this work done?"_** — and neither can answer the other's question.

- **Medallion** bronze → silver → gold across 20 tables and ~50k rows of synthetic data, an AI/BI dashboard, and CI/CD through Declarative Asset Bundles
- **RAG** over 31 practice-management PDFs: `ai_parse_document` → semantic chunking → Delta Sync vector index with managed embeddings
- **Genie agent** over the silver tables, answering in plain English with the SQL shown

The lesson the project is built around: **Genie accuracy is a metadata problem, not a model problem.** A better model writes better SQL *given the same understanding of the schema* — it cannot guess that a benefit year starts on September 1 rather than January 1, or that a denial code stores the literal string `'N/A'` instead of NULL. Table comments and a value inventory moved it further than a model swap would have.

Retrieval was measured, not assumed: answerable questions returned the right source document at 0.70–0.76, while a deliberately unanswerable data question scored **0.54** — a visible cliff that says *this is a question for the tables, not the documents*.

---

### [ML Experiment Tracker](https://github.com/jwu444/ml-experiment-tracker-mlflow-optuna) · **[live demo](https://wavepoint-web.onrender.com)**

`MLflow` · `Optuna` · `Postgres + pgvector` · `scikit-learn` · `FastAPI` · `React` · `OpenTelemetry`

Training runs logged to MLflow, hyperparameter search driven by Optuna, semantic retrieval over experiment history, and an agent that reads what you have already tried and recommends what to run next. The working domain is computer-component pricing and demand.

Forked from the CSV assistant below, which made the inherited design decisions explicit rather than incidental — the upload-and-ask flow and the judge-gated loop carry over unchanged.

Deployed on Render with models in Cloudflare R2, because free-tier disks are wiped on every deploy. The runbook documents the deployment step by step, including the three failures that cost the most time.

> **Cold start:** the demo sleeps after ~15 minutes idle, so the first request takes about 50 seconds. It is cold, not broken.

---

### [CSV Analysis Assistant](https://github.com/jwu444/csv-analysis-assistant-fastapi-react)

`FastAPI` · `React + Vite` · `Claude tool-calling` · `pandas` · `SQLAlchemy`

The origin project the other two compound on. Upload a CSV, ask a question in plain language, get charts, statistics, and a written interpretation.

The part worth reading the code for is the **judge-gated loop**. An analyst pass selects chart tools from a fixed menu and writes an interpretation; a *separate* judge pass then scores that attempt 0–100 against the charts and statistics that **actually rendered** — not a prediction of them. The loop feeds the analyst its own prior attempt plus the judge's feedback and repeats until the score clears a threshold or a pass cap is hit, then returns the **best-scoring** pass rather than the last one.

A fixed tool menu instead of generated code means no arbitrary execution, and a chat can span multiple datasets with an explicit `compare` tool across exactly two.

---

### How I work

A few principles these repos were actually built on, not aspirations:

- **Verify, don't assume.** Value inventories, schema shapes, and date boundaries were executed against the live workspace before being written down — and several turned out different from what the documentation implied.
- **Cost is a design constraint.** A vector search endpoint bills continuously with no pause, so the expensive work lives in durable tables and only the disposable part gets torn down. Billing resources are never declared silently in a bundle.
- **Honest failure beats a confident guess.** *"Which patients will no-show next month?"* gets declined, because the data records what happened, not what will.

---

<!-- TODO: contact row — delete what you don't want public.
     [LinkedIn](https://linkedin.com/in/...) · [Email](mailto:...) · [Website](https://...)
-->
