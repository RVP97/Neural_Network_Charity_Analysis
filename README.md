# Neural Network Charity Analysis

## Overview

Using neural networks, this projects attempts to analyze the success of a funded company based on several variables. This will help make better decisions as to which companies to fund. This project utilizes data from more than 34,000 organizations, their respective variables and if it was successful or not with the funding.

## Results

**What variable(s) are considered the target(s) for your model?**

- There is only one target in our model, whose name is "IS_SUCCESSFUL".

**What variable(s) are considered to be the features for your model?**

- There are several features for the model: "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT".

**What variable(s) are neither targets nor features, and should be removed from the input data?**

- There are only two: "EIN","NAME"

**How many neurons, layers, and activation functions did you select for your neural network model, and why?**

- I selected 5 layers, including the output layer. The first layer has 60 neurons, the next 50, and such until it got to 30 for the fourth layer. The first trial had way more neurons due to the rule of thumb of three time as many neurons as inputs but it did not outperform so the number of neurons were lowered. The first two layers used the relu activation function while the last two the tanh, while the last one, the output layer, used the sigmoid function because of the binary classification type. I thought the relu and tanh activation function would perform well given the non linear relation of the data and its complexity.

**Were you able to achieve the target model performance?**

- I was not able to increase to significantly increase the performance. While the original model had an accuracy of .7262 and a loss of .5527, mine had an accuracy of .7264 and a loss of .5545.

**What steps did you take to try and increase model performance?**

- I tried to forgo the "ASK_AMT" since it was not giving anything to the model. I tried to decrease the cutoff fot the "other" bins but it was not successful so I did not put it in the final model. I increased the number of neurons, increased the number of hidden layers and epochs, and changed the activation function.

## Summary

The results were a bit disappointing since the model only had an accuracy of .7264, which is less than ideal in such scenario and would likely not be approved to be used. I had hoped to get better results when I changed different parameters of the model but the results remained practically the same. In the future, I would try to use a machine learning model to get better accuracy. The random forest model could work for this and get a better results. I would not use a linear function since the results of that would be extremely bad.
