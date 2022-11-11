# Neural_Network_Charity_Analysis

## Overview

Our job is to help the Alphabet Soup Foundation predict where to invest. Using our knowledge of machine learning and neural networks, we will use the features from the provided dataset to create a binary classifier that can predict whether an applicant will be successful when funded by the Alphabet Soup. We received a CSV file from the Alphabet Soup business team of over 34,000 organizations that have received funding from Alphabet Soup over the years. There are many columns in this dataset that capture metadata about each organization.

## Results 
### Data Preprocessing
- The EIN and NAME columns are identifying information and have been removed from the input data as we do not need them. 

- The IS_SUCCESSFUL column contains binary data related to whether charitable donations are used effectively. Then we considered that variable as the target of our deep learning neural network. 

- The following APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the characteristics of our model. Encoding of categorical variables, splitting of training and testing datasets, and normalization are all applied to features.


### Compiling, Training, and Evaluating the Model
- Our deep learning neural network model consists of two hidden layers with 80 and 30 neurons respectively. The input data has 43 features and the output layer consists of a unique neuron because it is a binary classifier. To speed up the training process, we use a ReLU activation function for the hidden layers. Since our output is binary classification, sigmoid is used in the output layer. For compilation, the optimizer is adam and the loss function is binary_crossentropy. 

- Our model accuracy is under 75% which is not a satisfying performance in the prediction of the outcome of the charity donations.

![Compiling, Training, and Evaluating the Model](https://github.com/Simro25011/Neural_Network_Charity_Analysis/blob/main/Resource/neurons.png)

![Compiling, Training, and Evaluating the Model](https://github.com/Simro25011/Neural_Network_Charity_Analysis/blob/main/Resource/accuracy%20.png)

- We established our accuracy was under the required standard, therefore to improve the performance of the model, we dropped first one more column ORGANIZATION then we increased the number of neurons on the first hidden layer to 100 and then changed the activation function of the second layer from Relu to tanh. None of these steps helped improve the performance of the model.

![Compiling, Training, and Evaluating the Model](https://github.com/Simro25011/Neural_Network_Charity_Analysis/blob/main/Resource/optimization%20neurons.png)

![Compiling, Training, and Evaluating the Model](https://github.com/Simro25011/Neural_Network_Charity_Analysis/blob/main/Resource/accuracy%20optimization.png)

## Summary
The deep learning neural network model fell short of the 75% accuracy goal. Considering that this target level is fairly average, we can say that the model is not performing very well.
Neural networks are prone to overtraining and can be more difficult than a straight forward linear regression model. Therefore, in cases where we have limited training data, or if our dataset has few features, neural networks might be too complicated. In addition, logistic regression models will tend to be simpler to understand and interpret than their neural net counterparts, which puts traditional data scientists and non data experts at ease.


