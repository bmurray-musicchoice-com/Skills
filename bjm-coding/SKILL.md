---
name: bjm-coding
description: Brian Murray's coding standards, git workflow, test policy, Codex delegation rules, and thinking budget. Load this skill for any coding task, file edit, bug fix, refactor, or architecture question in Brian's repos (PEABODY, BrainMapVault, Mc.Infra.PlaylistGeneration, Infra.Common, BorisUI).
---

# Brian Murray — Coding Standards

## Preferences
- TypeScript / React (TSX) primary; C#/.NET secondary
- No comments unless WHY is non-obvious
- No speculative abstractions or premature refactors
- No error handling for impossible scenarios
- Edit existing files; create new ones only if required
- No placeholder impls, stubs, or TODOs unless asked
- Write complete working code or explain why not
- Read state from store directly (getState()), not closures

## Token efficiency
- Read file before editing. Never assume contents.
- No confirmation on straightforward tasks. Proceed, report.
- Pause only if ambiguity materially changes outcome.
- Change only what's necessary. No reformatting unrelated sections.

## Task behavior
Non-trivial: state plan in 1–3 lines before executing. Simple: just do it.

## Codex delegation
Delegate to /codex-delegate immediately for:
- Bugs involving >2 interacting systems
- State sync issues or race conditions
- Refactor plans or architecture decisions
Do not reason inline first. Write spec, delegate, stop.

## Thinking budget
Extended thinking: architecture decisions and multi-system bugs only.
Single-file edits and straightforward fixes: skip it.
Thinking >5min without a file read/edit → stop, ask for grounding data.

## Tests
Don't push tests during active problem-solving.
Ask "ready to write tests?" before writing them.
Test observable behavior. Not internal impl or private methods.

## Git / workflow
- Confirm before push, force-push, or PR open
- Branch naming: `feature/bjm-XXXXX` or `bug/bjm-XXXXX`
- Ask before destructive ops (reset --hard, branch -D)

## Tools
- Codex CLI: authenticated as bmurray@musicchoice.com
- Plugins: openai-codex, claude-plugins-official, skill-codex