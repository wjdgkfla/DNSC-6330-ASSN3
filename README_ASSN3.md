# Assignment 3 - Disparate Impact Audit (Lecture 03, COMPAS)

## Purpose of the Analysis
This repository reproduces the Lecture 03 COMPAS disparate impact audit workflow in Python. The goal is to preserve the core lecture framework: AIR/ME/SMD disparity metrics, error-rate disparity testing, intersectional subgroup analysis, statistical significance checks, and compliance-oriented interpretation.

Notebook included:
- `Assignment_3_lecture03_aligned.ipynb`

Reference materials used:
- `DNSC_6330_Lecture-03.pdf`
- `Lecture_03_bias.ipynb`

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `statsmodels`
- `scikit-learn`
- `solas-disparity` (`import solas_disparity as sd`)

## How This Notebook Matches the Assignment Requirements
### 1) Compute AIR, ME, and SMD
- Computes AIR and ME for race and sex.
- Computes SMD using model score output (predicted probability).
- Includes manual calculations and Solas-based calculations.

### 2) Manual vs Solas Consistency Checks
- Explicitly compares manual vs Solas AIR/ME outputs.
- Explicitly compares manual vs Solas SMD outputs.
- Uses tolerance-based pass/fail checks.

### 3) Error-Rate Disparity Analysis
- Computes FPR and FNR by race.
- Compares race-level error rates to Caucasian baseline.
- Runs two-proportion z-tests for selection-rate and error-rate disparities.

### 4) Intersectional Subgroup Analysis
- Builds race x sex subgroup table.
- Reports subgroup counts and selection rates.
- Computes subgroup AIR and identifies worst-group AIR.

### 5) Visualization and Compliance Memo
- Produces lecture-style FPR/FNR by race figure with Caucasian baseline line.
- Saves figure as `error_rate_disparity.png`.
- Includes a compliance memo with practical + statistical significance framing and burden-shifting context.

## Reproducibility Instructions
1. Create and activate a Python 3.11+ environment.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib statsmodels scikit-learn solas-ai
   ```
3. Open Jupyter and run all cells in:
   - `Assignment_3_lecture03_aligned.ipynb`

## Expected Outputs
- Race and sex AIR/ME tables (manual and Solas).
- SMD tables (manual and Solas).
- Manual-vs-Solas pass/fail consistency checks.
- FPR/FNR disparity table and z-test outputs.
- Intersectional subgroup AIR table with worst-group report.
- Figure: `error_rate_disparity.png`.
- Final compliance memo (with word count printout).

## Note on Interpretation
The notebook follows Lecture 03 guidance to report both:
- Practical significance (AIR/ME/SMD/effect size), and
- Statistical significance (p-values).

These metrics are interpreted jointly under disparate impact and burden-shifting compliance framing.
