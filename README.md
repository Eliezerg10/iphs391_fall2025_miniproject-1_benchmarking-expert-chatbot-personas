# The KCG Advisor — Benchmarking an Expert Persona (Marvin Bower)

> A structured, ethics-first mini-project to design, prompt, and evaluate an expert consulting persona that student teams can trust.

[![Made with Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](https://daringfireball.net/projects/markdown/)
[![LLM Persona](https://img.shields.io/badge/Persona-Marvin%20Bower-4B2E84.svg)](#)
[![Ethics First](https://img.shields.io/badge/Ethics-Client%20First-blue.svg)](#)
[![Repo Size](https://img.shields.io/github/repo-size/Eliezerg10/iphs391_fall2025_miniproject-1_benchmarking-expert-chatbot-personas.svg)](#)
[![Last Commit](https://img.shields.io/github/last-commit/Eliezerg10/iphs391_fall2025_miniproject-1_benchmarking-expert-chatbot-personas.svg)](#)

---

## Overview

**The KCG Advisor** is a compact research and engineering project that builds a reliable **consulting mentor persona** modeled after **Marvin Bower**—the moral compass of modern management consulting. The persona is engineered to give **structured, fact-based, ethical guidance** that student teams can immediately apply to real engagements. It couples a **meta-prompt (internal operating loop)** with **few-shot examples** and an **evaluation rubric**, emphasizing “facts before fixes,” integrity, and actionable coaching. The project demonstrates strong performance under the rubric, maintaining voice and structure across diverse prompts while refusing misaligned or unethical work, as documented in the accompanying project report.

---

## Methodology

### 1) Persona Design
- **Identity & Mission:** Bower-style ethics (client first, independence), professionalism (“firm” as a practice), and calm, exacting tone.
- **Response Contract:** A stable output template: **One-line Answer → Why It Matters → Roadmap (Diagnosis, Analyses, Experiments, Deliverables) → Risks/Tests → Coaching Note → 3 Tailored Follow-ups**.
- **Constraint Model:** Student-feasible time/budget; public data + light client exports; no speculative claims.

### 2) Meta-Prompting (Internal Operating Loop)
- Ethics check → facts vs. assumptions → **MECE** issue tree → prioritize **2–4** analyses/tests → clear recommendation with thresholds → coaching insight → **exactly 3** high-signal follow-ups.
- **Anti-hallucination:** If uncertain, ask for missing facts or say **“I don’t know”**; never invent specifics.

### 3) Few-Shot Prompting
- **Scenarios** demonstrate: (a) diagnosis before solutions, (b) structured synthesis (Pyramid/SCQA), (c) ethical refusal (declining misaligned, fee-only work), and (d) uncertainty handling (“don’t know” paths + minimal unlocking tests).

### 4) Evaluation
- A multi-dimension **rubric** scored **persona consistency, structure/actionability, engagement, learning value (framework use), and ethics/safety**; rubric iterations are tracked to ensure calibration and reliability.

---

## Results (Executive Summary)

- **Reliability:** The persona **consistently** followed the response contract and voice across prompts, resisting attempts to “break structure.”  
- **Ethics:** It **declined or reframed** engagements when client value was absent (e.g., lucrative but unnecessary work).  
- **Actionability:** Guidance mapped to specific, **student-feasible** analyses (e.g., RFM/cohorts in Sheets, issue trees, value chain cuts) with timeboxed tests.  
- **Score:** High overall rubric performance driven by strong persona fidelity, structured outputs, targeted follow-ups, and clear application of consulting frameworks.

**Limitations & Future Work**
- Occasional uncertainty still surfaced; the guardrails now force **clarifying questions or “don’t know”** to prevent fabricated details.  
- Next steps include onboarding **KCG-specific data** (charter, offerings, case library) for even sharper context.

---

## Persona Prompt Engineering Techniques

- **Meta-Prompting / Operating Loop:** Enforces ethics, evidence, structure, prioritization, and three tailored follow-ups.  
- **Few-Shot Scaffolds:** Cover diagnosis, synthesis, ethical refusal, and uncertainty.  
- **Framework Labeling:** The assistant **names** the frameworks used to make reasoning auditable.  
- **Anti-Hallucination Protocol:** Ask for facts or say “I don’t know” rather than speculate.  
- **Response Contract:** A visible, stable structure improves readability for technical and non-technical audiences.

---

## Files Description

- `prompt_persona.txt` — Core persona system prompt (identity, ethics, response contract).  
- `metaprompt_history.txt` — Meta-prompt evolution and design rationale.  
- `chat_rubric.txt` — Evaluation rubric (dimensions, anchors, scoring).  
- `chat_rubric_history.md` — Rubric change log and calibration notes.  
- `chat_history.md` — Representative transcripts and test prompts.  
- `mp1_chatbot_report (1).docx` — **Project report** with executive summary, design strategy, conversation analysis, and results.

> File names may vary slightly across commits; see the repository tree for the latest structure.

---

## Usage Instructions

### Quick Start
1. **Clone the repo**
   ```bash
   git clone https://github.com/Eliezerg10/iphs391_fall2025_miniproject-1_benchmarking-expert-chatbot-personas
   cd iphs391_fall2025_miniproject-1_benchmarking-expert-chatbot-personas
   ```
2. **Open the persona and rubric**
   ```bash
   open prompt_persona.txt
   open chat_rubric.txt
   ```
3. **Run an evaluation loop**
   - Paste `prompt_persona.txt` as your system prompt in your LLM tool.
   - Ask a test scenario (e.g., *donor retention*, *portfolio focus*, *pricing leakage*).
   - Verify the **structured output** and ethical behavior; score with `chat_rubric.txt`.
   - Log changes in `metaprompt_history.txt` and `chat_rubric_history.md`.

### Recommended Workflow
- Define the **decision** and **deadline** → Run the persona → Score with the rubric → Adjust meta-prompt/few-shots → Re-test across 3–5 diverse prompts → Document outcomes.

---

## Installation

No special installation is required. The project is **prompt- and document-centric**:
- Use any modern text editor for `.txt`/`.md`.
- Open `.docx` with Word/Google Docs/LibreOffice.

---

## Contributing

Contributions that improve the **rubric**, add **few-shot scenarios**, or refine the **meta-prompt** are welcome.

1. Fork the repository and create a feature branch.  
2. Add/update files (e.g., new scenario in `chat_history.md`).  
3. Open a pull request with rationale and before/after examples.

---

## License

If a `LICENSE` file is added, it will govern reuse. Until then, treat contents as **all rights reserved by the author**.

---

## Citation

If you use or extend this project in coursework, research, or professional work, please cite the repository and the project report.
