# Using Bayesian modelling to predict default of credit card users

## Project overview:

**I build a simple Bayesian Logistic Regression model in order to help predict whether credit card customers are going to default.**

As will be shown, thresholds can be tilted to create a model that has a high bias of predicting default but very high accuracy on any "non-default" predictions.

The result is a very defensive model that has 90% accuracy on any "non-default" predictions.

We discuss how from a business perspective, the model may be appropriate for scenarios where capacity to onboard new clients is small and the main objective is risk mitigation.

## Table of Contents

0. **Project Statement and Purpose**
1. **Setup and Data Preprocessing**
   - 1.1 Importing modules and data
   - 1.2 One-hot encoding categorical variables
   - 1.3 Standardising the data
   - 1.4 Detecting multicollinearity in continuous variables using VIF (Variance Inflation Factor)
2. **Implementing our Bayesian Logistic Regression Model**
   - 2.1 Model Assumptions
   - 2.2 Splitting data into training and test sets
   - 2.3 Defining the priors & likelihood function distributions
   - 2.4 Running (Markov chain Monte Carlo) MCMC analysis to build the posterior sample
   - 2.5 Posterior Sampling Process Diagnostics
   - 2.6 Adjusting our model to bias towards predicting more defaults
3. **The Bayesian Models Predictions & Results**
   - 3.1 Bayesian Model evaluated on training data
   - 3.2 Bayesian Model evaluated on test data
   - 3.3 Conclusion & summary of results
4. **Acknowledgements**

## Acknowledgements

Dataset taken from Kaggle: https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset

**As per Kaggle acknowledgements, they reference the following:**

- Lichman, M. (2013). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

- The original dataset can be found here at the UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients
