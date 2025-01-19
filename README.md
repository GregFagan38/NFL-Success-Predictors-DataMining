# NFL Success Predictors

**Contributors:**  
Max Enabnit, Greg Fagan, Brian Karstens, Christian Kleronomos, Luke Rubin  

## Instructions for Repository 

The repository is broken down into three folders consisting of infromation on the data, report, and Models used in the project. Each folder except "Report" will have a "README.md" file to explain how to navigate the folders.

## Summary

This project focuses on creating two predictive models for the NFL:  
1. **Playoff Qualification Predictor:** Determines whether an NFL team will make the playoffs.  
2. **Game Winner Predictor:** Predicts if the home or away team will win a game.  

Using data from the past 22 NFL seasons, these models aim to provide actionable insights for sportsbooks like FanDuel to enhance their money line and futures predictions. By incorporating these models, sportsbooks can improve profitability while offering a more engaging experience for their users.  

Key insights reveal that offensive stats and some defensive metrics significantly contribute to accurate predictions. The models are designed to complement existing projection systems with minimal associated costs.

---

## Problem Description

### Background
The NFL's competitive nature leads to fluctuating team performances influenced by various factors. Accurately predicting game winners and playoff qualifications has significant implications for both sports analytics and the betting industry. With over $35 billion wagered on the NFL annually in the U.S., better predictions can lead to increased profitability and engagement.

### Goals
- **Business Goal:** Support sports betting strategies by predicting game winners and playoff teams to set more profitable betting lines.
- **Data Mining Goal:** Build supervised classification models for game outcomes and playoff qualifications using historical data.

---

## Data Description

### Source
The dataset was sourced from [Kaggle](https://www.kaggle.com/datasets/cviaxmiwnptr/nfl-team-stats-20022019-espn/data), featuring team statistics from the 2002-2003 to 2023-2024 NFL seasons. After preprocessing, the dataset included:
- **Rows:** 4,861  
- **Columns:** 61 (e.g., passing yards, red zone completions, sacks, penalties)

### Preprocessing
1. **Data Cleaning:** Removed structurally missing data from seasons prior to 2006-2007.  
2. **Feature Engineering:** Created "difference" variables for home and away stats (e.g., passing yards difference).  
3. **Aggregation:** For the playoff predictor, team statistics were aggregated by season, and a binary `made_playoffs` variable was added.  

### Exploratory Analysis
Key visualizations included:
- Bar charts highlighting feature importance (e.g., passing yards, third-down completions).  
- Correlation analyses to identify relationships between variables.  
- Box plots and line charts to explore trends in playoff qualification and game outcomes.

---

## Data Mining Solution

### Models
**Model 1: Game Winner Predictor**  
- **Target Variable:** `winner` (home/away)  
- **Training Data:** 2006-2018 seasons  
- **Testing Data:** 2019-2023 seasons  
- **Classifiers Tested:** Logistic Regression, Decision Tree, Gradient Boosting, Random Forest  

**Model 2: Playoff Qualification Predictor**  
- **Target Variable:** `made_playoffs` (yes/no)  
- **Training Data:** 2002-2018 seasons  
- **Testing Data:** 2019-2023 seasons  
- **Classifiers Tested:** Logistic Regression, Decision Tree, Gradient Boosting, Random Forest  

### Performance Evaluation
- **Game Winner Predictor:** Logistic regression achieved the best balance of performance metrics (AUC = 0.968, CA = 0.900) with minimal overfitting.  
- **Playoff Qualification Predictor:** Logistic regression also outperformed other models (AUC = 0.862, CA = 0.787).  

---

## Conclusion

### Recommendations
1. **Leverage Home-Field Advantage Insights:** Home teams consistently perform better in metrics like passing yards and red zone efficiency. These insights can inform more accurate betting lines.  
2. **Expand Betting Options:** Introduce prop and parlay bets based on key predictors (e.g., penalties, turnovers).  
 

### Limitations
- **Data Constraints:** Limited samples for season-level aggregated playoff data.  
- **Future Improvements:** As more data becomes available, the models can be refined for even greater accuracy.  

---
