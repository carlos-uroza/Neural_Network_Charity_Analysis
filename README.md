# Module 19 Challenge - Neural_Network_Charity_Analysis

## Overview of the Project

### Purpose
The purpose of this project is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Our client, Beks, has requested a machine learning model that can process a dataset of metadata for more than 34,000 organizations that have previously recieved funding in order to determine where the foundation should investment.

## Results

### Deliverable 1 - Preprocessing Data for a Neural Network Model

-What variable(s) are considered the target(s) for your model?

The target variable for our model is the enconded "IS_SUCCESSFUL" column. This column contains a boolean value denoting whether the applicant was success after recieving funding from Alphabet Soup.

-What variable(s) are considered to be the features for your model?

All of the other columns besides the "IS_SUCCESSFUL" column in our final application_df DataFrame are considered to be features in our model.

-What variable(s) are neither targets nor features, and should be removed from the input data?

The columns containing non-beneficial ID data, such as the "EIN" and "NAME" columns, are considered to be neither target variables nor features. These columns were dropped from the final application_df DataFrame for our analysis.

### Deliverable 2 - Compile, Train, and Evaluate the Model

-How many neurons, layers, and activation functions did you select for your neural network model, and why?

Our model was initially trained using 2 hidden layers. The first hidden layer contains 80 neurons and uses a "relu" activation function. The second hidden layer contains 30 neurons and also uses a "relu" activation function. Finally, our output layer contains 1 neuron and uses a "sigmoid" activation function. The sigmoid activation function in the final layer will ouput binary classification predictions from our model. The first layer uses 80 neurons in order to account for the 44 separate features in our model. This model uses two layers in order to capture the interactions between the many features accross a large dataset of 34,000 observations.

### Deliverable 3 - Optimize the Model

-Were you able to achieve the target model performance?

Our program made three attempts at restructuring the model to achieve the target model performance of over 75%. However, our model was unable to achieve the target model performance. The most accurate model generated had a accuracy score of 72.85% and a loss metric of 0.5578

-What steps did you take to try and increase model performance?

Our first model attempt made use of the same number of hidden layers and neurons as our original model, however uses different activation functions. This model used a "softmax" and "tanh" functions in the first and second layers respectively. The model achieved a accuracy score of 72.52% with a loss metric of 0.5662

![Optimization1](https://user-images.githubusercontent.com/103288980/192647921-38ce9a84-7aab-4e80-98d7-c34bcb10f749.PNG)

Our second model attempt also made use of the same number of hidden layers, neurons, and activation functions as our original model. However, this model uses the "SGD" optimizer instead of the "Adam" optimizer used the other models. The model achieved a accuracy score of 72.48% with a loss metric of 0.5603

![Optimization2](https://user-images.githubusercontent.com/103288980/192647939-1a47b831-664f-4a58-b348-ecdf8afc7f67.PNG)

Our third model attempt changes the structure of the original model. This model uses three hidden layers with 90 neurons in the first layer, 45 neurons in the second layer, and 10 neurons in the third layer. The model uses the "selu" activation function throughout all three hidden layers, the "sigmoid" function in the output layer, and the "Adam" optimizer. The model achieved a accuracy score of 72.85% with a loss metric of 0.5578

![Optimization3](https://user-images.githubusercontent.com/103288980/192647948-8b94b853-fb9f-439e-9db7-25d222070886.PNG)

## Summary
In summary, our top deep learning model resulted in an accuracy score of 72.85% with a loss metric of 0.5578. This represents a marginal improvement over the original model and would suggest additional analysis is required. 

### Recommendations
It is our recommendation the model would benefit from further feature engineering. Particularly testing the individual features for independence, outliers, and importance to the model. By reducing or eliminating additional features, we may be able to produce the largest improvements to our deep learning model.
