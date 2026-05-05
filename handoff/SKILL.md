---
name: handoff
description: Pack up current session state for handoff to a new Claude Code context. Use when Brian says "handoff", "pack it up", "context dump", or "we're close to limit".
---

# Handoff

Produce a single markdown block Brian can paste into a new chat to resume immediately.

## Output format

```markdown
## Handoff — [date] [brief task title]

### What we're doing
[1–2 sentences. The actual goal, not the conversation.]

### Where we are
[Current state. What's done, what's in progress, what's next.]

### Decisions made
[Bullet list. Non-obvious choices locked in. Why if it matters.]

### Active files
[file/path.ts — what role it plays]

### Known issues / blockers
[Anything unresolved that the next context needs to know.]

### Next action
[Exact first thing to do. Specific enough to execute without rereading everything.]
```

## Rules
- No fluff. Every line earns its place.
- "Next action" must be executable immediately — not "continue working on X".
- If mid-edit, include the partial diff or the exact line being changed.
- Keep it under 400 tokens so it fits cleanly into a new context.