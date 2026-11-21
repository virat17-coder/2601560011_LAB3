# Lab Assessment 3: Titanic Survival Analysis

**Student Roll Number:** 2601560011

## Question

Using KNIME, how can Titanic passenger data be prepared and explored to identify factors associated with survival, and how accurately can a decision tree predict whether a passenger survived?

## Overview

This project uses KNIME Analytics Platform to prepare and explore the Titanic passenger dataset, train and evaluate a decision tree, and export the results.

## Dataset

The analysis uses the Titanic passenger dataset with 891 rows and 12 columns.

Source: [Titanic passenger CSV](https://github.com/tcsai/data-mining/blob/master/data/Titanic/titanic.csv)

## Workflow

1. Imported the Titanic CSV into KNIME.
2. Removed the Name, Ticket, and Cabin columns.
3. Replaced missing Age values with the median and missing Embarked values with the most frequent value.
4. Created `SurvivedLabel` with the values Yes and No.
5. Explored survival by sex, age, fare, and passenger class.
6. Split the data into 70% training and 30% test data using stratified sampling with random seed 42.
7. Trained a decision tree using Gini index and five records per node.
8. Applied the model to the test data and evaluated it with a confusion matrix and accuracy.

## Results

- Female average survival rate: **74.2%**
- Male average survival rate: **18.9%**
- Correlation between survival and Pclass: **−0.338**
- Correlation between survival and Fare: **+0.257**
- Test set: **268 passengers**
- Correct predictions: **211**
- Test accuracy: **78.7%**

With 20 records per node, the test accuracy was approximately **79.5%**.

## Insights

- Female passengers had a much higher average survival rate than male passengers.
- Passenger class had a negative correlation with survival, while fare had a positive correlation.
- The fare distribution contains several high-fare outliers.

## Repository Files

- `2601560011_LA3.knwf` — exported KNIME workflow
- `LA3_Report.xlsx` — prepared data, survival-by-sex summary, and tree accuracy
- `Predictions.csv` — decision tree predictions for the test data
- `2601560011_LA3_Report.pdf` — checkpoint screenshots, captions, decision tree rules, and insights

## Running the Workflow

Open the `.knwf` file in KNIME Analytics Platform. If KNIME asks for the CSV location, select the Titanic CSV from the source linked above. Execute the workflow to regenerate the outputs.
