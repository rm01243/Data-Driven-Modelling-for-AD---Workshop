# Data-Driven Modelling for AD Workshop

## Overview
This repository contains a comprehensive, beginner-friendly Jupyter notebook workshop on using Artificial Neural Networks (ANNs) for data-driven modelling of anaerobic digesters (AD) to predict biogas production. The workshop is designed for biogas researchers, AD plant operators, consultants, and sustainability professionals with limited programming or modelling experience. It covers key concepts like data loading, feature selection, preprocessing, building and training ANNs, evaluation, and visualisation—all without requiring local installations, as it runs in Google Colab.

The focus is on predicting biogas production (`q_gas`) from AD parameters using synthetic data inspired by models like ADM1. Topics include ANN fundamentals (types, working principles, activation functions), handling overfitting/underfitting, and practical implementation with Python libraries like TensorFlow/Keras and scikit-learn.

## Features
- **No Installation Needed**: Everything runs in Google Colab (free, browser-based).
- **Hands-On**: Interactive code cells for experimentation (e.g., adjust epochs, neurons, or layers).
- **Reproducible**: Random seeds ensure consistent results.
- **Visualisations**: Plots for feature importance, predictions, and training loss using Matplotlib.
- **Synthetic Data**: `AD_Synthetic_Data.xlsx` included; easily replace with real data.

## Usage
1. **Open in Google Colab**: Click the badge below to launch the notebook directly in Colab—no setup required.
   
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rm01243/Data-Driven-Modelling-for-AD-Workshop/blob/main/AD_ANN_Workshop.ipynb)

2. **Run the Notebook**: Execute cells sequentially (Shift+Enter). Upload or load the data file as prompted.
3. **Experiment**: Modify parameters like `top_n` (features), epochs (50), or neuron counts (e.g., 64/32) and re-run to see impacts.
4. **Data Preparation**: For real data, ensure columns match (e.g., update `features` list). Use full-form names like 'Carbohydrates' for clarity.
5. **Troubleshooting**: Restart runtime if issues arise (Runtime > Restart runtime).

## Notebook Structure
- **Introduction**: Overview of AD and ANNs.
- **Step 1-3**: Libraries, data loading, input/output definition.
- **Step 4**: Feature selection with Mutual Information (includes schematics).
- **Step 5**: Preprocessing (scaling and splitting).
- **Step 6**: Build ANN (feedforward network with ReLU activation; covers working principles, activation functions like Sigmoid/Tanh/ReLU, and why they're essential).
- **Step 7**: Training (50 epochs, monitors overfitting).
- **Step 8**: Predictions and evaluation (R², RMSE; discusses overfitting/underfitting).
- **Step 9**: Visualise results (actual vs. predicted, loss curves).
- **Wrapping Up**: Next steps, including hyperparameter tuning.

## Key Concepts Covered
- **ANN Types**: Feedforward (basic, one-way flow) vs. Recurrent (multi-directional, for sequences like handwriting/language).
- **ANN Workflow**: Random weights → Forward pass (input + weights through layers) → Output → Backpropagation (adjust weights via error comparison).
- **Neurons & Activation**: Neurons learn individually; activations (e.g., ReLU: max(0,x)) add non-linearity. Without them, ANN reduces to linear regression—unable to handle complex data (e.g., images/time-series).
- **Activation Details**:
  - **Sigmoid**: 0-1 output, S-curve; vanishing gradients, slow convergence.
  - **Tanh**: -1 to 1, zero-centred; better than Sigmoid but still vanishing gradients.
  - **ReLU**: Efficient, fast convergence; 'dead neurons' risk (fixed by Leaky ReLU).
  - Output: Linear for regression; Softmax for classification.
- **Overfitting/Underfitting**: Detected via train/test metric gaps; addressed by feature selection, early stopping, or dropout (not implemented here).

## Requirements
- Python 3 (via Colab).
- Libraries: NumPy, Pandas, Matplotlib, scikit-learn, TensorFlow/Keras (all pre-installed in Colab).
- Data: `AD_Synthetic_Data.xlsx` (included in repo).
