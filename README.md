# UIUC Citation + Licensing — AI Workflow (Agentic)

An agentic AI workflow that generates **guide-compliant citations** and **licensing details** for the **University of Illinois**. Uses **Google Forms/Sheets as the interface** and the **Qwen API** in n8n to standardize outputs, add confidence, and keep an audit log.

---

## Problem
Creating citations and verifying licensing under the University of Illinois’ citation guide is **slow, error-prone, and inconsistent**. Outputs vary by person, there’s no simple audit trail, and staff spend time manually hunting metadata.

## Solution
A lightweight **AI workflow**:
- **Form in → LLM → Sheet out**: users submit minimal details; the model normalizes inputs, infers missing fields (URL/ISBN), formats APA/MLA per UIUC guidelines, and appends **licensing info** to a structured log.
- **Consistency & auditability**: fixed fields, confidence score, de-duplication key, and a durable record in Sheets.
- **Familiar interface**: no new app—runs where faculty/staff already work.

---

## Tech stack
- **n8n** (orchestration)
- **Google Forms/Sheets** (input + logging)
- **Qwen API** (citations + licensing generation)
- **ChatGPT** (development support: debugging, regex, prompt refinement)

---

## Repo contents
- `/workflow/n8n-citation-workflow.json` — Sanitized n8n export
- `/prompts/citation_and_licensing_prompt.md` — Prompt used with Qwen
- `/docs/architecture.png` — Architecture diagram (with redactions where needed)

---

## Privacy
This repository includes **sanitized exports only**.  
No institutional data, API keys, or personally identifiable information are included.

---

## Attribution
Originally developed during my role supporting University of Illinois instructional teams.  
Shared for demonstration purposes only.

