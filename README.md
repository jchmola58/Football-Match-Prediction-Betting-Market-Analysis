# Football Match Analysis and Prediction

## Author

Jozef Chmola

## Project Overview

This project focuses on the analysis and prediction of football match results using historical data from the top five European football leagues.

The dataset contains match data from the following leagues:

* Premier League
* Bundesliga
* Serie A
* La Liga
* Ligue 1

The analysis covers five seasons:

* 2021/22
* 2022/23
* 2023/24
* 2024/25
* 2025/26

The main goal of the project is to explore football match statistics, identify relationships between different match characteristics and match outcomes, and build machine learning models capable of predicting future match results.

## Data Source

The data was obtained from **Football-Data.co.uk**:

https://football-data.co.uk/

Football-Data.co.uk provides historical football results, match statistics and betting odds in CSV and Excel formats.

## Main Objectives

The project focuses mainly on football match statistics rather than betting data.

The main objectives are:

* Explore and understand the football dataset.
* Analyse differences between the five major European leagues.
* Investigate factors related to match outcomes.
* Analyse home advantage.
* Analyse team form and previous performance.
* Investigate the relationship between shots, shots on target, corners, fouls and cards and match results.
* Create new features based on historical team performance.
* Build machine learning models for predicting match outcomes.
* Evaluate how well the models generalise to unseen data.
* Investigate whether a model trained on some leagues can be applied to another league.

Betting odds will also be considered as an additional part of the project, mainly to investigate whether a machine learning model can outperform bookmaker predictions on unseen data.

## Research Hypotheses

The project will investigate several hypotheses, including:

1. Teams with better recent form have a higher probability of winning their next match.

2. Home teams have a higher probability of winning than away teams.

3. Teams perform differently at home and away.

4. A higher number of shots and shots on target is associated with a higher probability of winning.

5. Teams that have more corners than their opponents are more likely to win.

6. The number of fouls and cards differs significantly between leagues.

7. The five major European leagues have different playing characteristics.

8. Serie A has a lower average number of goals per match than the other major European leagues.

9. Bundesliga has a higher average number of goals per match than the other major European leagues.

10. Historical team performance can be used to predict the outcome of future matches better than a simple baseline model.

11. A model based on general team performance characteristics can generalise to a league that was not used for training.

12. A machine learning model can potentially achieve better predictions than bookmaker odds on unseen matches.

Additional hypotheses may be developed during the exploratory data analysis.

## Dataset Features

The dataset contains several types of information.

### Match Information

Examples:

* Date
* Time
* Home team
* Away team
* League
* Season
* Referee

### Match Results

Examples:

* Full-time home goals
* Full-time away goals
* Full-time result
* Half-time home goals
* Half-time away goals
* Half-time result

### Match Statistics

Examples:

* Shots
* Shots on target
* Fouls
* Corners
* Yellow cards
* Red cards

These variables will be particularly important for the exploratory analysis.

### Betting Data

The original dataset also contains a large number of bookmaker odds and betting-related variables.

These variables will not be the main focus of the project, but they may be used in a separate experiment comparing machine learning predictions with bookmaker odds.

## Feature Engineering

An important part of the project will be the creation of new features based only on information available before a match.

Possible features include:

* Recent team form
* Points from previous matches
* Goals scored in previous matches
* Goals conceded in previous matches
* Home performance
* Away performance
* Win rate
* Average shots
* Average shots on target
* Average corners
* Average cards

Care will be taken to avoid data leakage. Information that only becomes available after a match, such as the final number of goals, shots or corners from that same match, will not be used as input features for pre-match prediction.

## Machine Learning

Several machine learning approaches will be tested and compared.

Possible models include:

* Baseline model
* Logistic Regression
* Random Forest
* Other models if appropriate

The target variable will primarily be the full-time match result:

* `H` – Home win
* `D` – Draw
* `A` – Away win

The models will be evaluated using appropriate classification metrics such as:

* Accuracy
* Balanced Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

## Generalisation to Unseen Data

A key part of the project will be testing whether the developed models can generalise beyond the data used for training.

The historical seasons will be used for model development and evaluation, while a completely unseen season may be used for a final evaluation.

If available, the 2026/27 season can be used as an additional external test set because it is not part of the original five-season dataset.

## Project Structure

```text
football-match-analysis/
│
├── data/
│   └── ...
│
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_data_exploration.ipynb
│   ├── 03_feature_engineering.ipynb
│   └── 04_modeling.ipynb
│
├── src/
│   └── ...
│
├── README.md
└── requirements.txt
```

The exact structure may change during development.

## Technologies

The project is developed using Python.

Main libraries:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* scipy

Additional libraries may be added if necessary.

## Expected Outcome

The goal is not only to achieve the highest possible prediction accuracy, but also to understand which football characteristics are useful for predicting match outcomes.

The project will investigate whether simple historical team statistics and engineered features can provide useful predictive information and whether these relationships remain valid across different leagues and seasons.

The final results will include exploratory analysis, hypothesis evaluation, feature engineering, machine learning models and evaluation on unseen data.
