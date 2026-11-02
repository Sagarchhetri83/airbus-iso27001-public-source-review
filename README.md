# Airbus ISO/IEC 27001:2022 - Public-Source GRC Review

**Company studied:** Airbus SE (public corporate disclosures)  
**Separate certification reference:** Airbus Protect (do not generalize its scope to all Airbus SE operations)  
**Review date:** 15 October 2026  
**Type:** Public-source desk review / portfolio exercise

## Why this project exists
This portfolio project uses publicly available company disclosures instead of a fictional organization. It demonstrates how a GRC analyst can map public evidence to selected ISO/IEC 27001:2022 Annex A control topics, record evidence limitations, identify what must be requested from control owners, and build a validation roadmap.

## Repository files
- `Airbus_ISO27001_Public_Source_Gap_Review.xlsx` — summary, selected-control review, evidence tracker, and validation roadmap.
- `control_review.csv` — selected-control public-source review.
- `evidence_tracker.csv` — evidence needed to validate each control.
- `validation_roadmap.csv` — phased next steps for authorized internal validation.
- `public_sources.csv` — source register with links and limitations.

## Public sources used
1. Airbus Annual Report 2024, including its cybersecurity disclosure: https://www.airbus.com/sites/g/files/jlcbta136/files/2025-04/Airbus%20Annual%20Report%202024.pdf
2. Airbus Sustainability: https://www.airbus.com/en/sustainability
3. Airbus Protect certifications: https://www.protect.airbus.com/about-us/our-certifications/
4. Airbus Sustainability Standards and Performance document centre: https://www.airbus.com/en/sustainability/sustainability-standards-and-performance/document-centre

The annual report describes cybersecurity risk and enterprise-level governance, including a federated digital security model and group-level cyber risk review. Airbus Protect publicly describes ISO 27001 certification for specified main European sites and activities. The exact certificate scope, legal entity, exclusions, and validity must be checked in the certificate itself.

## Method
- Use public reports and official company pages as source material.
- Record only statements directly supported by a source.
- Separate public disclosure from operational proof.
- Use **Not assessable from public sources** when the public record does not permit a control effectiveness conclusion.
- Define evidence requests and validation steps that an authorized auditor or control owner could complete.
- Confirm the assessment scope and applicability using the organization's risk assessment and Statement of Applicability (SoA) before a formal assessment.

## Key interpretation rule
**No public evidence found is not the same as a control being absent, failing, or non-compliant.** Internal controls such as access reviews, backup tests, MFA coverage, vulnerability remediation, and logging cannot usually be conclusively assessed from public reports alone. This project therefore does not claim that Airbus has gaps in these controls; it records where public sources do not provide enough evidence to assess them.

## ISO certification scope caution
Airbus Protect is a distinct business/entity context within the Airbus group. A public statement about Airbus Protect's ISO 27001 certification must not be represented as proof that every Airbus SE entity, site, system, or activity is certified. Always inspect the certificate's legal entity, scope, locations, exclusions, and validity.

## Limitations
- This is not an Airbus internal audit, penetration test, certification audit, or statement of conformity.
- No confidential, proprietary, employee, customer, or internal control evidence was accessed.
- Only selected Annex A control topics are mapped; this does not assess all Annex A controls or ISO/IEC 27001 clauses 4–10.
- Public source statements can change; confirm links and current versions before reuse.
- Validate control names and requirements against an authorized copy of ISO/IEC 27001:2022. This project paraphrases control topics and does not reproduce the standard.

## Suggested GitHub repository
`airbus-iso27001-public-source-review`

## Suggested resume bullet
Built a public-source ISO/IEC 27001:2022 GRC review of Airbus, mapping 15 selected Annex A control topics to official disclosures, separating disclosed governance from unverified control effectiveness, and creating an evidence tracker and validation roadmap.

## Recommended GitHub topics
`grc`, `iso27001`, `isms`, `compliance`, `risk-assessment`, `cybersecurity`, `audit-evidence`, `governance-risk-compliance`
