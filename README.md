# Yield Curve Reconstruction using the Cox-Ingersoll-Ross (CIR) Model
## Project Overview

This project was completed as a part of Open Projects 2026 program of Finance Club, IIT Roorkee.

The goal of the project was to build the Treasury yield curve using only the 3-month yield. This involved the implementation, calibration, testing, and extension of the Cox-Ingersoll-Ross (CIR) interest rate model.

## Methodology

The process involves:

1. Data cleaning and preprocessing

2. Yield curve dynamics exploratory analysis

3. CIR model implementation from scratch

4. Calibration of the full training yield curve (cross-sectional)

5. Yield curve reconstruction based on the 3M rate

6. Evaluation on unseen data (out-of-sample)

7. Comparison of CIR model with CIR++ extension

## Repository Structure

data/

    train_data.csv
    
    test_data.csv
    
    test_data_3M.csv


fig/

    generated figures
    

CIR.ipynb


README.md


requirements.txt


## Results

|Model	Out-of-Sample | R²|

|Base CIR | 0.9206|

|CIR++ | 0.8832|

CIR base model met the performance requirement and demonstrated excellent out-of-sample prediction ability with a single latent factor.

## Key Findings

- Traditional MLE calibration was inconsistent due to near-unit-root behavior on short rates.

- Cross-sectional calibration, in this case, produced stable and interpretable parameter estimates.

- The CIR model output both upward and inverted yield curves as part of the model output.

- CIR++ extension improved some of the biases related to maturity but did not enhance out-of-sample performance.

- The correct calibration of structural model parameters was more relevant than model complexity.

## Running the Notebook

1.Install dependencies:

2.pip install -r requirements.txt

3.Open CIR.ipynb and run all cells (there is no need to move any datasets, they are included in the data/ folder in the CIR repository).
