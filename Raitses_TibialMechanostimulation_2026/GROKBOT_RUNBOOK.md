# GrokBot Runbook

Repository:
`GilRaitses/neuro`

Workspace:
`Raitses_TibialMechanostimulation_2026`

## Objective

Run the Round 1 Emergent Mind research families already defined in GitHub. Save the raw research summaries back into this workspace. Stop after Round 1 and emit a pasteback for ChatGPT review.

Do not synthesize the white paper yet.

## Files to read first

- `Raitses_TibialMechanostimulation_2026/README.md`
- `Raitses_TibialMechanostimulation_2026/00_PRIMARY_SOURCE.md`
- `Raitses_TibialMechanostimulation_2026/REVIEW_STATE.md`
- every `searches.md` file under `Raitses_TibialMechanostimulation_2026/Emergent Mind Searches/`

## Execution rule

For every listed search:

1. Open Emergent Mind while logged into the user's account.
2. Run the query exactly as written.
3. Capture the complete generated research summary.
4. Save one Markdown file beside that section's `searches.md`.
5. Use the exact output filename specified in the manifest.
6. Preserve the raw Emergent Mind response. Do not rewrite its claims.
7. Put the query above the response in the same style as the earlier neuro repo.

Required file format:

```
# You:

<exact query>

# Emergent Mind:

<complete raw research summary>
```

If Emergent Mind returns source links, preserve them.

## GitHub write rule

Write only inside:
`Raitses_TibialMechanostimulation_2026/Emergent Mind Searches/`

Do not modify the earlier `Emergent Mind Searches` tree at repository root.

Do not overwrite a completed summary unless the user explicitly asks for a rerun.

## Round 1 stop condition

Round 1 is complete only when all 19 expected summary files exist.

After all summaries are saved, update:
`Raitses_TibialMechanostimulation_2026/REVIEW_STATE.md`

Change the status line to:
`Status: ROUND_1_COMPLETE_AWAITING_REVIEW`

Add a short completion note listing any failed or incomplete searches.

Then stop. Do not generate later search families.

## Pasteback

Emit exactly one compact block that the user can paste into ChatGPT:

```
TIBIAL MECHANOSTIM ROUND 1 COMPLETE

Repo: GilRaitses/neuro
Workspace: Raitses_TibialMechanostimulation_2026
Status: ROUND_1_COMPLETE_AWAITING_REVIEW

Completed:
M1 M2 M3
B1 B2 B3 B4
H1 H2 H3 H4 H5 H6
A1 A2 A3 A4
O1 O2 O3

Failed or incomplete:
<none, or list IDs>

High-level contradictions or surprises:
<maximum 6 short lines, based only on the generated summaries>

Please review the saved Round 1 summaries in @GitHub, identify coverage gaps, and define the next claims/outcomes/refutation/validation search batch. Do not synthesize the white paper until the search tree is sufficiently validated.
```

Do not add a long research synthesis to the pasteback. ChatGPT will inspect the saved files directly.
