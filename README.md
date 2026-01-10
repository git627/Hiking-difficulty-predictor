# Hiking-difficulty-predictor
A machine learning-based approach to predicting the difficulty of hiking trails

## Purpose
Hiking is a pastime enjoyed by millions of people around the world, including myself. There is a huge variety of trails in terms of length, terrain, and scenery. Naturally, there is also a variety of difficulties, ranging from beginner-friendly to extremely strenuous. Additionally, there can be many contributors to the difficulty of hike, including length, elevation gain, and various forms of obstacles. This project seeks to develop a machine learning-based approach to predict the difficulty of hiking trails based on publicly-available information. The performance of the resulting model is compared against conventional predictors[^1] of hiking trail difficulty, and the relative importance of input features is analyzed.

## Datasets
The Georgia hiking trails .csv file contains information about the top 100 rated hiking trails in the U.S. state of Georgia according to alltrails.com. Recorded information includes rank, name, length, elevation gain, and obstacles (rocky, scramble, no shade, slippery, stairs, muddy, and roots). Additionally, user difficulty ratings are provided by count according to four difficulties: easy, moderate, hard, and strenuous. These ratings are used to create the composite difficulty scores that serve as the target values for this project.

The hiking_trails directory contains files corresponding to the elevation profile for individual hiking trails. Files are named according to the corresponding trail. Each file contains the latitude coordinates, longitude coordinates, and raw elevation in meters for the trail.

Other files (hiking1.csv, hiking2.csv, etc.) are files that are created as the Jupyter notebooks are completed and thus are not required to start with if the user intends to complete the notebooks in order. However, they are provided for convenience if the user does not wish to start at the beginning.

## Notebooks
There are four Jupyter notebooks used in this project:
1. hiking1_EDA.ipynb: this notebook performs exploratory data analysis on the hiking trails found in Georgia hiking trails.csv and is used to inform preliminary feature selection.
2. hiking2_max_grade.ipynb: this notebook generates a maximum grade feature by examining elevation profiles and adds this feature to the dataset.
3. hiking3_tsfresh.ipynb: this notebook generates new features based on the sequential elevation profiles and uses principal component analysis (PCA) to capture the most important information. A train/test split is performed on the dataset.
4. hiking4_modeling.ipynb: this notebook trains an xgboost model on the training data and evaluates its performance over the testing data. Feature importance is analyzed and model performance is compared against conventional approaches.

[^1]:Troy, Maridy McNeff; Phipps, Maurice (2010). "The validity of Petzoldt's Energy Mile theory".
