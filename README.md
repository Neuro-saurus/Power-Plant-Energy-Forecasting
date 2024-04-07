# Combined Cycle Power Plant Data

## Overview

This report presents a comprehensive analysis conducted on a dataset from a Combined Cycle Power Plant over a six-year operation period (2006-2011), during which the plant was fully loaded. The study focused on utilizing hourly average ambient variables—Temperature (T), Ambient Pressure (AP), Relative Humidity (RH), and Exhaust Vacuum (V)—to predict the plant's net hourly electrical energy output (EP).

### Data Acquisition and Exploration

- **Data Source**: The dataset was obtained from the UCI Machine Learning Repository's [Combined Cycle Power Plant dataset](https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant).
- A thorough initial examination revealed the dataset comprises several rows and columns, representing individual measurements and their corresponding ambient variables.
- Pairwise scatterplots were generated to visualize relationships between all variables, revealing interesting patterns and correlations.
- Descriptive statistics, including mean, median, range, quartiles, and interquartile ranges for each variable, were computed and summarized, providing insights into the data distribution and variability.

### Regression Analysis

- Simple linear regression models were applied to each predictor against the response, identifying statistically significant associations and highlighting potential outliers.
- A multiple regression model incorporating all predictors was then fitted, pinpointing predictors significantly associated with the electrical output.
- Coefficients from both simple and multiple regression models were compared, investigating non-linear associations and the impact of predictor interactions on the response.

### Model Refinement

- Efforts to improve the model included the introduction of interaction terms and exploration of nonlinear associations between predictors and the response. The refined models were trained on a randomly selected 70% subset of the data, incorporating all predictors along with their interactions and quadratic nonlinearities.
- Statistically insignificant variables were pruned based on their p-values, and the models were subsequently tested on the remaining data points. Training and test mean squared errors (MSEs) were reported for both models.

### KNN Regression

- The k-nearest neighbor regression technique was employed, utilizing both normalized and raw features to find the optimal k value that minimized prediction error. The investigation spanned k values from 1 to 100.
- Train and test errors were plotted as a function of 1/k, facilitating the selection of the best k value for the model.

### Comparative Analysis and Conclusions

- A comparison between the KNN Regression model and the linear regression model with the smallest test error was conducted. This comparison offered valuable insights into the strengths and limitations of each modeling approach.
- The analysis confirmed the presence of nonlinear associations between some predictors and the response, as well as statistically significant interactions between certain predictors.

This summary encapsulates the analytical processes undertaken and highlights key findings from the study of the Combined Cycle Power Plant dataset, underscoring the practical applications of statistical and machine learning techniques in predicting energy output based on environmental conditions.
