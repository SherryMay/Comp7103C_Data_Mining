
# Hotel Booking Prediction

This study aims to develop reliable hotel booking estimators, as well as conduct in-depth
demand analysis and predict cancellations.




## Abstract

This project covers data analysis operated by Jupyter Notebook. All files are in the `.ipynb` format, allowing for a mixed visualization of code, figures, and narrative text. To view and run these notebooks, you will need to have *Jupyter Notebook* installed on your system.


Jupyter Notebook : https://jupyter.org/
## Introduction

The analysis is mainly split into two segments, examining both the hotel's perspectives as well
as that of the customers. 

Part A.1 : A general overview of hotel booking trends and the
factors that customers consider when selecting a hotel. 

Part A.2 : Several
appropriate prediction models are determined for predicting hotel booking cancellations and
identifying the variables for customer cancellations. 

Part B : It delivers an analysis of
customers, referring to their characteristics such as nationality, age, family composition, etc.
## Data

Hotel booking demand  

The data is originally from the article Hotel Booking Demand Datasets, written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019.

Data source: https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand
## Install Requirement
```
scikit-learn 
scipy 
pandas
numpy
matplotlib
seaborn
missingno
folium
plotly
sort-dataframeby-monthorweek
xgboost
catboost
lightgbm
jupyter
cufflinks
```
## Note

In PartA.2, All models includes: lr_base, Navie_bayes, Navie_bayes_grid, Ada_model, Ada_grid, xgb_model, xgb_grid, voting_classifier. Then the feature importance of Ada_model is calculated.

Ada_grid is that the soft classifier of Ada_model is changed to Navie_bayes_grid and tuned the hyper-parameters to get Ada_grid with the best parameters. And the code is shown as follows.
ada_model= AdaBoostClassifier( base_estimator=Navie_bayes_grid, random_state = 10)

The voting_classifier is combined by Navie_bayes_grid(wight=0.1), xgb_model(weight=0.8), ada_model(weight=0.9).
This ada_model is the following model:
ada_model= AdaBoostClassifier( base_estimator=Navie_bayes_grid, random_state = 10)

And then the feature importance of Navie_bayes_grid, and xgb_model is calculated.
