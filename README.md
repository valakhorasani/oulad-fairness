# OULAD Intersectional Fairness Audit

Code and resources for: *Intersectional Fairness in Early Student 
Withdrawal Prediction: Absolute Harm Quantification, Feature Leakage 
Audit, and Module-Level Replication on OULAD*

Vala Khorasani, University of Leicester (sk1175@student.le.ac.uk)

## Data

This study uses the Open University Learning Analytics Dataset (OULAD).
Download the 7 CSV files from:
https://analyse.kmi.open.ac.uk/open_dataset

Place all CSV files in a single directory and update DATA_PATH in Cell 1 
of the notebook to point to that directory.

## Requirements

Python 3.9+, pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn, scipy

Install with: pip install pandas numpy scikit-learn xgboost matplotlib seaborn scipy

## Running the notebook

Open OULAD_Fairness_final.ipynb and run all cells top to bottom.
Cell 1 must be updated with your local DATA_PATH before running.
All figures are saved to ./figures/ automatically.

## Key findings

- Feature leakage in prior OULAD studies inflates AUC from 0.805 to 0.995
- Disabled & Deprived students face 2.19× the Absolute Miss Rate of 
  the reference group (AMR diff = 17.88 per 100, p < 0.0001)
- AMR finding replicates across 3 independent course cohorts 
  (IVW pooled: 18.27 [9.25, 27.30], p = 0.0001, I² = 0%)
- Group-specific threshold calibration reduces FNR disparity by 92% 
  at negligible F1 cost (ΔF1 = −0.002)

## Reproducibility

All experiments use random_state=42. Results are fully reproducible 
given the OULAD dataset and the package versions above.
