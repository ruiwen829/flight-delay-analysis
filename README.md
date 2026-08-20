# Flight Delay Analysis

This project predicts whether a U.S. domestic flight will arrive at least 15 minutes late using information available **two hours before scheduled departure**.

The analysis uses U.S. DOT/BTS flight data, FAA aircraft data, and IEM weather observations. It covers EDA, feature engineering, model development, validation, and operational evaluation.

## Final Results

The final model was evaluated on a held-out Jul–Dec 2025 test set:

- **ROC-AUC:** 0.7417
- **PR-AUC:** 0.4941
- **Top 10% precision:** 60.11%
- **Top 10% recall:** 26.47%

## Files

- `submission_notebook.ipynb` — analysis and report
- `requirements.txt` — Python dependencies

Raw and processed datasets are not included due to their size.