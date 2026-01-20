# Assignment 1 – Learning Probability Density Function

## About This Repository
This repository contains my solution for **Assignment 1**, where I learned how to:
1. Apply a roll-number–based non-linear transformation on real data
2. Learn the parameters of a probability density function (PDF)

The solution is implemented using **Python** in **Google Colab**.

---

## Student Details
- **Name**: Yash Sidana  
- **Roll Number**: 102313063  

---

## Dataset Used
- **Dataset Name**: India Air Quality Data
- **Source**: Kaggle  
- **Link**: https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data
- **Feature Used**: NO2 (Nitrogen Dioxide)

Only the NO2 column is used in this assignment.

---

## Methodology

### Step 1: Data Loading and Cleaning
- The dataset is loaded from `data.csv`
- Column names are cleaned
- The NO2 column is selected
- Non-numeric and missing values are removed

---

### Step 2: Roll Number Based Transformation
Each value `x` (NO2) is transformed into `z` using:

z = x + aᵣ sin(bᵣ x)

where:
- aᵣ = 0.05 × (r mod 7)
- bᵣ = 0.3 × (r mod 5 + 1)
- r is the roll number

This step introduces non-linearity into the data.

---

### Step 3: Learning the PDF Parameters
The transformed variable `z` is modeled using:

p̂(z) = c · exp(−λ (z − μ)²)

The parameters are learned using mean and variance:
- μ = mean of z
- λ = 1 / (2σ²)
- c = √(λ / π)

---

## Comparing Two Roll Numbers
The code compares **two different roll numbers** to show that:
- Different roll numbers give different `aᵣ` and `bᵣ`
- This results in different values of μ, λ, and c

---

## Results
The learned parameters (μ, λ, c) are printed in the notebook output.
A PDF graph is also plotted in the Colab notebook.

---

e
