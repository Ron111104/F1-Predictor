---

# Formula 1 Race Prediction System

A comprehensive machine learning pipeline for predicting Formula 1 race outcomes using ensemble methods, Bayesian optimization, and circuit-specific feature engineering.

---

## I. Overview

This system combines multiple machine learning techniques to forecast Formula 1 race positions with high accuracy. It features two main models:

* A baseline XGBoost model
* An enhanced ensemble model with advanced feature engineering and hyperparameter optimization

---

## II. Key Features

* Dual Model Architecture: Baseline XGBoost and Enhanced Ensemble models
* Bayesian Hyperparameter Optimization using Optuna
* Circuit-Specific Features: Historical performance per track
* Time-Aware Cross Validation with GroupKFold
* Ensemble Learning with XGBoost and Random Forest
* Comprehensive Evaluation: Podium, Top 10, and points-scoring metrics
* Advanced Visualizations: 12 diagnostic analysis charts

---

## III. Model Performance

### Enhanced Ensemble Model

* Mean Absolute Error (MAE): 1.282 positions
* Podium Prediction Accuracy: 91.2%
* Top 10 Prediction Accuracy: 93.7%

### Baseline XGBoost Model

* Mean Absolute Error (MAE): 1.603 positions
* Podium Prediction Accuracy: 90.6%
* Top 10 Prediction Accuracy: 91.4%

---

## IV. Technical Stack

* Python 3.11+
* Libraries: pandas, numpy, scikit-learn, xgboost
* Optimization: optuna
* Visualization: matplotlib, seaborn
* Data Processing: Custom feature engineering pipeline

---

## V. Quick Start

### Baseline Model

```bash
jupyter notebook basemodel.ipynb
```

### Ensemble Model

```bash
jupyter notebook ensemblemodels.ipynb
```

---

## VI. Model Features

### Core Features

* Grid Position (qualifying)
* Driver Standings: Points and Wins
* Constructor Standings
* Lap Time Statistics: Mean, Min, Max, Std
* Pit Stop Duration and Count
* Best Qualifying Time
* Sprint Race Position and Points (from 2021)

### Enhanced Features (for Ensemble)

* Circuit-Specific Driver/Constructor Trends
* Circuit Difficulty Index
* Rolling Averages and Aggregated Season Stats

---

## VII. Model Pipeline

1. **Data Preprocessing**

   * Load and merge multiple Formula 1 datasets
   * Filter data for years 2018–2024
   * Handle missing values and data inconsistencies

2. **Feature Engineering**

   * Aggregate statistics for drivers and constructors
   * Extract circuit-level performance data
   * Incorporate qualifying and sprint race metrics

3. **Model Training**

   * Baseline: XGBoost with fixed parameters
   * Ensemble: Hyperparameter tuning with Optuna (30 trials)
   * Cross-validation with GroupKFold (year-based)

4. **Ensemble Learning**

   * Stacking using XGBoost and Random Forest
   * Ridge Regression as meta-learner
   * 5-fold cross-validation for base estimators

5. **Evaluation**

   * MAE and classification metrics (Podium, Top 10)
   * Season-wide predictions and race-by-race breakdown
   * Comprehensive plots and analytics

---

## VIII. Visualizations

1. Model Performance Comparison
2. Podium and Top 10 Accuracy Scores
3. Feature Importance Ranking
4. Circuit Performance Trends
5. Prediction vs Actual Scatter Plot
6. Error Distribution Histograms
7. Cross-Validation Fold Scores
8. Optuna Optimization History
9. Predicted Points Distribution
10. Finishing Position Histograms
11. Grid vs Final Position Correlation
12. Constructor Season Trends

---

## IX. Use Cases

* Race Position Forecasting
* Fantasy Formula 1 Team Optimization
* Performance-Based Betting Analysis
* Team Strategic Decision Support
* Machine Learning in Sports Research

---

## X. Technical Highlights

### Hyperparameter Optimization

* Optuna with Bayesian search
* 30 trials to fine-tune XGBoost and Random Forest
* \~15% error reduction over manual tuning

### Time-Aware Validation

* Year-based GroupKFold
* Prevents temporal data leakage
* Realistic test scenarios

### Circuit Intelligence

* Track-specific trends per constructor and driver
* Circuit difficulty ratings
* Historical performance encoding

---

## XI. Model Improvements

* 0.6 MAE improvement over baseline
* Three circuit-specific features added
* Error reduction through optimization and ensembling
* Stacked learning with diverse regressors

---

## XII. Example Output

```
RACE 1132: Silverstone Circuit
----------------------------------------
Driver   Grid   Pred   Actual
HAM       2       1       1
VER       4       2       2
NOR       3       3       3
PIA       5       4       4
SAI       7       5       5
ALO      10       6       8
STR       8       7       7
HUL       6       8       6
ALB       9       9       9
TSU      13      10      10
```

---

## XIII. Contributing

1. Fork the repository
2. Create a new feature branch (`git checkout -b feature/your-feature-name`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature-name`)
5. Open a Pull Request

---

## XIV. License

This project is licensed under the GNU General Public License v3.0. See the [LICENSE](LICENSE) file for details.

---

## XV. Acknowledgments

* [Formula 1 World Championship (1950–2020) Dataset on Kaggle](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020)
* The Kaggle and F1 data communities
* Developers of XGBoost, scikit-learn, and Optuna

---


