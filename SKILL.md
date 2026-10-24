---
name: brain-hygiene
description: >-
  Audits Second Brain memories for duplicates, obsolete drafts, and fragmented notes
  under a specific topic or project, and provides a structured consolidation and cleanup plan.
---

# Brain Hygiene — Knowledge Base Deduplicator & Cleaner (`/brain-hygiene`)

Use this skill to keep your Second Brain lean, fast, and high-signal by finding duplicate memories, outdated drafts, and fragmented notes that should be merged or deprecated.

---

## What Happens When Invoked

When `/brain-hygiene` is triggered, execute these steps:

### Step 1: Query Memories for the Domain
1. Identify target topic or project from the user command (e.g. `Live Actions`, `audio`, `design`).
2. Fetch relevant memories via `recall` with high topK (`topK: 20`) and inspect `list_recent`.

### Step 2: Detect Hygiene Issues
Analyze the retrieved memories across three categories:
1. **Duplicates & Near-Duplicates**: Two or more memories describing virtually the same decision or setup detail.
2. **Obsolete or Contradictory Information**: Older memories whose facts were superseded by later entries but never marked deprecated.
3. **Draft / Untagged Clutter**: Memories marked `draft` or missing standard project tags.

### Step 3: Formulate Cleanup Plan
Generate an actionable cleanup plan:
- 📦 **Merge Proposals**: Which duplicate entries to consolidate into a single authoritative entry (via `update` on the primary entry).
- 🚫 **Deprecation Proposals**: Obsolete entries to flag as `deprecated` via `set_status` (preserves them for audit history while removing them from default recall).
- ⭐ **Canonical Promotions**: Foundational, settled architectural choices to promote to `canonical` status.

### Step 4: Batch Execution
Present the plan with ready-to-run commands:
```
/brain status mem_old123 deprecated
/brain status mem_primary456 canonical
```
If the user confirms, execute the status updates or merges immediately.

---

## Syntax

```
/brain-hygiene <topic or tag>
```

## Examples

```
/brain-hygiene Live Actions
/brain-hygiene audio
/brain-hygiene preferences
```
