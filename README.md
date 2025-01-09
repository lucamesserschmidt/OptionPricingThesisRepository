# What are my Options: Comparing Modern Approaches to Derivatives Pricing

This repository contains the code and data for my Bachelor thesis, **"What are my Options: Comparing Modern Approaches to Derivatives Pricing."** The project explores and compares different methods for pricing financial derivatives, specifically American and European call and put options, using analytical and machine learning-based approaches.

---

## Table of Contents

- [Overview](#overview)
- [Files and Structure](#files-and-structure)
- [Usage](#usage)
- [Data Description](#data-description)
- [Results](#results)
- [Acknowledgments](#acknowledgments)

---

## Overview

The project combines traditional financial modeling (e.g., the binomial tree model) with modern machine learning approaches to analyze and price derivatives. The key objectives are:
- To implement and evaluate traditional pricing models.
- To develop machine learning models for pricing options.
- To compare the results of different methods and evaluate their performance.

---

## Files and Structure

### Main Files

- **`binomial_model.py`**: Implements a binomial tree model for pricing call and put options.
- **`machine_learning_models.py`**: Trains various machine learning models (e.g., SVR, Random Forest, XGBoost, LightGBM, MLP) to predict option prices.
- **`OptionsAmerican.csv`**: Example dataset for American options used in the binomial tree model.

### Outputs
- Results for model performance are stored in Excel files: `<DatasetName>_results_with_best_params.xlsx`.
- Learning curves are generated as plots for each model and dataset combination.

---

## Usage

### 1. Binomial Model
Run the binomial model script:

```bash
python binomial_model.py
```

This will:

- Load and clean the `OptionsAmerican.csv` dataset.
- Compute the theoretical call and put option prices.
- Evaluate deviations between calculated and actual prices.

### 2. Machine Learning Models
Run the machine learning script:

```bash
python machine_learning_models.py
```

This will:

- Load datasets for American and European options.
- Train multiple machine learning models with hyperparameter tuning.
- Generate learning curves and save performance metrics in Excel files.

---

## Data Description

The datasets consist of the following columns:

- **Volatility**: Historical volatility of the underlying asset (Here I used the 3 year historical volatility).
- **Risk free rate**: Annualized risk-free interest rate (I used treasury rates from the corresponding country).
- **Underlying Price**: Current price of the underlying asset.
- **Strike Price**: Strike price of the option.
- **In Years**: Time to maturity in years.
- **Settle C**: Observed market price of the call option.
- **Settle P**: Observed market price of the put option.

### Example Data Row

| Volatility | Risk free rate | Underlying Price | Strike Price | In Years | Settle C | Settle P |
|------------|----------------|-------------------|--------------|----------|----------|----------|
| 0.3739     | 0.03288        | 27.44            | 16           | 0.077    | 11.49    | 10.32    |

---

## Results

### Binomial Model
- Calculated prices for American call and put options.
- Compared theoretical prices to market-settled prices.

### Machine Learning Models
- Evaluated **RMSE**, **MAE**, and **R²** scores for various machine learning models across multiple datasets.
- Performance metrics and optimal hyperparameters are saved in `"<DatasetName>_results_with_best_params.xlsx"`.

---

## Acknowledgments

The datasets and the structure of this project were inspired by research into financial derivatives pricing models.

Special thanks to the supervisor who guided this project.

---

### Questions or Suggestions?
Feel free to open an issue or submit a pull request if you have any questions or suggestions!


