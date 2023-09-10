# Starbucks Capstone Challenge: Customer Behavior Analysis

## Table of Contents
1. [Introduction](#introduction)
2. [Objective](#objective)
3. [Methodology](#methodology)
    - [Data Exploration and Understanding](#data-exploration-and-understanding)
    - [Data Preprocessing and Feature Engineering](#data-preprocessing-and-feature-engineering)
    - [Modeling](#modeling)
4. [Model Evaluation and Validation](#model-evaluation-and-validation)
5. [Performance Measure](#performance-measure)
6. [Insights and Conclusions](#insights-and-conclusions)
7. [Licensing](#licensing)
8. [Authors](#authors)
9. [Acknowledgements](#acknowledgements)
10. [Blog Post](#blog-post)

## Introduction <a name="introduction"></a>

The Starbucks Capstone Challenge is a Udacity Data Scientist Nanodegree program project. For this project, Starbucks provided simulated data miming customer behavior on their rewards mobile app.

## Objective <a name="objective"></a>

The primary goal is to combine transaction, demographic, and offer data to determine which demographic groups most respond to different offers. This understanding will enable Starbucks to target its promotions more effectively.

---

## Methodology <a name="methodology"></a>
For this project, I am going to use the CRISP-DM methodology. The Python libraries used are: 

* asttokens==2.2.1
* backcall==0.2.0
* comm==0.1.4
* contourpy==1.1.0
* cycler==0.11.0
* debugpy==1.6.7.post1
* decorator==5.1.1
* executing==1.2.0
* fonttools==4.42.0
* ipykernel==6.25.1
* ipython==8.14.0
* jedi==0.19.0
* joblib==1.3.2
* jupyter_client==8.3.0
* jupyter_core==5.3.1
* kiwisolver==1.4.4
* matplotlib==3.7.2
* matplotlib-inline==0.1.6
* nest-asyncio==1.5.7
* numpy==1.25.2
* packaging==23.1
* pandas==2.0.3
* parso==0.8.3
* pexpect==4.8.0
* pickleshare==0.7.5
* Pillow==10.0.0
* platformdirs==3.10.0
* prompt-toolkit==3.0.39
* psutil==5.9.5
* ptyprocess==0.7.0
* pure-eval==0.2.2
* Pygments==2.16.1
* pyparsing==3.0.9
* python-dateutil==2.8.2
* pytz==2023.3
* pyzmq==25.1.1
* scikit-learn==1.3.0
* scipy==1.11.2
* seaborn==0.12.2
* six==1.16.0
* stack-data==0.6.2
* threadpoolctl==3.2.0
* tornado==6.3.3
* traitlets==5.9.0
* tzdata==2023.3
* wcwidth==0.2.6

### Data Exploration and Understanding <a name="data-exploration-and-understanding"></a>

The initial step involved exploring three primary datasets: `portfolio`, `profile`, and `transcript`. These datasets were analyzed for structure, missing values, and potential features. Data visualizations were also employed to gain initial insights.

### Data Preprocessing and Feature Engineering <a name="data-preprocessing-and-feature-engineering"></a>

Several preprocessing steps were taken:

1. **Handling Missing Values**: Addressed, particularly in the `profile` dataset.
2. **Data Transformation**: Transformed features like `became_member_on` into more informative metrics.
3. **Encoding and Scaling**: Categorical variables were one-hot encoded, and numerical variables were scaled.

### Modeling <a name="modeling"></a>

Initially, a Linear Regression model served as the baseline. Later, advanced models like Random Forest and Gradient Boosting were trained. Hyperparameter tuning was performed on the Gradient Boosting model.

---

## Model Evaluation and Validation <a name="model-evaluation-and-validation"></a>

The final model chosen was the Gradient Boosting Regressor, based on its performance metrics and ability to capture complex data relationships.

### Hyperparameters

The model was optimized using grid search with the following hyperparameters:

- **Number of Estimators**: 100
- **Learning Rate**: 0.1
- **Max Depth**: 3

### Key Features

Significant features include:

- **Customer Income**
- **Membership Duration**
- **Offer Type**

### Qualities of the Model

#### Strengths

1. **Interpretable Results**: Feature importance can be extracted.
2. **High Accuracy**: Achieved a Training RMSE of 17.71 and a Test RMSE of 19.89.
3. **Resilience to Overfitting**: The model generalizes well to new data.

#### Weaknesses

1. **Computationally Intensive**: Can be slow to train.
2. **Hyperparameter Sensitivity**: Performance is highly sensitive to hyperparameter settings.

---

## Performance Measure <a name="performance-measure"></a>

The models were evaluated using the Root Mean Square Error (RMSE) metric. The Gradient Boosting model resulted in a Training RMSE of 17.71 and a Test RMSE of 19.89.

## Insights and Conclusions <a name="insights-and-conclusions"></a>

The model performs well but has room for improvement, which could be achieved through additional feature engineering, algorithm testing, or further hyperparameter tuning.

---

## Licensing <a name="licensing"></a>

This project is licensed under the MIT License.

## Authors <a name="authors"></a>

Fabio Carvalho Lima

## Acknowledgements <a name="acknowledgements"></a>

Special thanks to Udacity for providing the curated data sets used in this project.

---

## Blog Post <a name="blog-post"></a>

For more detailed insights and discussions, read the blog post [here](https://medium.com/@lima.fisico/unlocking-customer-insights-a-data-science-journey-with-starbucks-214d416c0dcc) and jupyter notebook of this project

---
