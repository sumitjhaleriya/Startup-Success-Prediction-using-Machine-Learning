# Startup-Success-Prediction-using-Machine-Learning

This project uses machine learning to predict the success of startup companies based on various features such as funding, location, industry, and team size. The goal is to help investors and entrepreneurs make more informed decisions about which startups to invest in or launch or the startup will be successfull or not.

## DataSet
The dataset used in this project is sourced from crunchbase.com . It contains information about several thousand startup companies, including their funding history, location, industry, team size, and other relevant features. The dataset requires cleaning and preprocessing to remove missing values and outliers, and to convert categorical variables into numeric ones.

## Machine Learning Models
To predict the success of startups, we tested several machine learning models, including XGBoost Classifier(XBC), AdaBoost Classifier(ABC) , Random Forest Classifier (RFC), and Gradient Boosting Classifier (GBC). For each model, we performed a grid search to find the optimal hyperparameters that maximize the accuracy of the model.

## Results
After testing all the models, we found that Random Forest Classifier (RFC) gave the best accuracy score of 0.85. We also created a scatterplot of the feature importances of each model, which shows that funding and industry are the most important predictors of startup success.

## Running the Code

```bash
To run the code, you'll need to do following steps :

- Import necessary libraries :
  pandas
  numpy
  seaborn
  scikit-learn
  plotly

- Read a CSV file "startup data.csv" and storing the data in the 'dataset' dataframe.

- Rename the 'status' column to 'is_acquired' and changing its values from 'acquired' to '1' and from 'operating' to '0'.

- Create a heatmap to check the correlation between different features of the dataset.

- Remove outliers from the dataset by computing the interquartile range (IQR) and checking if any value falls outside the range of [Q1 - 1.5IQR, Q3 + 1.5IQR]. The values outside this range are considered as outliers.

- Input missing values in numerical features of the dataset using KNNImputer from the scikit-learn library.

- Convert some features from object type to numeric type and deleting unnecessary features.

- Create a correlation matrix and dropping features that have a correlation coefficient less than 0.2 with the target variable 'is_acquired'.

- Code functions such as 'ignore_warn', 'draw_heatmap', 'getOutliersMatrix', and 'imputing_numeric_missing_values' that are used in the main code to perform the mentioned operations.

- Finally, the cleaned and processed dataset is stored in the 'dataset' dataframe.

- Use meta-modeling approach  to combine the predictions of multiple base models to improve the accuracy of the final prediction. The base models used are a XGBoost Classifier(XBC), AdaBoost Classifier(ABC), a Random Forest Classifier (RFC), and a Gradient Boosting Classifier (GBC).

- For each of the base models, a grid search is performed to find the optimal hyperparameters that give the best accuracy score. The hyperparameters that are tuned vary depending on the model, but some common ones include the maximum depth of the tree, the number of estimators, and the learning rate.

- Print The results of each grid search are , and the best estimator is added to a list of the best classifiers. Finally, Define a function to create a scatterplot of the feature importances of each base model using Plotly.


```

## Limitations and Future Research
It's important to note that this analysis has several limitations, such as the potential for bias in the dataset and the limited set of features used to predict success. Future research could explore additional features or data sources to improve the accuracy of the model, as well as validate the model's predictions on real-world data.
