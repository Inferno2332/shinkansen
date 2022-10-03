# shinkansen

The goal of this problem is to predict whether a passenger was satisfied or not, given information on the passengers and the Shinkansen train in which they travelled. We are also given survey data containing passenger feedback on various parameters related to the travel, such as cleanliness or check-in service.

The data had some missing values, which were imputed appropriately, and the columns were scaled to have a mean of 0 and a standard deviation of 1. I tried feature selection with PCA for a while but this led nowhere and actually decreased the accuracy.

Different classification models such as Logistic Regression, Support Vector Machines, k-Nearest Neighbors, Decision Trees, Random Forests, Naive Bayes, Gradient Boosting, and XGBoost were used to train the model. After hyperparameter tuning with cross-validation, the XGBoost model performed the best.

In the end, I decided to combine the top 3 models (XGBoost, Gradient Boosting, Random Forest) and take the most common prediction. The reason for this is that these three models gave similar cross-validation accuracy scores, and would theoretically cancel each others' errors.

I came 3rd in this hackathon with an accuracy of around 0.956.
