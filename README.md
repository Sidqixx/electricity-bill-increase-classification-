# Household Electricity Bill Increase Classification

Machine learning classification project that investigates household
electricity billing behavior using primary survey data collected from
households.

The project aims to identify households experiencing increases in
electricity bills while exploring household characteristics, appliance
usage, and behavioral factors associated with the classification target.

## Project Overview

Household electricity billing behavior can be influenced by various
factors, including appliance usage, household characteristics, and
daily energy-related behavior.

This project applies machine learning classification techniques to
identify households experiencing an increase in electricity bills based
on household survey data.

The original research project evaluated five classification models:

- Logistic Regression
- Naive Bayes
- K-Nearest Neighbors (K-NN)
- Multi-Layer Perceptron (MLP)
- Support Vector Machine (SVM)

This repository presents the author's contribution, focusing on:

- Data preprocessing
- K-NN classification
- MLP classification

---

## Objectives

The project aims to:

1. Prepare household electricity survey data for machine learning.
2. Classify households based on electricity billing behavior.
3. Evaluate different machine learning classification approaches.
4. Investigate household, appliance, and behavioral factors associated
   with electricity billing increases.

---

## Dataset

### Data Source

Primary household electricity survey data collected as part of the
research project.

### Dataset Size

- **306** survey responses collected
- **286** records in the final processed dataset

### Target Variable

The target variable represents household electricity billing behavior:

| Value | Meaning |
|---:|---|
| 0 | No Increase |
| 1 | Increase |

The target was constructed from the survey response regarding changes
in monthly electricity billing.

---

## Methodology

The overall workflow consists of:

```text
Household Survey Data
        ↓
Data Cleaning
        ↓
Categorical Variable Mapping
        ↓
Feature Preparation
        ↓
Target Construction
        ↓
Train-Test Split
        ↓
SMOTE on Training Data
        ↓
Machine Learning Classification
        ↓
Model Evaluation
```

### Data Preprocessing

The preprocessing stage includes:

- Data cleaning
- Removal of unsuitable variables
- Categorical response mapping
- Missing-value handling
- Feature preparation
- Binary target construction
- Final feature matrix preparation

The preprocessing workflow produces the final dataset containing
**286 records**, which is used as input for the classification
experiments.

### Class Imbalance Handling

SMOTE (Synthetic Minority Over-sampling Technique) was applied to the
training data to address class imbalance.

The test set was kept separate from the oversampling process.

### Model Development

The original research project evaluated five classification models:

- Logistic Regression
- Naive Bayes
- K-NN
- MLP
- SVM

This repository contains the implementation of K-NN and MLP as part of
the author's personal contribution.

---

## Personal Contribution

**Role:** Research Intern  
**Organization:** BINUS University  
**Team:** 3 Members

The author's contribution consisted of three main areas.

### Data Preprocessing

Prepared the household survey data for machine learning through data
cleaning, categorical mapping, missing-value handling, target
construction, and feature preparation.

### K-NN Classification

Implemented and evaluated K-Nearest Neighbors classification experiments
using the processed household survey dataset.

### MLP Classification

Implemented and evaluated Multi-Layer Perceptron classification
experiments across multiple hidden-layer configurations.

---

## Model Evaluation

The classification models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score

F1-score was considered alongside the other metrics because the dataset
contains class imbalance.

### K-NN Experiments

Multiple K values were evaluated to examine their effect on
classification performance.

| K | Accuracy | Precision | Recall | F1-Score |
|---:|---:|---:|---:|---:|
| 3 | 0.50 | 0.47 | 0.46 | 0.44 |
| 5 | **0.53** | **0.49** | **0.48** | **0.46** |
| 7 | **0.53** | **0.49** | **0.48** | 0.456 |
| 9 | 0.52 | 0.48 | 0.47 | 0.45 |

The tested K values produced relatively similar performance. The K=5
configuration achieved an F1-score of 0.46.

### MLP Experiments

Multiple hidden-layer configurations were evaluated.

| Hidden Layer Configuration | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| (16) | 0.55 | 0.45 | 0.44 | 0.44 |
| (32) | 0.52 | 0.52 | 0.52 | 0.52 |
| (32, 8) | 0.62 | 0.53 | 0.54 | 0.53 |
| **(32, 16)** | **0.71** | **0.57** | **0.56** | **0.57** |
| (32, 32) | 0.59 | 0.47 | 0.46 | 0.46 |
| (64, 32) | 0.59 | 0.49 | 0.49 | 0.48 |
| (64, 32, 16) | 0.62 | 0.42 | 0.43 | 0.42 |

The MLP configuration with hidden layers **(32, 16)** achieved the
highest reported performance in the experiment, with **0.71 accuracy**
and an **F1-score of 0.57**.

---

## Overall Model Comparison

The original research project compared five classification models.

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 0.66 | 0.55 | 0.56 | 0.55 |
| Naive Bayes | 0.69 | 0.50 | 0.50 | 0.50 |
| K-NN | 0.53 | 0.49 | 0.48 | 0.46 |
| MLP | 0.71 | 0.57 | 0.56 | 0.57 |
| SVM | 0.69 | 0.50 | 0.50 | 0.49 |

> The overall comparison represents the team's experiment. This
> repository specifically contains the author's preprocessing, K-NN,
> and MLP work.

---

## Key Findings

- The tested K-NN configurations showed relatively small variations in
  classification performance.
- The MLP configuration with hidden layers **(32, 16)** achieved the
  highest reported performance among the evaluated configurations,
  with **71% accuracy** and **0.57 F1-score**.
- SMOTE was applied to address class imbalance during model training.
- Household appliance usage, behavioral patterns, and residential
  characteristics were investigated as potential factors associated
  with electricity billing behavior.

---

## Feature Analysis

Feature analysis conducted during the research identified several
household, appliance, behavioral, and residential variables associated
with the classification target.

Examples include:

- Washing Machine
- Electric Vehicle
- Electric Dispenser
- Living Temperature
- TV
- Washing Machine Usage Frequency
- Charger Unplugging Behavior
- Kitchen Light Usage Behavior
- Bathroom Light Duration
- Type of Residence
- Desktop Computer

These variables were explored as potential factors related to household
electricity billing behavior.

---

## Repository Structure

```text
electricity-bill-increase-classification/
│
├── README.md
│
├── notebooks/
│   ├── 01_preprocessing.ipynb
│   ├── 02_knn_classification.ipynb
│   └── 03_mlp_classification.ipynb
│
├── data/
│   ├── raw_household_survey.csv
│   └── processed_household_survey.csv
│
├── requirements.txt
│
└── .gitignore
```

---

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Research Context

This project was conducted as part of a 3-member research project at
BINUS University.

The original research included a research paper and experiments
covering five machine learning classification models.

This repository presents the author's individual contribution to the
research work, specifically:

- Data preprocessing
- K-NN classification
- MLP classification

The research paper is not included in this repository.

---

## Limitations

- The dataset consists of **286 processed household survey records**.
- The data was collected through a primary household survey and may
  not represent the broader population.
- The target represents electricity **billing behavior**, rather than
  direct electricity consumption measured in kWh.
- Model performance may be affected by the relatively limited dataset
  size and class distribution.
- The project was developed as an academic/research experiment and was
  not deployed as a production prediction system.

---

## Disclaimer

This project is an academic/research machine learning experiment.
The results should not be interpreted as a production-grade electricity
consumption or billing prediction system.
