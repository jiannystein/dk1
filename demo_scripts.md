# Demo Scripts

## Demo 1 — Translation with back-translation

Objective: show safe translation workflow using synthetic patient instructions.

Prompt:

```text
You are assisting a hospital educator.

Draft a patient instruction sheet in English and Bahasa Melayu.
Requirements:
- use short sentences
- use plain language
- preserve all safety warnings
- add a back-translation section to English
- mark any sentence that may need human interpreter review
- do not invent dosing, diagnosis, or follow-up intervals
```

Safety point: translation output must be reviewed before patient use.

## Demo 2 — Synthetic patient note to structured summary

Prompt:

```text
You are assisting a hospital staff member preparing a draft summary for review.

Using only the provided synthetic note:
1. Create a structured summary.
2. List follow-up items.
3. Identify missing information.
4. Draft a patient-friendly explanation.
5. Do not invent diagnosis, medication, dosage, or appointment dates.
6. Mark the output as "Draft for clinical review".
```

## Demo 3 — Radiology worklist prioritisation

Prompt:

```text
You are assisting a radiology operations manager.

Given a CSV with accession_id, modality, body_part, arrival_time, AI_risk_score, suspected_critical_flag, inpatient_or_ed, and target_SLA_minutes:
1. Rank studies for review priority.
2. Explain the prioritisation rule in plain language.
3. Flag which studies require immediate radiologist attention.
4. Output a table with ranked_order, accession_id, reason_for_priority.
5. Do not diagnose.
6. Do not generate final clinical interpretations.
```

## Demo 4 — Physiotherapy progress summary

Prompt:

```text
You are a rehabilitation assistant helping a physiotherapist.

Input:
- baseline movement summary
- week-4 movement summary
- pain score trend
- adherence rate
- therapist goals

Task:
1. Summarize progress in plain clinical English.
2. Identify 3 questions the physiotherapist should verify in person.
3. Draft a patient-friendly home exercise reminder.
4. Do not diagnose.
5. Do not recommend progression if adherence <70% or if any red flag is present.
```

## Demo 5 — Vestibular symptom diary summary

Prompt:

```text
You are assisting a physiotherapist with documentation.

Using the provided vestibular symptom diary:
1. Summarize symptom trend.
2. Identify entries that may require therapist review.
3. Draft a short patient-friendly reminder.
4. Do not diagnose BPPV, vestibular migraine, central cause, or any other condition.
5. Do not recommend manoeuvres or exercise progression.
6. Flag red symptoms for clinician review.
```

## Demo 6 — Vendor evaluation scorecard

Prompt:

```text
You are helping a hospital AI governance group evaluate AI platform options.

Using the vendor scorecard fields:
privacy, data residency, audit logs, IAM/SSO, RAG capability, multimodal capability, healthcare suitability, integration, cost, lock-in, clinical-use restriction

Task:
1. Score each vendor from 1 to 5.
2. Explain each score briefly.
3. Identify missing evidence.
4. Recommend which vendors are suitable for low-risk pilots only.
5. Do not make final procurement decisions.
```
