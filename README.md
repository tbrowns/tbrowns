<div align="center">

<img src="./terminal.svg" width="760" alt="tom@obande — stack and current projects">

</div>

I'm a developer in Nairobi building full-stack products with an applied-AI core. The thing I care about most is keeping the model on a short leash: deterministic code should decide, and the LLM should explain.

## Selected work

### [ShambaLens AI](https://github.com/tbrowns/shambalens-ai) — evidence-first crop triage

<img src="./stack/shambalens.svg" alt="FastAPI, Next.js, TypeScript, Postgres, Firebase, vision and LLM">

Most crop classifiers hand you one confident label and hide the uncertainty. ShambaLens does the opposite. It gates the photo on quality first, records only what's visibly there, then ranks up to three competing causes and asks the farmer up to three questions *chosen for their ability to separate the leaders*. The ranking is revised from those answers, an independent pass verifies evidence and calibration, and deterministic guardrails strip unsafe chemical instructions even when the model generates them.

19 tests, CI running against a live Postgres service.

### [Mindbase](https://github.com/tbrowns/mind-base) — cited answers over an internal knowledge base

<img src="./stack/mindbase.svg" alt="Next.js, TypeScript, Firestore, Pinecone, Groq">

Ingests internal documents, meeting transcripts and a Gmail inbox; masks obvious personal data before anything is stored; chunks and indexes to Pinecone. Retrieved chunks are filtered for relevance *before* they reach the model, so answers stay grounded and every claim carries a source. Missing credentials fail loudly instead of silently degrading to a worse provider.

**[Live →](https://mind-base-nine.vercel.app)**

### [DRIP Orchestrator](https://github.com/tbrowns/drip_orch_platform) — dividend reinvestment for the NSE

<img src="./stack/drip.svg" alt="FastAPI, Python, SQLAlchemy, Postgres">

Nairobi Securities Exchange data isn't available in the tools that model dividend reinvestment, so I built the missing piece: live quote scraping, dividend history tracking, and simulation of what reinvested dividends actually compound into over time.

<details>
<summary><b>More projects</b> — an AI financial controller, sign language recognition, a study assistant, and others</summary>

<br>

### [Finly](https://github.com/tbrowns/finly_platform) — AI financial controller for founders

<img src="./stack/finly.svg" alt="FastAPI, Python, Neon Postgres, Zoho OAuth2, Groq">

Pulls monthly books from Zoho, normalises them into Postgres, then runs four *deterministic* checks — cash-flow risk, fraud indicators, personal/business account mixing, reconciliation. The model only writes the explanation; it never decides whether something is wrong. That split is the whole design.

### [Gesture World](https://github.com/tbrowns/gesture-world) — sign language recognition and speech synthesis

<img src="./stack/gesture.svg" alt="Python, MediaPipe, OpenCV, scikit-learn">

Detects sign language gestures from a webcam using MediaPipe hand landmarks, classifies them with scikit-learn, and synthesises speech from the recognised text through Azure Cognitive Services.

### [Moscore](https://github.com/tbrowns/moscore-web-app) — NotebookLM-style study assistant

<img src="./stack/moscore.svg" alt="Next.js, TypeScript, Supabase, Firebase, RAG">

Students upload their own course material into notebooks and ask questions against it. Documents are chunked, embedded and retrieved so answers stay tied to what the student actually uploaded.

### Also on this account

| | |
|---|---|
| [invoice_pdf_extractor](https://github.com/tbrowns/invoice_pdf_extractor) · [backend](https://github.com/tbrowns/invoice_pdf_extractor_backend) | Structured field extraction from invoices and receipts |
| [tafsiri](https://github.com/tbrowns/tafsiri) | Translation tooling |
| [vendor-connect](https://github.com/tbrowns/e-commerce) | Vendor-side ecommerce platform |
| [wines-spirits](https://github.com/tbrowns/wines-spirits) | Stock and purchase tracking · [live](https://winesapp.netlify.app/) |
| [chat-app-sockets](https://github.com/tbrowns/chat-app-sockets) | Realtime chat over WebSockets |
| [pawa-weather-app](https://github.com/tbrowns/pawa-weather-app) | Weather client |

</details>

## How I build

The through-line above is keeping the model on a short leash. Finly decides with deterministic code and lets the LLM narrate. ShambaLens makes uncertainty visible instead of collapsing it into one label, and runs a separate verification pass before a farmer sees anything. Mindbase filters retrieved context before generation rather than hoping the model ignores the noise.

I'd rather ship something narrow that holds up than something broad that demos well.

## Stack

| | |
|---|---|
| **Backend** | <img src="./stack/cat-backend.svg" alt="Python, FastAPI, SQLAlchemy, Node.js, Express"> |
| **Frontend** | <img src="./stack/cat-frontend.svg" alt="TypeScript, Next.js, React, Tailwind, shadcn/ui"> |
| **Data** | <img src="./stack/cat-data.svg" alt="PostgreSQL, Neon, Supabase, Firestore, Pinecone"> |
| **AI** | <img src="./stack/cat-ai.svg" alt="RAG pipelines, embeddings, vector search, Groq, Gemini, vision models"> |
| **Infra** | Docker · GitHub Actions · Vercel · nginx |

## Elsewhere

[Portfolio](https://obande.netlify.app/) · [LinkedIn](https://www.linkedin.com/in/tom-obande-13811a1a8) · [tb.obande@gmail.com](mailto:tb.obande@gmail.com)
