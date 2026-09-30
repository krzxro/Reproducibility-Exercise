# Diabetes Risk Factor Analysis


## Project Purpose
This project performs an exploratory and inferential analysis of a
patient-level diabetes dataset to identify clinical variables associated with
a diabetes diagnosis. It is designed as a reproducible template that can be
adapted by other clinical sites for similar analyses on their own patient data.

## Required Software
- Python 3.10 or later
- Jupyter Notebook, JupyterLab, VS Code, or Google Colab

## Required Python Libraries
| Package | Tested Version |
|---|---|
| pandas | 2.x |
| numpy | 1.26.x |
| matplotlib | 3.x |
| scipy | 1.11.x |

### Installation
If running locally:

Google Colab includes all required packages by default.

## Dataset Requirements
- File name: `Example Dataset_Diabetes.csv`
- Must be placed in the **same directory** as the notebook.
- Expected columns: `Pregnancies`, `Glucose`, `D_BP`,
  `Skin_Thickness`, `Insulin`, `BMI`, `Pedigree`, `Age`,
  `Outcome` (binary: 0 = no diabetes, 1 = diabetes).
- Known data quality note: `Glucose`, `D_BP`, `Skin_Thickness`,
  `Insulin`, and `BMI` use `0` as a placeholder for missing values; the
  notebook converts these to `NaN` prior to analysis.

## How to Run
1. Clone or download this repository.
2. Place `Example Dataset_Diabetes.csv` in the same folder as
   `Diabetes_Risk_Factor_Analysis.ipynb`.
3. Open the notebook in Google Colab, Jupyter, or VS Code.
4. Run all cells from top to bottom (recommended: **Runtime -> Restart
   session and run all** in Colab, or **Kernel -> Restart & Run All** in
   Jupyter).
5. Do not skip or reorder sections as later cells depend on variables (`df`,
   `df_clean`) created earlier in the notebook.

## Expected Outputs
- Console output confirming dataset shape, missing values, and schema
  validation.
- Descriptive statistics table for all clinical variables.
- Four visualizations: two univariate histograms, two bivariate plots
  (boxplot and scatter plot), and one correlation heatmap.
- Statistical test results: an independent t-test (Glucose by Outcome) and a
  chi-square test (Age Group by Outcome), each with printed test statistics
  and p-values.
- A reproducibility check confirming identical results across repeated
  calculations within the same session.

## Assumptions and Limitations
- The provided dataset matches the documented schema; the notebook will
  raise a clear error if expected columns are missing.
- Results reflect associations only; no causal claims are made.
- This dataset represents a single patient population and results may not
  generalize to other clinical sites without local validation.
- No predictive model is trained in this notebook; it establishes the
  exploratory and statistical foundation for a subsequent supervised
  machine learning pipeline.

## Reproducibility Notes
- A fixed random seed (`RANDOM_SEED = 42`) is set at the beginning of the
  notebook and should be used in any future random operations (e.g.,
  train/test splitting).
- All data transformations create new variables (e.g., `df_clean`) rather
  than repeatedly modifying the original DataFrame in place, so cells can be
  safely re-run without changing results.

## Google Colab Notebook
[Open in Google Colab](https://colab.research.google.com/drive/1jqwRpJGoPCQGRTt7wOQVBzc4Gc1c-yI1?usp=sharing)
