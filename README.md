# MSCS 634 Lab 2: Classification Using KNN and RNN

## Overview

This repository contains Lab 2 for MSCS 634. The lab applies and compares the K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classification algorithms using the Wine Dataset from the Scikit-learn library.

The Wine Dataset contains 178 observations, 13 numerical input features, and three wine classes.

## Objectives

The objectives of this lab are to:

- Load and explore the Wine Dataset.
- Split the dataset into 80% training data and 20% testing data.
- Implement KNN with multiple values of k.
- Implement RNN with multiple radius values.
- Record and visualize classification accuracy.
- Compare the performance of KNN and RNN.
- Explain how parameter selection affects model performance.

## KNN Parameters

The KNN classifier was tested using:

- k = 1
- k = 5
- k = 11
- k = 15
- k = 21

## RNN Parameters

The RNN classifier was tested using:

- Radius = 350
- Radius = 400
- Radius = 450
- Radius = 500
- Radius = 550
- Radius = 600

## Key Results

The best KNN accuracy was approximately 80.56%, achieved with k = 5. The same accuracy was also observed for several larger k values.

The best RNN accuracy was approximately 72.22%, achieved with a radius of 350. RNN accuracy generally decreased as the radius increased.

Based on the tested parameter values, KNN performed better than RNN on the Wine Dataset.

## Key Insights

- Increasing k from 1 to 5 improved KNN accuracy.
- KNN accuracy remained stable across several larger k values.
- A very small k value can make KNN sensitive to individual observations and noise.
- Increasing the RNN radius introduced observations from different classes into the same neighborhood.
- Large radius values reduced RNN classification accuracy.
- Parameter selection significantly affected model performance.
- KNN was more accurate and stable than RNN for this experiment.

## Challenges and Decisions

One challenge with Radius Neighbors classification is that a test observation may not have any training observations within the selected radius. The model used `outlier_label="most_frequent"` so these observations could be assigned the most frequent training class instead of generating an error.

A stratified train-test split was used to preserve class proportions in the training and testing datasets. A fixed random state was used to make the experiment reproducible.

The original feature values were retained because the assigned RNN radius values of 350 through 600 correspond to the unscaled Wine Dataset. Standardizing the features would change the meaning of these radius values.

## Repository Contents

- `MSCS_634_Lab_2.ipynb` — Complete Jupyter Notebook with code, results, visualizations, observations, and conclusions.
- `README.md` — Summary of the lab purpose, results, insights, challenges, and decisions.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Author

Abhilash Reddy Marthala
