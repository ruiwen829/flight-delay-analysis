# Flight Delay Analysis

This project predicts whether a U.S. domestic flight will arrive at least 15 minutes late using information available two hours before scheduled departure.

The analysis was completed as a data science case study and includes exploratory analysis, feature engineering, model development, validation, and operational evaluation.

## Approach

The prediction point is set at **T-2 hours before scheduled departure**. The goal is to give an airline operations team enough time to act while still using recent operational information.

The analysis compares:

- Schedule-based features
- Inbound aircraft status
- Aircraft information
- Origin weather conditions

Logistic regression is used as a baseline, followed by XGBoost.

## Data

The analysis uses:

- U.S. DOT / BTS On-Time Performance data
- FAA aircraft registry data
- Iowa Environmental Mesonet (IEM) ASOS weather observations

Raw and processed data are not included in this repository because of their size.

## Final Results

The final model was evaluated on a held-out test period covering July–December 2025.

| Metric | Result |
|---|---:|
| ROC-AUC | 0.7417 |
| PR-AUC | 0.4941 |

Operational performance:

| Flights Targeted | Precision | Recall |
|---|---:|---:|
| Top 1% | 86.96% | 3.83% |
| Top 5% | 70.18% | 15.45% |
| Top 10% | 60.11% | 26.47% |
| Top 20% | 49.11% | 43.25% |

For example, among the **10% of flights ranked highest risk, 60.11% were actually delayed**, capturing 26.47% of all delayed flights.

## Repository

- `submission_notebook.ipynb` — full analysis and report
- `requirements.txt` — Python dependencies

## Setup

Install the required packages with:

```bash
pip install -r requirements.txt