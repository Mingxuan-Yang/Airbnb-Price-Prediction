# Airbnb Price Prediction

*Project Date: 2020-11-19*

## Introduction

This is a [Kaggle competition](https://www.kaggle.com/c/duke-cs671-fall20-airbnb-pricing-data/overview) project to apply machine learning methods to predict the prices of Airbnb listing places in Buenos Aires, the capital and largest city of Argentina. The price in the Kaggle dataset has been divided into 4 categories, from the cheapest to the most expensive labelled as 1 to 4. Thus the price prediction problem in this project is a multiclass classification problem instead of a regression problem. Therefore, accuracy is used as a model evaluation method.

## Contents

This project contains three major components:

- [Airbnb-Price-Prediction.ipynb](./Airbnb-Price-Prediction.ipynb): The Python codes of this project, including exploratory data analysis and model construction.
- [Data](./Data): The project datasets.
    - [train.csv](./Data/train.csv): The training dataset, containing 24 predictors and the outcome variable `price`.
    - [test.csv](./Data/test.csv): The testing dataset, containing 24 predictors.
    - [sample_submission.csv](./Data/sample_submission.csv): The submission sample of Kaggle competition.
    - [neighbourhood.xlsx](./Data/neighbourhood.xlsx): The external dataset about detailed information such as area, population and number of communes about each neighborhood of Buenos Aires.
- [Report.pdf](./Report.pdf): The detailed report of this project.

## Model

### Variable

The detailed variable selection process can be obtained at the [project report](./Report.pdf). Since the original Kaggle dataset doesn't provide variable description, the following variables don't have any explanation as well. The selected variables are shown below.

- `room_type`
- `host_is_superhost`
- `instant_bookable`
- `required_guest_profile_picture`
- `required_guest_phone_verification`
- `minimum_nights`
- `number_of_reviews`
- `reviews_per_month`
- `calculated_host_listings_count`
- `availability_365`
- `bathrooms`
- `bedrooms`
- `beds`
- `cleaning_fee`
- `guests_included`
- `extra_people`
- `maximum_nights`
- `cancellation_policy`
- `density`
- `Commune`
- `host_duration`

### Model

The model selection procedure can be accessed through the [project report](./Report.pdf). The resulting classification models are

- Light Gradient Boosting Machine
- Random Forest Classifier

## Results

The final results of Light Gradient Boosting Machine and Random Forest Classifier are

|Model|CV Accuracy|Test Accuracy|
|:---:|:---------:|:-----------:|
|Light GBM|0.542|0.553|
|RF|0.554|0.596|