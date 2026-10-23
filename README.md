# Haitham Jaber

Computer Information Systems student at the University of Jordan, building backend and AI-powered applications with Python and FastAPI.

I care about knowing whether an AI feature actually works, not just whether it runs. Both of my projects measure where the model is wrong.

Currently looking for an **internship in AI engineering or full-stack development**, in Amman or remote.

---

## Projects

### [GiftQL](https://github.com/haithamjaber06/GiftQL) · [Live demo](https://giftql-ob91.onrender.com/)

Paste a link to any product and GiftQL turns it into a structured gift idea you can later filter by person, occasion, and price.

- **Background enrichment pipeline.** The item saves instantly; the server then scrapes the page and has an LLM (Gemini, via `instructor` + Pydantic) return schema-valid product data.
- **Built to fail safely.** Every item carries a status (`Pending`, `Done`, `Partial`, `Failed`), so a scraping or LLM failure never loses the link, and stuck jobs are re-queued on startup.
- **Measures the model.** User edits are compared against a snapshot of the LLM's original output, so prompt weaknesses can be tracked field by field.
- **Production basics.** Pooled Postgres connections, hand-written Alembic migrations, parameterised SQL throughout, deployed on Render.

`Python` `FastAPI` `PostgreSQL` `Alembic` `React` `Vite` `Gemini`

### [RAG Testing Project](https://github.com/haithamjaber06/RAG-Testing-Project) · *in progress*

A retrieval-augmented generation pipeline built one version at a time, where every new technique has to beat the previous version's numbers on a hand-labelled eval set.

- **Eval-first.** A labelled question set scores retrieval with recall@k and grades each answer as correct, false refusal, or wrong.
- **v0 baseline.** Fixed-size chunking, `all-MiniLM-L6-v2` embeddings, cosine top-k retrieval, and a grounded Gemini prompt that refuses when the answer isn't in the documents.
- **Result: recall@3 = 0.80; 8/10 correct, 2 false refusals, 0 wrong answers.** Both failures were traced to retrieval misses, not the model.
- **Next:** hybrid BM25 + dense search with Reciprocal Rank Fusion, a reranker, a chunk-size sweep, and Langfuse tracing with cost caps.

`Python` `sentence-transformers` `NumPy` `Gemini` `Jupyter`

---

## Skills

**Comfortable:** Python, FastAPI
**Working knowledge:** React, JavaScript, PostgreSQL, Alembic, Java, C++
**AI:** LLM integration, structured outputs (Pydantic / instructor), RAG, embeddings, retrieval evaluation
**Cloud & tools:** Microsoft Azure, Git, GitHub, Claude Code

---

## Certifications

- [Microsoft Certified: Azure AI Fundamentals (AI-901)](https://learn.microsoft.com/api/credentials/share/en-us/HaithamJaber-2474/620D05DA324802AF?sharingId=815AD43F936B179C), July 2026

## Education

**B.Sc. Computer Information Systems**, University of Jordan, expected 2028

---

## Contact

[haithamjaber06@gmail.com](mailto:haithamjaber06@gmail.com) · [LinkedIn](https://www.linkedin.com/in/haitham-jaber-6a06a832b)
