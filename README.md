# Airbus ISO/IEC 27001:2022 — Public-Source GRC Review

A public-source Governance, Risk & Compliance (GRC) review of **Airbus SE**, mapping 15 selected ISO/IEC 27001:2022 Annex A control topics to official corporate disclosures — and clearly separating *what Airbus publicly states* from *what an auditor would need to verify*.

**This is a portfolio exercise, not an audit.** It demonstrates the analyst workflow: source collection → evidence mapping → gap identification → evidence request definition → validation roadmap. It does **not** claim Airbus has control gaps.

---

## Why this project exists

Most GRC portfolio projects use a **fictional company**. That makes control mapping easy — you invent the evidence. It proves almost nothing, because real GRC work is messy: sources are incomplete, scopes are ambiguous, and public statements rarely equal operational proof.

This project uses a **real company with real public disclosures**. The challenge is not "map a control to a document" — it's:

- Deciding what a public statement *actually* proves
- Recording where the public record is silent instead of guessing
- Defining what an authorized auditor would request from control owners
- Separating certification claims from certified scope

That judgment is the skill. The spreadsheet is the artifact.

---

## What this project demonstrates

| Skill | How this repo shows it |
|---|---|
| **Control mapping** | 15 ISO/IEC 27001:2022 Annex A topics mapped to official Airbus disclosures |
| **Evidence discipline** | Every row cites a source ID (S1–S5); unsupported claims marked "Not assessable from public sources" |
| **Scope literacy** | Distinguishes Airbus SE (group) from Airbus Protect (certified entity); inspects certificate scope |
| **Evidence request design** | 15 detailed evidence requests (EV-01 to EV-15) with owner, acceptance criteria, and priority |
| **Validation planning** | 5-phase roadmap from scope validation to remediation closure |
| **Documentation quality** | Structured CSV registers with source register and assessor notes |

---

## Scope and boundaries

### In scope
- **Entity studied:** Airbus SE (public corporate disclosures only)
- **Standard:** ISO/IEC 27001:2022, **selected Annex A control topics only** (15 of 93)
- **Method:** Public-source desk review
- **Review date:** 15 October 2026

### Out of scope
- ISO/IEC 27001 clauses 4–10 (management system requirements)
- All 93 Annex A controls (only 15 selected topics mapped)
- Any internal, confidential, proprietary, employee, or customer data
- Penetration testing, certification audit, or statement of conformity
- Operational effectiveness testing of any control

### Scope caution — Airbus Protect vs. Airbus SE
> **Airbus Protect** publicly describes ISO 27001 and ISO 9001 certification for specified main European sites and activities. This is **not** proof that every Airbus SE entity, site, system, or activity is certified. EV-15 in the evidence tracker exists specifically to verify the actual certificate — legal entity, sites, scope, exclusions, validity.

---

## Method

1. **Source collection** — Official Airbus disclosures (Annual Report 2024, sustainability pages, Airbus Protect certification page, document centre).
2. **Control selection** — 15 Annex A topics that could plausibly have public evidence.
3. **Evidence mapping** — Exact public statement, source ID, date accessed.
4. **Effectiveness classification** — Each control is one of:
   - **Publicly disclosed framework exists** — Governance framework named (2 controls: A.5.1, A.5.2)
   - **Publicly disclosed risk context; control effectiveness unknown** — Risk named, operation unclear (1 control: A.8.8)
   - **Not assessable from public sources** — Public record is silent; **not** a gap finding (12 controls)
5. **Evidence request design** — For every control, what an authorized auditor would request (15 rows in `evidence_tracker.csv`).
6. **Validation roadmap** — 5 phases, from scope confirmation to remediation closure.

---

## Key interpretation rule

> **No public evidence found ≠ control absent, failing, or non-compliant.**

Internal controls — access reviews, backup restore tests, MFA coverage, vulnerability remediation SLAs, privileged session logging — cannot usually be assessed from public reports. This project records where public sources are **silent**, not where Airbus is **deficient**.

---

## Repository structure

| File | Description |
|---|---|
| `README.md` | This documentation |
| `.gitignore` | Standard gitignore |
| `Airbus_ISO27001_Public_Source_Gap_Review.xlsx` | Master workbook: summary, control review, evidence tracker, validation roadmap |
| `control_review.csv` | 15 controls mapped to public evidence (source-linked) |
| `evidence_tracker.csv` | 15 evidence requests (EV-01 to EV-14 controls + EV-15 certificate scope) |
| `validation_roadmap.csv` | 5-phase validation plan (scope → closure) |
| `public_sources.csv` | 5 official sources (S1–S5) with URLs and limitations |

---

## Deliverables in detail

### `control_review.csv` (15 rows)
Columns: Company/Scope, Assessment Date, Control ID, Control Topic, Theme (Organizational / People / Technological), Public-Source Assessment, Public Evidence/Source Finding, Assessment Limitation, Evidence to Request, Priority, Suggested Owner, Recommended Validation Action, Source ID, Assessor Note.

Controls covered: A.5.1, A.5.2, A.5.7, A.5.9, A.5.15, A.5.23, A.5.24, A.5.30, A.6.3, A.8.5, A.8.8, A.8.13, A.8.15, A.8.24, A.8.32.

### `evidence_tracker.csv` (15 rows)
Columns: Evidence ID, Control/Topic, Evidence Required, Acceptance Criteria, Evidence Owner, Public Evidence Reviewed, Evidence Gap, Source ID, Follow-up Priority, Next Step, Status.

**EV-01 to EV-14** cover control evidence. **EV-15** is a scope-verification row for the Airbus Protect ISO certificate — it exists because a certification claim must be verified against the certificate itself, not the marketing page.

### `validation_roadmap.csv` (5 phases)
| Phase | Workstream | Exit criteria |
|---|---|---|
| 1 | Scope and source validation | Scope statement; certificate scope recorded |
| 2 | Evidence mapping | Source-linked assessment; no unsupported pass/fail |
| 3 | Control-owner evidence requests | Evidence tracker with received/accepted/rejected |
| 4 | Testing and gap confirmation | Evidence-backed findings with test steps |
| 5 | Remediation and closure | Approved action plan and closure evidence |

### `public_sources.csv` (5 sources)
| ID | Source | Used for |
|---|---|---|
| S1 | Airbus Annual Report 2024 — Cybersecurity section | Governance, federated model, Cyber Risk Review, alignment to ISO 27001 / IEC 62443 |
| S2 | Airbus Sustainability — Security and integrity | Corporate security commitment statement |
| S3 | Airbus Protect — Certifications | ISO 27001/9001 certification claim (specified sites) |
| S4 | Airbus Sustainability Standards — Document Centre | Listed ISO/IEC 27001:2022 certificate (to verify) |
| S5 | Airbus Annual Report 2024 — Cyber IROs | Cyber risk disclosure (not control evidence) |

---

## Findings summary

- **15 controls reviewed** across Organizational (A.5.x), People (A.6.x), Technological (A.8.x).
- **Disclosed (2):** A.5.1 (policies), A.5.2 (roles & responsibilities).
- **Partially disclosed (1):** A.8.8 (vulnerability management) — risk context named, control operation unknown.
- **Not assessable (12):** A.5.7, A.5.9, A.5.15, A.5.23, A.5.24, A.5.30, A.6.3, A.8.5, A.8.13, A.8.15, A.8.24, A.8.32 — public sources silent on operational evidence. **Expected, not a finding.**
- **Scope verification:** Airbus Protect certification must be verified against the actual certificate (EV-15) and **not** generalized to Airbus SE.

---

## Limitations

- Not an audit, penetration test, or statement of conformity.
- No confidential, proprietary, employee, or customer data accessed.
- Only 15 selected Annex A topics; not all 93 controls or clauses 4–10.
- Public sources can change; re-verify links before reuse.
- Control names paraphrased; validate against an authorized copy of ISO/IEC 27001:2022.

---

## What an auditor would do next

1. Confirm scope using Airbus's risk assessment and Statement of Applicability (SoA).
2. Request evidence per `evidence_tracker.csv` (EV-01 to EV-15).
3. Sample and test controls for operating effectiveness.
4. Interview control owners.
5. Inspect the actual Airbus Protect ISO certificate (entity, scope, exclusions, validity).
6. Document exceptions and produce findings report.

This repo stops at step 1.

---

## Skills demonstrated

ISO/IEC 27001:2022 Annex A mapping · audit evidence discipline · source register hygiene · scope analysis · evidence request design · validation planning · structured CSV/Excel documentation.

---

## Tools used

Excel / CSV · Markdown · Git / GitHub · Public web sources.

---

## Author

**Sagar Chhetri** — Cybersecurity engineering student (B.Tech CSE, Parul University, graduating May 2027), building toward GRC & audit.

- GitHub: [@Sagarchhetri83](https://github.com/Sagarchhetri83)
- LinkedIn: [sagar-chhetri-dev](http://www.linkedin.com/in/sagar-chhetri-dev)
- Email: sagarchhetri1243@gmail.com

---

## License

MIT License. See [LICENSE](LICENSE) for details.

---

*Portfolio exercise using public sources. Not affiliated with, endorsed by, or representative of Airbus SE or Airbus Protect.*
