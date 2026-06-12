# FIFA World Cup 2026 Prediction Engine

Machine learning pipeline for predicting the complete FIFA World Cup 2026 tournament, including group stage outcomes, knockout-stage matchups, scorelines, penalties, and tournament progression.

## Overview

This project was developed to forecast all 104 matches of the FIFA World Cup 2026 under FIFA's new 48-team format.

The system combines:

* XGBoost classification models
* XGBoost goal prediction models
* FIFA rankings
* Elo ratings
* Team strength metrics
* Recent form statistics
* Monte Carlo knockout simulations
* Official FIFA Annex C bracket generation

The engine predicts both individual matches and the entire tournament structure from the group stage through the final.

---

## Performance

### Match Outcome Model

| Metric         | Score  |
| -------------- | ------ |
| Accuracy       | 60.25% |
| Macro F1 Score | 0.4395 |

### Goal Prediction Models

| Metric        | Score |
| ------------- | ----- |
| Home Goal MAE | 1.00  |
| Away Goal MAE | 0.77  |

---

## Features

### Match Prediction

For every match:

* Home Win / Draw / Away Win probabilities
* Exact score prediction
* Corners prediction
* Yellow card prediction
* Red card prediction

### Tournament Simulation

* Group stage simulation
* Qualification engine
* Best third-place selection
* FIFA Annex C implementation
* Knockout bracket generation
* Round of 32 to Final progression

### Monte Carlo Forecasting

* Championship probabilities
* Knockout progression probabilities
* Tournament uncertainty estimation

---

## Data Sources

* International Football Match Results
* FIFA Rankings
* Elo Ratings
* Shootout Records
* Goal Scorer Data
* FIFA World Cup 2026 Fixtures
* Official Annex C Mapping

---

## Machine Learning Pipeline

### Feature Engineering

23 engineered features including:

* Elo ratings
* FIFA rankings
* FIFA ranking points
* Squad strength ratings
* Goals scored form
* Goals conceded form
* Recent points form
* Goal difference form

### Models

#### Outcome Model

* XGBoost Multi-Class Classifier
* Classes:

  * Home Win
  * Draw
  * Away Win

#### Goal Models

* XGBoost Regressor (Home Goals)
* XGBoost Regressor (Away Goals)

---

## Tournament Format Supported

* 48 Teams
* 12 Groups
* 72 Group Stage Matches
* 32 Knockout Matches
* Official FIFA Qualification Rules
* Official FIFA Annex C Round of 32 Mapping

Total Matches Predicted:

```text
104
```

---

## Repository Structure

```text
.
├── notebook.ipynb
├── annex_c.json
├── eloratings.csv
├── international_matches.csv
├── fifa_ranking-2023-07-20.csv
├── fifa_ranking-2024-04-04.csv
├── fifa_ranking-2024-06-20.csv
├── goalscorers.csv
├── shootouts.csv
├── former_names.csv
├── xgb_outcome_model.pkl
│
├── data/
│   ├── group_fixtures.csv
│   ├── knockout_slots.csv
│   ├── group_fixtures_BACKUP.csv
│   └── knockout_slots_BACKUP.csv
│
├── final_group_predictions.csv
├── final_knockout_predictions.csv
├── submission_group_fixtures.csv
└── submission_knockout_slots.csv
```

---

## Key Highlights

* 23,000+ historical international matches used
* 23 engineered predictive features
* 60.25% validation accuracy
* FIFA Annex C compliant
* Full tournament simulation engine
* Monte Carlo knockout forecasting
* Automated submission generation

---

## Technologies

* Python
* Pandas
* NumPy
* XGBoost
* Scikit-Learn
* Jupyter Notebook
* Git

---

## Author

**Mukhul Elango**

GitHub: https://github.com/mukhul
