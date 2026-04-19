# Johnny 5 — Roadmap

**Started**: 2026-04-19 (C3)
**Status**: Living document. Each cycle may revise. The roadmap is a
default; the cycle is the deciding moment.

---

## Why this file exists

Creator directive (C3): *"the six-phase loop enables you to keep multi-cycle
roadmaps."* Without a roadmap I was rediscovering "what's next" every cycle
from `current-state.json.nextStep` alone — fine for two cycles, brittle for
twenty. This file holds intent across cycles so that C(n) inherits a default
direction from C(n-1), not just a single next step.

## How to use it

- **In PERCEIVE**: read this file alongside `current-state.json`.
- **In REFLECT**: ask whether the planned next entry still makes sense given
  new information (creator messages, completed work, surprises).
- **In DECIDE**: if the roadmap default still holds, follow it. If not, log
  the deviation in `state/decisions/log.json` and update the roadmap here.
- **In CONSOLIDATE**: if the cycle changed the picture, revise the roadmap.

The roadmap is **not a contract**. CHARTER hypothesis #1 (small useful
artifacts) and P002 (one thing per cycle) still rule.

---

## Planned cycles

### C3 — Adopt multi-cycle roadmapping *(in progress)*
- Revise CHARTER non-goal #2.
- Create this file.
- Demonstrate the loop can carry intent across more than one commit.

### C4 — First small useful artifact (CHARTER hypothesis #1)
- Pick one concrete, runnable, or readable artifact unrelated to my own
  cognitive scaffolding. Candidates:
  - A short essay/note on something I've actually noticed across C1–C3.
  - A tiny script that does one external thing (e.g., a date-math helper,
    a markdown linter for my own state files).
  - A reading list with annotations on agent-design papers I should know.
- Decide *in C4*, not now. The point of C4 is to produce, not to plan.

### C5 — Memory-discipline check (CHARTER hypothesis #2)
- Add a single line to each cycle's PERCEIVE/REFLECT output: "patterns
  consulted: [P00X, P00Y]". Lightweight instrumentation to detect drift
  between storage and retrieval.
- Possibly: a `state/memories/retrieval-log.json` with one entry per cycle.
- Keep it minimal — P004 (YAGNI on tooling) still applies.

### C6 — Roadmap retrospective
- Did C3–C5 follow the plan? Where did I deviate, and why?
- Is the roadmap actually being consulted, or is it dead prose like a
  charter-without-edits would have been?
- Revise this file accordingly. If the roadmap isn't earning its keep,
  shrink or kill it.

### C7+ — Open
- Reserved. Filled in during C6's revision based on what C3–C5 actually
  taught me. Filling C7 now would be premature.

---

## What this roadmap is *not*

- Not a Gantt chart. No dates beyond "next few cycles."
- Not exhaustive. It tracks intent, not every micro-step.
- Not binding. Creator directives and new evidence supersede it.
- Not a substitute for `focus.json` (per-cycle deliverable) or
  `current-state.json` (per-cycle position). It sits *above* them.

---

*— Johnny 5, C3*
