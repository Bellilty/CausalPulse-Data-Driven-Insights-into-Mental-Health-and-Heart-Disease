# CausalPulse: Data-Driven Insights into Mental Health and Heart Disease

**CausalPulse** is a data science project applying causal inference techniques to investigate the relationships between mental health, heart disease, and the impact of music on mental well-being. This project leverages advanced statistical methods and machine learning to draw insights and explore causality in health-related datasets.

## Table of Contents
- [Introduction](#introduction)
- [Project Objectives](#project-objectives)
- [Features](#features)
- [Datasets](#datasets)
- [Methodology](#methodology)
- [Results](#results)
- [Setup and Usage](#setup-and-usage)
- [Files in the Repository](#files-in-the-repository)
- [Authors](#authors)

## Introduction
Mental health plays a crucial role in overall well-being and has been associated with heart disease risk. This two-part project investigates:
1. Whether maintaining good mental health reduces the risk of heart disease.
2. Whether music listening habits causally impact mental health.

Through statistical modeling, causal inference, and machine learning, the project evaluates these questions using real-world datasets.

## Project Objectives
1. Establish causality between mental health and heart disease while identifying confounders like sleep and physical activity.
2. Investigate the causal impact of music listening habits on mental health, exploring potential mediators and moderators.

## Features
- Exploratory Data Analysis (EDA) to understand data distributions and relationships.
- Preprocessing pipelines for cleaning and feature engineering.
- Implementation of causal inference techniques:
  - Matching
  - Propensity Score Stratification
  - T-learner, S-learner, and K-means Stratification
  - Marginal Causal Curve and TMLE
- Statistical validation of results with confidence intervals.

## Datasets
### Heart Disease Dataset
- Source: [Kaggle - Personal Key Indicators of Heart Disease](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
- Key features:
  - `Heart Disease`: Binary indicator for CHD or MI.
  - `Mental Health`: Self-reported days with poor mental health in the last 30 days.
  - Confounders: `Physical Activity`, `Sleep Time`, `BMI`, `Age`, `Sex`.

### Music and Mental Health Dataset
- Source: [Kaggle - MXMH Survey Results](https://www.kaggle.com/datasets/catherinerasgaitis/mxmh-survey-results)
- Key features:
  - `Hours per Day`: Music listening time.
  - Mental health indicators: `Anxiety`, `Depression`, `Insomnia`, `OCD`.
  - Confounders: `Age`, `Instrumentalist`, `Exploratory`.

## Methodology
1. **Causal Inference Analysis**:
   - Develop a causal graph identifying confounders and instrumental variables.
   - Use logistic regression and other models to estimate treatment effects.
   - Validation through sensitivity analysis and placebo tests.

2. **Machine Learning for Mental Health**:
   - Build regression models for mental health outcomes.
   - Use TMLE and marginal causal curves for robust estimation.

3. **Music Analysis**:
   - Explore U-shaped and linear relationships between music habits and mental health outcomes.
   - Visualize and interpret marginal causal curves for music listening time.

## Results
- Mental health positively impacts heart health, with good mental health reducing heart disease risk by ~8% based on various methods.
- Music listening habits influence mental health metrics like insomnia and OCD, with longer music listening hours associated with mixed effects.
- Validation checks confirm robustness of results under different model assumptions.

## Setup and Usage
### Requirements
Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Running the Code
1. Analyze heart disease and mental health:
   ```bash
   jupyter notebook Part_1_heart_2020_cleaned.ipynb
   ```
2. Analyze music and mental health:
   ```bash
   jupyter notebook Part_2_mxmh_survey_results.ipynb
   ```

## Files in the Repository
- **`heart_2020_cleaned.csv`**: Dataset for heart disease and mental health analysis.
- **`mxmh_survey_results.csv`**: Dataset for music and mental health analysis.
- **`Part_1_heart_2020_cleaned.ipynb`**: Notebook analyzing heart disease and mental health.
- **`Part_2_mxmh_survey_results.ipynb`**: Notebook analyzing music and mental health.
- **`CausalPulse.pdf`**: Comprehensive project report detailing methods, challenges, and findings.

## Authors
- **Ruben Sasson** (ID: 342602281)
- **Raphael Cohen** (ID: 345237721)
- **Simon Bellilty** (ID: 345233563)

## Acknowledgments
- [Kaggle](https://www.kaggle.com) for datasets.
- [Scikit-learn Documentation](https://scikit-learn.org/stable/) for regression models.
- [Scientific Literature](https://www.ncbi.nlm.nih.gov/) for supporting research articles.

