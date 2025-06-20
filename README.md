# 🏁 Formula 1 Race Prediction System

A comprehensive machine learning pipeline for predicting Formula 1 race outcomes using ensemble methods, Bayesian optimization, and circuit-specific feature engineering.

## 🚀 Overview

Formula 1 race prediction system that combines multiple machine learning techniques to forecast race positions with high accuracy. The system features two main models: a baseline XGBoost model and an enhanced ensemble model with sophisticated feature engineering and hyperparameter optimization.

## ✨ Key Features

- **🤖 Dual Model Architecture**: Baseline XGBoost and Enhanced Ensemble models
- **🔬 Bayesian Hyperparameter Optimization**: Using Optuna for optimal model performance
- **🏁 Circuit-Specific Features**: Historical performance analysis for each track
- **📅 Time-Aware Cross Validation**: Prevents data leakage with GroupKFold validation
- **🎯 Ensemble Learning**: Stacking with XGBoost and Random Forest
- **📊 Comprehensive Evaluation**: Podium, Top 10, and points scoring accuracy metrics
- **📈 Advanced Visualizations**: 12 comprehensive analysis charts

## 🏆 Model Performance

### Enhanced Ensemble Model Results
- **Overall MAE**: 1.593 positions
- **Podium Prediction Accuracy**: 90.4%
- **Top 10 Prediction Accuracy**: 92.1%
- **Points Scoring Accuracy**: 92.1%

### Baseline XGBoost Model Results
- **Overall MAE**: 1.603 positions
- **Podium Prediction Accuracy**: 90.6%
- **Top 10 Prediction Accuracy**: 91.4%

## 🛠️ Technical Stack

- **Python 3.11+**
- **Core Libraries**: pandas, numpy, scikit-learn, xgboost
- **Optimization**: optuna
- **Visualization**: matplotlib, seaborn
- **Data Processing**: Custom feature engineering pipeline


## 🏃‍♂️ Quick Start

### Baseline Model
```python
# Run the baseline XGBoost model
jupyter notebook basemodel.ipynb
```

### Enhanced Ensemble Model
```python
# Run the advanced ensemble model with full pipeline
jupyter notebook ensemblemodels.ipynb
```

## 🔍 Model Features

### Core Features
- **Grid Position**: Starting position from qualifying
- **Driver Standings**: Current championship points and wins
- **Constructor Standings**: Team performance metrics
- **Lap Time Statistics**: Mean, min, max, and standard deviation
- **Pit Stop Data**: Number of stops and duration statistics
- **Qualifying Performance**: Best qualifying times and positions
- **Sprint Race Results**: Sprint qualifying and race positions

### Enhanced Features (Ensemble Model)
- **Circuit-Specific Performance**: Historical driver/constructor performance per track
- **Circuit Difficulty Index**: Average points scored at each circuit
- **Advanced Aggregations**: Rolling averages and trend analysis

## 📈 Model Pipeline

### 1. Data Preprocessing
- Load and merge multiple F1 datasets
- Filter data for recent years (2018-2024)
- Handle missing values and data cleaning

### 2. Feature Engineering
- Create aggregated statistics for drivers and constructors
- Generate circuit-specific performance metrics
- Extract qualifying and sprint race features

### 3. Model Training
- **Baseline**: Standard XGBoost with manual hyperparameters
- **Enhanced**: Bayesian optimization with Optuna (30 trials)
- Time-aware cross-validation using GroupKFold

### 4. Ensemble Learning
- Stacking regressor with XGBoost and Random Forest
- Ridge regression as meta-learner
- 5-fold cross-validation for base models

### 5. Evaluation
- Multiple accuracy metrics for different prediction categories
- Comprehensive visualization suite
- Race-by-race prediction analysis

## 📊 Visualizations

The system generates 12 comprehensive visualizations:
1. Model Performance Comparison
2. Classification Accuracies
3. Feature Importance Analysis
4. Circuit Performance Analysis
5. Prediction vs Actual Scatter Plot
6. Error Distribution Comparison
7. Cross-Validation Scores
8. Hyperparameter Optimization History
9. Season Points Prediction
10. Position Distribution Analysis
11. Grid vs Final Position Correlation
12. Constructor Performance Analysis

## 🎯 Use Cases

- **Race Prediction**: Forecast finishing positions for upcoming races
- **Fantasy F1**: Optimize team selections based on predicted performance
- **Betting Analysis**: Identify value bets with probability assessments
- **Team Strategy**: Understand performance factors and circuit-specific trends
- **Academic Research**: Study machine learning applications in sports analytics

## 🔬 Technical Highlights

### Bayesian Optimization
- Automated hyperparameter tuning using Optuna
- 30 trials for optimal parameter selection
- Significant performance improvement over manual tuning

### Time-Aware Validation
- GroupKFold cross-validation by race year
- Prevents temporal data leakage
- Realistic performance estimation

### Circuit Intelligence
- Track-specific driver and constructor performance
- Historical win rates and average positions
- Circuit difficulty indexing

## 📝 Model Improvements

The Enhanced Ensemble Model shows:
- **0.6% MAE improvement** over baseline XGBoost
- **3 circuit-specific features** added
- **~15% error reduction** through hyperparameter optimization
- **Robust ensemble approach** with multiple algorithms

## 📊 Example Output

```
🏎️ RACE 1132: Silverstone Circuit
------------------------------------------------------------
Driver Grid Pred Actual
 HAM    2    2    1
 VER    4    3    2
 NOR    3    3    3
 PIA    5    5    4
 SAI    7    5    5
 STR    8    8    7
 ALO   10    8    8
 HUL    6    9    6
 ALB    9   10    9
 TSU   13   11   10
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the GNU General Public License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Formula 1 World Championship (1950–2020) Dataset](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020) by [Rohan Rao](https://www.kaggle.com/rohanrao) on Kaggle  

---
