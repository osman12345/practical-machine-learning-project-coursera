# Machine Learning Project with R
This repository contains an R script for running and training multiple models to predict "classe" using a training dataset, and subsequently using the best model to predict outcomes for a test dataset.

```markdown

## Getting Started

To run the script, ensure you have the following R libraries installed:

- `lattice`
- `ggplot2`
- `caret`
- `kernlab`
- `rattle`
- `corrplot`

You can install these libraries using the `install.packages()` function in R.

```r
install.packages(c("lattice", "ggplot2", "caret", "kernlab", "rattle", "corrplot"))
```

## Data

The script assumes the presence of two CSV files:
- [Training dataset](https://d396qusza40orc.cloudfront.net/predmachlearn/pml-training.csv): Training dataset
- `pml-testing.csv`: Test dataset

Ensure these files are placed in the same directory as your R script or provide the correct paths in the script.

## Script Overview

1. **Data Loading and Cleaning:**
   - Loads training and test datasets.
   - Cleans the training dataset by removing columns with mostly NA values, irrelevant metadata, and zero variance variables.

2. **Model Training:**
   - Creates a training and validation set from the training dataset.
   - Trains the following models:
     - Decision Tree
     - Random Forest
     - Gradient Boosting Machine (GBM)
     - Support Vector Machine (SVM) with a linear kernel.

3. **Model Evaluation:**
   - Evaluates each model using cross-validation (CV).
   - Prints confusion matrices and overall accuracy for each model.

4. **Prediction:**
   - Uses the best performing model (Random Forest in this case) to predict "classe" for observations in the test dataset.
   - Prints the predicted outcomes.

## Running the Script

To run the script:
1. Ensure R and the required libraries are installed.
2. Place the script and datasets in the same directory or update file paths accordingly.
3. Execute the script in an R environment.

