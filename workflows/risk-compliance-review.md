# Workflow: Risk Compliance Review

## Objective

Check whether a subsection's Risk Register and Risk Report comply with its
Risk Management Plan, and produce a concise, professional review report
with evidence-backed findings and practical corrective actions.

## Input

For a given project/section/subsection, three document types:

1. **Risk Management Plan** — defines procedure steps, the shared
   likelihood/impact matrix and score bands, roles, and review frequency.
2. **Risk Register** — the current risk data (Risk ID, cause, consequence,
   likelihood/impact, score, band, treatment, owner, due date, status,
   target residual rating).
3. **Risk Report** — summarises the register for management (band counts,
   priorities, escalations, overdue actions).

If no standalone Risk Report exists, check whether a risk register is
embedded inside the Risk Report document itself and use that embedded
register as the register source instead of looking for a separate file.

All source documents are **read-only** for this workflow. Never edit,
rename, move, or delete any Plan, Register, or Report file.

## Procedure

1. **Read the Risk Management Plan first.** Extract:
   - The procedure steps (what the Register and Report are each required
     to contain or do).
   - The shared likelihood/impact matrix and score-band definitions.
   - Roles, responsibilities, and review frequency.
2. **Read the Risk Register.** Extract every risk record (Risk ID, cause,
   consequence, likelihood, impact, score, band, treatment, owner, due
   date, status, target residual likelihood/impact/score/band).
3. **Read the Risk Report.** If no separate Risk Report file exists, use
   the risk register embedded within the Risk Report document instead.
   Extract the summary, band counts, priorities/escalations, and any
   overdue-action statements.
4. **Verify Register scores deterministically.** For every risk, recompute
   Score = Likelihood x Impact and the Target Score = Target Likelihood x
   Target Impact, and check both against the Plan's band table. Flag any
   risk where the stated score/band does not match the recomputed
   score/band.
5. **Check Register compliance against the Plan's procedure steps** (e.g.
   cause/consequence recorded, treatment/owner/due date/status recorded,
   target residual rating estimated, current rating retained until
   verified). Flag any step not satisfied, citing the specific missing
   field(s).
6. **Check Report compliance against the Plan's procedure steps** (e.g.
   reconciliation with the register, inclusion of open high/critical
   risks and overdue actions, escalation of High/Critical risks for human
   review, decisions recorded before closure). Flag any step not
   satisfied.
7. **Cross-check Report against Register.** Confirm reported band counts,
   priority lists, and overdue-action claims match what is actually in
   the Register. Flag any discrepancy.
8. **Compile findings.** Every finding must cite the specific document,
   section/row, and the exact evidence (e.g. "Risk Register, PRJ-A1-R03:
   stated score 12 vs recomputed 4x3=12 — compliant" or "Risk Report
   Step 3: Plan requires a recorded decision and next review date for
   escalated risks; Register has no such fields for PRJ-A1-R01–R04 —
   gap").
9. **Propose corrective actions** only for genuine discrepancies/gaps —
   practical, specific, and tied to the finding. Do not propose a
   corrective action for a compliant item.
10. **Produce the review report** (see Output). Do not modify, save over,
    or rename any of the source documents.

## Rules

- Read the Plan before the Register, and the Register before the Report —
  the Plan is the compliance baseline; never infer requirements from the
  Register or Report alone.
- If no standalone Risk Report exists, use the risk register embedded in
  the Risk Report document instead of treating the data as missing.
- Never invent missing information; report it as a gap with cited
  evidence.
- Never change a risk rating, status, or any field in the source
  documents as part of this review.
- Distinguish current ratings from target/residual ratings explicitly in
  every finding that touches scoring.
- A finding is only valid if it cites a specific document and
  row/section as evidence — no unsupported claims.

## Output

A concise, professional Risk Compliance Review report containing:

1. **Scope** — Section/Subsection, documents reviewed, snapshot date(s).
2. **Findings table** — columns: `Finding ID | Document(s) | Reference
   (Risk ID / section) | Observation | Evidence | Compliant? (Yes/No) |
   Severity`.
3. **Discrepancies and gaps** — grouped by Register-vs-Plan,
   Report-vs-Plan, and Report-vs-Register, each with cited evidence.
4. **Corrective actions** — only for findings marked non-compliant;
   practical and specific, with a suggested owner where the Plan
   identifies one.
5. **Confirmation** that all source documents remain unmodified
   (read-only) throughout the review.
