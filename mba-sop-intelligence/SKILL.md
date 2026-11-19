---
name: mba-sop-intelligence
description: >
  Use this skill when a user asks to build, rewrite, stress-test, or evaluate an MBA SOP
  with admissions-grade rigor, especially for FMS Delhi and similar Indian top MBA schools.
  This skill builds a candidate intelligence profile first, then drafts and evaluates SOPs
  through a ten-reviewer board with explicit disagreement and risk flags.
  Trigger phrases: "review my FMS SOP", "rewrite SOP for FMS Delhi", "evaluate my MBA SOP",
  "SOP for GEF candidate", "simulate admissions panel on SOP", "why MBA why FMS SOP".
user-invocable: true
---

# MBA SOP Intelligence & Review Board

Evidence-informed SOP construction and evaluation for FMS-first MBA applications.

---

## Use When

- User provides SOP text, resume text, personal statement, or `.docx` for MBA applications.
- User wants FMS-focused SOP strategy, not generic essay rewriting.
- User wants admissions-style stress testing with multiple reviewer perspectives.

---

## Dependencies and Verification

- Required: applicant content (text or `.docx`) and target school list.
- Required: latest official cycle requirements from official portals.
- Verify before writing:
  1. Admission cycle/year is explicitly tagged in all formal claims.
  2. Source reliability is labeled for every non-official claim.
  3. No fabricated profile detail is introduced.

---

## Progressive Loading

- Load [`./references/research-methodology.md`](./references/research-methodology.md) in **Step 1**.
- Load [`./references/fms-admissions-intelligence.md`](./references/fms-admissions-intelligence.md) in **Step 2**.
- Load [`./references/research-source-database.md`](./references/research-source-database.md) in **Step 2**.
- Load [`./references/gef-positioning-framework.md`](./references/gef-positioning-framework.md) in **Step 4** when profile resembles GEF competition pool.
- Load [`./references/sop-evaluation-rubric.md`](./references/sop-evaluation-rubric.md) in **Step 6**.
- Load [`./references/reviewer-personas.md`](./references/reviewer-personas.md) in **Step 7**.
- Load [`./references/authenticity-and-ethics.md`](./references/authenticity-and-ethics.md) in **Steps 5 and 8**.
- Load [`./references/writing-style-guide.md`](./references/writing-style-guide.md) in **Step 5**.

---

## Workflow

### Step 1: Intake and input normalization

Collect:
- Target institutions (default: FMS Delhi + IIM A/B/C/L/K/I + SPJIMR + MDI + XLRI).
- Admission cycle (required).
- Candidate input document(s).

If `.docx` parsing is unavailable in runtime, request pasted text sections and continue.

### Step 2: Build Candidate Intelligence Profile (before any rewrite)

Use `templates/candidate-profile-template.md`.

Extract and classify:
- Verified facts from user document.
- User-stated but unverified claims.
- Missing critical fields.
- Contradictions.

Never invent achievements, titles, metrics, or motivations.

### Step 3: Missing-information query

Ask only targeted follow-ups required to avoid guessing:
- Career goals, role transitions, business impact metrics, leadership evidence.
- Why MBA now.
- Why FMS specifically.

### Step 4: Positioning strategy

Map profile to:
- Differentiators that are evidence-backed.
- Risk factors likely to trigger interview skepticism.
- GEF-specific positioning opportunities (if relevant), without stereotyping.

### Step 5: SOP drafting

Draft institution-specific SOP that:
- Has a concrete opening.
- Connects past -> present -> future coherently.
- Justifies Why MBA and Why this school.
- Uses only defensible claims.
- Sounds personal, not generic.

### Step 6: Original draft diagnostic + rubric scoring

If original SOP exists:
- Score original on the 100-point rubric.
- Keep what is strong.
- Mark weak sections and factual risks.

### Step 7: Ten independent board reviews (blind pass)

Run ten reviewer personas independently.
Hard rule: each reviewer must not see other reviewer outputs before submitting.

Each reviewer must return:
1. Score /100
2. Top 3 strengths
3. Top 3 weaknesses
4. Rejection triggers
5. Unsupported/exaggerated statements
6. Concrete revisions
7. Verdict: Exceptional | Strong | Competitive | Average | Weak | Not ready for submission

### Step 8: Moderated disagreement round

After blind outputs:
- Let reviewers challenge each other.
- Preserve disagreement; do not force consensus.
- Allow score changes with rationale.

### Step 9: Chairperson synthesis

Produce board report with:
- Mean score, median score, high, low
- Agreement clusters
- Disagreement clusters
- Writing issues vs profile issues
- Rejection risk summary
- Final recommendation

### Step 10: Official-cycle compliance check

Live-check latest official requirements (cycle-specific), then label:
- Confirmed requirement
- Not found on official source
- Conflicting claims across unofficial sources

### Step 11: Mandatory deliverables

Return all 7 outputs:
1. Candidate Intelligence Report
2. Original SOP Diagnostic
3. Rewritten SOP
4. Ten-Reviewer Assessment
5. Admissions Board Report
6. Revision Roadmap (Critical/High/Medium/Optional)
7. 25-40 Interview Defense Questions

---

## Error Handling and Quality Loop

- Missing required profile data -> ask targeted questions, do not draft final SOP yet.
- Unknown official requirement -> label as unknown, provide source-check timestamp.
- Any fabricated detail detected -> remove and re-run affected sections.
- If reviewer outputs converge unrealistically -> rerun with persona-specific prompts.

---

## Gotchas

- Official process details change yearly; never reuse historical limits without cycle tag.
- High writing polish is not high authenticity by default.
- FMS conversion stories are anecdotal unless independently supported.
- Reddit/Instagram access may be restricted by platform security; log limitations explicitly.

---

## Output Quality Checklist

- [ ] Every formal claim has admission year/cycle tag
- [ ] Every non-official claim has reliability label
- [ ] Candidate facts are source-grounded, no invention
- [ ] Ten reviews are distinct and independently reasoned
- [ ] Board report separates narrative quality from profile quality
- [ ] Interview question bank challenges weak and risky claims

