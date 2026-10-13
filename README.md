# arrs-primary-care-access-analysis
A cross-sectional OLS regression analysis evaluating the impact of the Additional Roles Reimbursement Scheme (ARRS) workforce density on patient-reported primary care access in England using 2023 NHS and GPPS datasets.


# The Additional Roles Reimbursement Scheme and Patient-Reported Access to Primary Care in England: A Cross-Sectional Analysis

## Project Overview
This repository contains the replication data process, syntax, and regression models for my independent research evaluating the Additional Roles Reimbursement Scheme (ARRS) in England. Using cross-sectional data from 1,263 English Primary Care Networks (PCNs) from 2023, the study examines whether variation in multi-disciplinary workforce density is associated with differences in patient-reported access outcomes. 

The analysis reveals no robust independent association between ARRS workforce density and either availability or accommodation metrics. Conversely, GP workforce density emerges as a strong, stable, and consistently positive predictor of patient experiences across all model specifications.

## Methodology and Analytical Approach
The project uses Ordinary Least Squares (OLS) regression models, estimated sequentially across multiple specifications to isolate independent effects and control for underlying differences in demand and socioeconomic context.

### Diagnostic and Robustness Checks:
* **Residual Normality:** Checked using residual Quantile-Quantile (Q-Q) plots and distribution histograms to confirm the underlying assumptions of OLS.
* **Sensitivity Analysis:** Fully adjusted models were re-estimated using alternative 2025 Index of Multiple Deprivation (IMD) scores to verify the stability and consistency of the coefficients.

## Data Sources and Aggregation
To build the analytical dataset, data from four different public administrative and survey datasets were processed, population-weighted, and merged at the PCN level using official NHS Organisation Data Service (ODS) mapping files:
* **GP Patient Survey (GPPS) 2023:** Sourced the dependent variables representing the availability dimension (*Satisfaction with appointment availability*) and accommodation dimension (*Ease of telephone contact*).
* **NHS Primary Care Workforce & General Practice Workforce Datasets (December 2023):** Compiled Full-Time Equivalent (FTE) figures to calculate normalized staffing densities per 10,000 registered patients.
* **NHS Patients Registered at a GP Practice Dataset:** Used to handle registered list sizes and calculate population age structures (the proportion of patients aged 65 and over).
* **OHID National General Practice Profiles:** Extracted practice-level Index of Multiple Deprivation (IMD) indicators to aggregate into population-weighted averages.

## Software and Tools Used
* **Data Management & Visualisation:** Python (pandas, numpy, matplotlib)
* **Statistical Modelling & Regression:** IBM SPSS Statistics (Version 29) 

## Repository Structure
* /notebooks - Code files covering data cleaning, practice-to-PCN aggregation, and exploratory plot generation.
* /models — Regression outputs, descriptive summary matrices, and residual plots.
* README.md — Project summary and layout.
