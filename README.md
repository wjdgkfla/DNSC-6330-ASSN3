# Disparate Impact Audit — AIR, SMD & Statistical Testing (DNSC 6330, Assignment 3)

Conducted a full disparate impact audit on the COMPAS recidivism model using industry-standard fairness metrics: Adverse Impact Ratio (AIR), Mean Effect (ME), Standardized Mean Difference (SMD), and intersectional subgroup analysis.

**Skills:** Python · pandas · scikit-learn · statsmodels · solas-ai · Fairness Auditing · Statistical Hypothesis Testing

---

## What This Project Demonstrates

- Computing AIR, ME, and SMD manually and verifying with Solas-AI library
- Two-proportion z-tests for selection-rate and error-rate disparities by race and sex
- Intersectional subgroup analysis (race x sex) to surface compound discrimination
- Compliance framing: practical vs. statistical significance under disparate impact doctrine
- Producing audit-ready fairness visualizations and a compliance memo

---

## Dataset

ProPublica COMPAS Recidivism — same cleaned cohort as Assignments 1 & 2

---

## Notebook

`Assignment_3_lecture03_aligned.ipynb` — runs top-to-bottom and reproduces all outputs

**Key outputs:**
- Race and sex AIR/ME tables (manual and Solas, with consistency checks)
- SMD tables (manual and Solas)
- FPR/FNR disparity table and z-test results
- Intersectional subgroup AIR table with worst-group flagging
- `error_rate_disparity.png` visualization
- Compliance memo with burden-shifting analysis

---

## Setup

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn solas-ai
jupyter notebook Assignment_3_lecture03_aligned.ipynb
```
