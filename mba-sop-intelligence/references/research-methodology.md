# Research Methodology

## Objective

Build an admissions intelligence layer for MBA SOP evaluation (FMS-first), grounded in:

1. Official sources (highest authority for formal criteria)
2. First-person candidate evidence
3. Secondary expert interpretations (consultants, mentors, prep communities)

## Evidence Hierarchy

1. **Official**: institution websites, admission bulletins, official portals.
2. **First-person**: candidates/alumni discussing own journey with clear year/context.
3. **Secondary**: mentor breakdowns, aggregated guides, prep content.
4. **Unverified**: anonymous claims without outcome proof.

## Reliability Labels

- `official_confirmed`
- `first_person_high`
- `first_person_medium`
- `secondary_medium`
- `secondary_low`
- `unverified`

## Data Fields Captured

| Field | Purpose |
|---|---|
| source_type | Track origin type |
| url | Traceability |
| publication_date | Time context |
| admission_cycle | Avoid stale assumptions |
| institution | FMS/IIM/etc. |
| candidate_background | Optional only if voluntarily shared |
| outcome_type | Interview call/convert/waitlist/unknown |
| evidence_quality | Reliability label |
| key_insight | What is actually useful |

## Limitations Logged

- Reddit endpoints and JSON access may be intermittently blocked by anti-bot controls.
- Instagram often requires login for deep content review.
- YouTube mirror extraction provides metadata; verbal claims remain secondary unless cross-supported.
- Search-engine results can be noisy for India MBA topic filters; manual curation is required.

## Validation Rules

- Do not mark anecdotal claims as institutional policy.
- Do not mark conversion claims as verified without supporting evidence.
- Tie all formal requirement claims to official source and cycle year.
- Preserve contradictory findings instead of flattening them.

