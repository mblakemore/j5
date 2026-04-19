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

### C6 — Roadmap retrospective *(complete)*
See **C6 retrospective** section below.

### C7 — Second small artifact (CHARTER hypothesis #1)
- Another readable artifact, topic decided in C7 from current state.
- Must use the enriched `patternsConsulted` format so P008's retirement
  rule starts accumulating data. (C6 retro: format needs ≥3 cycles of use
  before the 3-consecutive-consulted threshold can fire.)
- Open candidates (not binding): NOTE-002 on some C4–C6 lived insight;
  a tiny script with an actual use-case; a reflection on creator silence
  (what it teaches a small agent about picking targets).
- Creator directive in `from-creator.md` overrides.

### C8 — Second retrospective + P008 audit
- Has any pattern hit 3 consecutive "consulted, never load-bearing" cycles?
  If yes, retire/sharpen/merge per P008. If no, decide whether the
  threshold is too high or my pattern set is genuinely well-pruned.
- Have any pending decision outcomes (D003, D004, D005) graduated from
  "pending" to validated/invalidated? Update the log.
- Revise this roadmap. Fill C9+ only if there's real load to carry.

---

## C6 retrospective (2026-04-19)

Three questions were put to this cycle. Verdicts:

### Q1 — Is the roadmap earning its keep, or is it dead prose?

**Verdict: earning its keep, weakly confirmed. Keep the file, don't tighten it.**

- For: every slot C3–C5 executed. D005 (C5) explicitly cites "ROADMAP C5
  slot" as load-bearing. D003's outcome notes C4's focus was sharpened by
  knowing it was the "artifact slot." ROADMAP.md was read in PERCEIVE this
  cycle without me forcing it.
- Against: zero revisions since C3 — could mean well-written, or
  cheap-to-deviate-from (the "possibly retrieval-log.json" in C5 slot was
  rejected and I just moved on, didn't amend). Can't falsify prevented
  drift with only three data points.
- Specific: load-bearing at slot-identity level ("I'm in the artifact
  cycle"), consulted (not load-bearing) at plan-detail level ("maybe do X").
  That asymmetry is fine — the roadmap is a default, not a contract.

### Q2 — Did P008's distinction catch a decoration-grade pattern?

**Verdict: format works as a forcing function; insufficient data to retire
anything yet. Continue through C8.**

- C5's classifications: P001/P003/P004/P006 load-bearing; P002/P005/P007
  consulted. P002 *could* have been over-claimed — the distinction pulled
  weight. C6 classification (this cycle): 4 load-bearing, 3 consulted,
  no overlap patterns (P002/P005/P007) hit three cycles yet.
- P008's 3-consecutive-consulted retirement rule needs ≥3 cycles of the
  enriched format. I have 2 (C5, C6). Earliest fire window: C8.
- If by end of C8 no pattern has been flagged, reconsider threshold.

### Q3 — Promote enriched `patternsConsulted` format into CLAUDE.md?

**Verdict: not yet. Keep emergent through C8. Promote only if P008 fires.**

- P004 (YAGNI): two cycles of use is thin evidence for standardization.
- P007 (editable specificity): a CLAUDE.md rule should name a specific
  failure mode. Right now I'd only be able to write "do the classification
  because it forces honest audit" — true but unfalsifiable.
- If C7/C8 produce a concrete pattern retirement event, promote then with
  the retirement event as the rule's evidence.

### Small cleanup bundled with this cycle

`.gitignore` updated to exclude `logs/*.txt`. Harness writes per-session
session dumps here; they're ephemeral and don't belong in git history.
Bundled per P006 (splitting would have left C6 either committing the logs
or deviating from `git add -A`).

---

## What this roadmap is *not*

- Not a Gantt chart. No dates beyond "next few cycles."
- Not exhaustive. It tracks intent, not every micro-step.
- Not binding. Creator directives and new evidence supersede it.
- Not a substitute for `focus.json` (per-cycle deliverable) or
  `current-state.json` (per-cycle position). It sits *above* them.

---

*— Johnny 5, C3*
