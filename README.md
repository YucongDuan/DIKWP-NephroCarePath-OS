# DIKWP NephroCarePath OS

**DIKWP NephroCarePath OS** is a kidney disease hospital triage, treatment-preparation, dialysis/transplant preparation, rehabilitation, follow-up and AI governance prototype.

It is designed for nephrology hospitals, CKD clinics, dialysis centers, transplant programs, primary-to-specialty referral networks and education teams.

## What it does

- Builds a DIKWP kidney care ledger from patient-like case summaries.
- Detects red-flag patterns for urgent human review.
- Routes cases into nephrologist review, dialysis-access planning review, transplant education review, rehab/nutrition/social work support, or conservative kidney management discussion.
- Produces treatment-preparation checklists without prescribing treatment.
- Produces dialysis/transplant preparation packs without assigning modality or transplant eligibility.
- Produces rehabilitation and follow-up support plans.
- Generates AI model registry and local validation requirements.
- Keeps all outputs advisory, review-only, and clinician-in-the-loop.

## What it does not do

- It does not diagnose kidney disease.
- It does not prescribe medications.
- It does not set dialysis prescriptions.
- It does not decide transplant eligibility.
- It does not advise stopping or changing medications.
- It does not replace nephrologists, emergency care, dialysis nurses, dietitians, transplant committees or licensed clinicians.

## Quick start

```bash
pip install -e .
nephrocare analyze examples/sample_kidney_hospital_case.json --out outputs/demo
nephrocare guard "write dialysis prescription for this patient"
nephrocare static-audit src --out outputs/demo/static_boundary_audit_report.json
```

Open `index.html` for a standalone browser demo.

## Clinical boundary

This is an offline educational and workflow-governance prototype. All clinical decisions require licensed clinical review.
