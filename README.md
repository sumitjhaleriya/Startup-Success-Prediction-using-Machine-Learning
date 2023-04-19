# Startup-Success-Prediction-using-Machine-Learning

This project uses machine learning to predict the success of startup companies based on various features such as funding, location, industry, and team size. The goal is to help investors and entrepreneurs make more informed decisions about which startups to invest in or launch or the startup will be successfull or not.

## DataSet
The dataset used in this project is sourced from crunchbase.com . It contains information about several thousand startup companies, including their funding history, location, industry, team size, and other relevant features. The dataset requires cleaning and preprocessing to remove missing values and outliers, and to convert categorical variables into numeric ones.

## Machine Learning Models
To predict the success of startups, we tested several machine learning models, including Decision Tree Classifier (DTC), Support Vector Machine Classifier (SVMC), Extra Trees Classifier (ExtC), Random Forest Classifier (RFC), and Gradient Boosting Classifier (GBC). For each model, we performed a grid search to find the optimal hyperparameters that maximize the accuracy of the model.

## Results
After testing all the models, we found that Random Forest Classifier (RFC) gave the best accuracy score of 0.85. We also created a scatterplot of the feature importances of each model, which shows that funding and industry are the most important predictors of startup success.

## Running the Code
To run the code, you'll need to install the following dependencies:
```bash
pandas
numpy
seaborn
scikit-learn
plotly
```
Once you have the dependencies installed, you can run the code by running the main.py file in your terminal or IDE.

## Limitations and Future Research
It's important to note that this analysis has several limitations, such as the potential for bias in the dataset and the limited set of features used to predict success. Future research could explore additional features or data sources to improve the accuracy of the model, as well as validate the model's predictions on real-world data.
