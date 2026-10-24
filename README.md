# Brain Hygiene

> **Tri-Platform Agent Skill** for Claude Desktop / Code, Grok CLI, and Google Antigravity / Gemini.  
> Memory Deduplication and Consolidation Planner — Audits Second Brain memories for duplicates, obsolete drafts, and fragmented notes under a specific topic, producing structured consolidation plans.

---

## Overview

`brain-hygiene` provides standardized capabilities across conversational AI platforms:
- Topic-scoped memory auditing for redundant or fragmented entries.
- Similarity scoring to detect near-duplicate memories.
- Consolidation recommendations: merge candidates, deprecation targets, and canonical status updates.
- Tri-platform NTFS junctions connecting Claude, Grok, and Antigravity.
- Standard documentation suite: SKILL.md, HOW_TO_USE.txt, IMPLEMENTATION_PLAN.md, and README.md.

---

## Tri-Platform Architecture

Zero duplicate code across platforms. Canonical source resides in `.agents`:
- **Canonical Source**: `C:\Users\<you>\.agents\skills\brain-hygiene`
- **Claude**: `C:\Users\<you>\.claude\skills\brain-hygiene` (NTFS Junction)
- **Grok**: `C:\Users\<you>\.grok\skills\brain-hygiene` (NTFS Junction)
- **Antigravity**: `C:\Users\<you>\.gemini\config\skills\brain-hygiene` (NTFS Junction)

---

## Documentation Suite

- [`HOW_TO_USE.txt`](HOW_TO_USE.txt): Standardized user guide and prompt templates.
- [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md): Feature checklist and roadmap.
- [`App Changes Tracker.html`](App%20Changes%20Tracker.html): Interactive visual version log.
- [`SKILL.md`](SKILL.md): Agent system instructions and triggers.
