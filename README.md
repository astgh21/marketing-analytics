
# README for Bass Model HW

## Overview
This project implements the **Bass Diffusion Model** to forecast the adoption of a new product based on shipment data from 2013 to 2022. The dataset contains annual shipment values, and we estimate the Bass model parameters \(p\) (coefficient of innovation) and \(q\) (coefficient of imitation) using **Nonlinear Least Squares** (nlsLM) from the `minpack.lm` package in R.

## Files
- **HW1.pdf**: Contains the theoretical background, model fitting, and results for the project.
- **data.xlsx**: This file contains the shipment data from 2013 to 2022, which is used to fit the Bass model.
- **HW1.R**: The R script used to load the data, fit the model, and generate plots showing the number of adoptions over time and cumulative adoptions.
  
## Required R Packages
To run the R script successfully, the following packages are required:
```R
install.packages("readxl")
install.packages("minpack.lm")
install.packages("ggplot2")
install.packages("ggpubr")
```

## Instructions
1. **Download and Load Data**:
   - The shipment data is loaded from the `data.xlsx` file.
   - The R script reads this file using the `readxl` library and prints the data for verification.

2. **Fit the Bass Model**:
   - The `nlsLM` function is used to fit the Bass model. The initial estimates for the parameters \(p\) and \(q\) are set to 0.02 and 0.4, respectively.

3. **Model Summary**:
   - After fitting the model, the summary provides the estimated values for \(p\), \(q\), and diagnostic metrics such as residual error.

4. **Generate Plots**:
   - The script generates two plots:
     - **Number of adoptions at time \(t\)**: Shows the predicted number of new adopters over time.
     - **Cumulative adoptions over time**: Displays the cumulative number of adopters up to time \(t\).

## Results
The model output provides the following information:
- The **estimated parameters** \(p\) and \(q\).
- **Plots** visualizing the adoption curve and the cumulative adoption.

## How to Run
1. Install the required packages.
2. Load the `HW1.R` script in your R environment.
3. Execute the script to see the model summary and plots.
