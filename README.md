# ResumeSync AI ⚡

> **Instant ATS Keyword Matcher, Dynamic Project Rephraser & Real-Time Overleaf LaTeX Sync**

Live Web App: **[https://resume-sync-jade.vercel.app](https://resume-sync-jade.vercel.app)**

---

## Overview

**ResumeSync AI** is a client-side ATS optimization engine and LaTeX synchronizer. It allows software engineers and data scientists to paste or upload any Job Description (.pdf, .docx, .txt) and instantly tailor their resume—dynamically aligning technical skills and reframing project bullet points while strictly preserving factual truth anchors and adhering to a 1-page LaTeX layout budget.

With 1-click synchronization, tailored LaTeX code is instantly injected into **Overleaf** (via CodeMirror 6 transactional state dispatch) and automatically recompiled.

---

## Key Features

1. **Instant Client-Side ATS Optimization (0 ms Latency)**:
   - Pure client-side JavaScript execution with zero external AI API keys or quota dependencies.
   - Real-time ATS match scoring, missing keyword detection, and instant highlight badges.

2. **Dynamic Project Rephraser & Ordering Engine (`optimizeProjectsForJD`)**:
   - Analyzes target domain (Healthcare/Bioinformatics, Fintech/Quant, Data Engineering, Machine Learning & AI, Analytics).
   - Dynamically reorders portfolio projects to put the most relevant experience first.
   - Intelligently weaves in specific JD terminology (e.g. *data harmonization*, *missing-value imputation*, *anomaly detection*, *agile workflows*, *technical documentation*, *time-series forecasting*).

3. **Strict Truth Anchors & 1-Page Budget**:
   - Zero hallucination: All core metrics ($R^2 = 0.88$, 17,000+ records, Stockfish 16 NNUE WASM, IEEE CVMI-2023, GPA 3.85 / 8.93) remain 100% verified.
   - Bullet lengths calibrated strictly between 25 and 30 words to guarantee a clean 1-page output in Overleaf.

4. **CodeMirror 6 Overleaf Integration**:
   - Integrates with the [JobFill Chrome Extension](https://github.com/Shivamshuroy448/jobfill-extension) via `MAIN` world script injection.
   - Dispatches atomic `view.dispatch` transactions into Overleaf's CodeMirror 6 editor and triggers automatic PDF recompilation.
   - Fail-safe fallback: automatically copies the tailored LaTeX to the system clipboard for immediate `Cmd+A` / `Cmd+V` paste.

5. **Universal JD File Ingestion**:
   - Client-side drag-and-drop parser for PDF (via PDF.js) and Word DOCX (via Mammoth.js).

---

## Tech Stack

- **Frontend**: Vanilla JavaScript (ES6+), HTML5, Modern CSS3 with CSS Grid & Flexbox
- **Document Parsers**: PDF.js, Mammoth.js
- **LaTeX Template**: `resume.cls`, `roy.tex`
- **Editor Bridge**: CodeMirror 6 transactional state engine
- **Hosting**: Vercel Serverless CDN
