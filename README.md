# Modeling Urban Crime Risk and Arrest Probability Using Spatio-Temporal Machine Learning Techniques

**Evidence from Chicago (2001–2023)**

This repository contains the code, data pipeline, and paper for a Major Research Paper (MRP) completed at the **Toronto Metropolitan University (TMU)**, School of Data Science and Analytics, under the supervision of **Dr. Xingwei (Nancy) Yang**.

The study develops a machine learning framework to predict **arrest probability** and **crime risk** using Chicago crime records integrated with socio-economic, weather, and CTA (Chicago Transit Authority) mobility data, supporting data-driven public safety decision-making.

## Overview

- **Dataset:** Chicago crime data, 2001–2023 (~7.97M records), merged with socio-economic, weather, and transit mobility features — 27 predictors in total
- **Task:** Binary classification of arrest likelihood following a reported crime
- **Approach:** Spatio-temporal feature engineering combined with 14 machine learning algorithms evaluated across 3 class-balancing strategies (original, random under-sampling, random over-sampling)
- **Best result:** Random Forest with over-sampling — **F1: 0.762, ROC-AUC: 0.912, PR-AUC: 0.855**

## Repository Structure

```
├── 0. Dataset/                          Raw and merged datasets (crime, socio-economic, weather, CTA mobility)
├── 1. Literature Review/                Reference materials and literature synthesis
├── 2. Data_Preprocessing_and_Integration/  Cleaning, merging, and integration of all data sources
├── 3. EDA/                              Exploratory data analysis notebooks
├── 4. EDA_Charts/                       Generated EDA visualizations
├── 5. Feature_Engineering/              Spatio-temporal feature construction and feature selection
├── 6. Experiments/                      Model training and evaluation across algorithms/sampling strategies
├── 7. Results/                          Final results, metrics, and output artifacts
└── MODELING URBAN CRIME RISK AND ARREST PROBABILITY USING SPATIOTEMPORAL
    MACHINE LEARNING TECHNIQUES EVIDENCE FROM CHICAGO.pdf   Full MRP paper
```

## Methodology

1. **Data Integration** — Chicago crime records are merged with socio-economic indicators, weather data, and CTA mobility data to build a spatio-temporally enriched dataset.
2. **Preprocessing & Feature Engineering** — Cleaning, handling of missing values, and construction of spatio-temporal features (e.g., location- and time-based aggregates).
3. **Class Imbalance Handling** — Since arrests are a minority outcome, three sampling strategies were compared: original (imbalanced) data, random under-sampling, and random over-sampling (including SMOTE-based approaches).
4. **Model Training & Evaluation** — 14 algorithms were benchmarked, including Logistic Regression, Random Forest, XGBoost, and LightGBM, evaluated using F1-score, ROC-AUC, and PR-AUC.
5. **Results** — Random Forest with over-sampling was selected as the best-performing configuration.

## Key Results

| Model | Sampling | F1 | ROC-AUC | PR-AUC |
|---|---|---|---|---|
| Random Forest | Over-sampling | **0.762** | **0.912** | **0.855** |

See `7. Results/` and the full paper (PDF) for the complete comparison across all 14 models and 3 sampling strategies.

## Paper

The full write-up — including literature review, methodology, experimental design, results, and discussion — is available in this repository:
[`MODELING URBAN CRIME RISK AND ARREST PROBABILITY USING SPATIOTEMPORAL MACHINE LEARNING TECHNIQUES EVIDENCE FROM CHICAGO.pdf`](./MODELING%20URBAN%20CRIME%20RISK%20AND%20ARREST%20PROBABILITY%20USING%20SPATIOTEMPORAL%20MACHINE%20LEARNING%20TECHNIQUES%20EVIDENCE%20FROM%20CHICAGO.pdf)

The paper is currently under process for publication.

## Author

**Devanshu Prajapati**
M.Sc. Data Science and Analytics, Toronto Metropolitan University
Supervisor: Dr. Xingwei (Nancy) Yang
GitHub: [@Devanshu1013](https://github.com/Devanshu1013)

## Citation

If you use this work, please cite the accompanying paper (see the PDF in this repository for full citation details, pending publication).
