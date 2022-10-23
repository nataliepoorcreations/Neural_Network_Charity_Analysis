# Neural_Network_Charity_Analysis

## Overview
With my knowledge of machine learning and neural networks, I used the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. 

## Resources: 
* Data Source: charity_data.csv
* Software: Python 3.9.12, Conda 22.9.0, Pandas, Google Colab

## Results
## Deliverable 1: Preprocessing Data for a Neural Network Model
Using my knowledge of Pandas and the Scikit-Learn’s StandardScaler(), I needed to preprocess the dataset in order to compile, train, and evaluate the neural network model later in Deliverable 2.

* What variable(s) are considered the target(s) for your model?
The target variable for the model was the "IS_SUCCESSFUL" category.


<img width="640" alt="Split our preprocessed data" src="https://user-images.githubusercontent.com/106033535/197420023-2c6d6e49-dfbb-4170-9d08-f3a9c31fdf3b.png">

* What variable(s) are considered the feature(s) for your model?
The original model considered the following columns as features: EIN, NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, IS_SUCCESSFUL.

<img width="1285" alt="one-hot encoded features" src="https://user-images.githubusercontent.com/106033535/197420102-5d6884b8-cb33-4737-98a9-ae445a6708cf.png">

* Drop the EIN and NAME columns.

<img width="477" alt="unique values" src="https://user-images.githubusercontent.com/106033535/197420157-fa83d25d-d820-4619-b736-25a75b342d79.png">


## Deliverable 2: Compile, Train, and Evaluate the Model
Using my knowledge of TensorFlow, I designed a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. I needed to think about how many inputs there are before determining the number of neurons and layers in the model. Once I completed that step, I compiled, trained, and evaluated my binary classification model to calculate the model’s loss and accuracy.

* Create a neural network model by assigning the number of input features and nodes for each layer using Tensorflow Keras.

<img width="925" alt="deep neural net" src="https://user-images.githubusercontent.com/106033535/197420234-adcbbba0-c845-4bda-921f-92b862ae7323.png">


* Evaluate the model using the test data to determine the loss and accuracy.

<img width="629" alt="Evaluate the model" src="https://user-images.githubusercontent.com/106033535/197420255-00c63c9c-0fac-4067-9a71-3d1682af5adc.png">


## Deliverable 3: Optimize the Model 
Using my knowledge of TensorFlow, I optimized the model in order to achieve a target predictive accuracy higher than 75%. 

* Attempt #1: An additional variable was removed from the data set, "SPECIAL_CONSIDERATIONS"

<img width="982" alt="drop special considerations" src="https://user-images.githubusercontent.com/106033535/197420306-83dca7a5-29b6-4d54-8d1f-4b7a38d0a84b.png">

* Attempt #2: Adjusted the amount of neurons and layers. The neurons on the first layer were adjusted to 100, the second layer 50 and an added third layer with 25. The third hidden layer was added with an activation of "relu".

* Attempt #3: The output layer was changed from "sigmoid" to "tanh".

<img width="944" alt="adjustments" src="https://user-images.githubusercontent.com/106033535/197420325-a323cce5-3cdc-48a2-bfb3-95b19f68fce4.png">

## Summary
The deep learning model failed to reach its target accuracy at 75%. The attempts to optimize the model also failed to reach the target of 75%. THe combined attempts to optimize only slightly improved upon the accuracy of the original model, increasing from 72.5% to 72.8%.
