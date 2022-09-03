# Neural Network Charity Analysis
## Overview

The purpose of the analysis is to use charity_data dataset and apply the knowedge in the field of machine learning and neural networks. We are using the dataset features to create a binary classifier capable of predicting whether applicant organizations would be successful if funded by the Alphabet Soup Foundation. The dataset contains over 34,000 organizations that have received funding from Alphabet Soup over the years.


## Results



### Data Preprocessing

- What variable(s) are considered the target(s) for your model?

One of the columns in the dataset called "IS_SUCCESSFUL" is the target of the model. The column displays the number "1" or "0" indicating "yes" or "no" regarding the probability that the organization will be successful if funded by the Alphabet Soup Foundation.


![1](https://user-images.githubusercontent.com/66500222/188254999-f342fb2e-6aa5-4832-9424-4fb1e4713e1d.png)

- What variable(s) are considered to be the features for your model?


![2](https://user-images.githubusercontent.com/66500222/188255283-31eeb9b5-9c8c-4596-a535-954cbe6d31fc.png)

- What variable(s) are neither targets nor features, and should be removed from the input data?

Two columns were removed from the model, 'EIN' and 'NAME' because the information they provided is not essential for predicting success of future funding.

![3](https://user-images.githubusercontent.com/66500222/188255344-ac6d9757-bab0-43f3-876b-0b4b9cb3fb40.png)


### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

This model consists of two stages of compilation, training and evaluation. At the first stage, two hidden layers and one outer layer were used. The neurons were arranged 80 in the first layer, 30 in the second layer, and 1 in the third layer. At the first stage, three activation functions were used: "relu", "sigmoidal" and "linear". Training epochs have been set to 10.

![4](https://user-images.githubusercontent.com/66500222/188255467-d88be7e9-dbbd-4631-bfa2-2889e998641f.png)

- Were you able to achieve the target model performance?

I was not able to achieve the target model preformance in the first phase. The highest accuracy evaluated by the model was 0.4668

![6](https://user-images.githubusercontent.com/66500222/188255652-cea86b00-fffc-4b8a-bca7-725e5d2ffc3b.jpg)


- What steps have you taken to try and improve the performance of the model?

In the second step, I tried to optimize the model by adding hidden layers, decreasing the number of neurons, increasing the epochs, and using the same activation function for each model layer. I managed to increase the performance of the model to 0.7235, but only once, which I considered an anomaly. 

![5](https://user-images.githubusercontent.com/66500222/188255864-e0b5beae-d221-41d7-b3a9-281064db6511.png)



## Summary



The dataset was read into a Jupyter Notebook environment using an mlenv type file, where it was pre-processed using density plots to visualize the number of target variable values, fitting and transformation was performed on a list of variables using OneHotEncoder, and the processed data was split into features and target arrays, and then again split into a dataset for training and testing. A Scikit_Learn StandardScaler was instantiated, data scaled, compiled, trained and tested for use in a neural network. The data was trained with a sequential neural network model, and various number of layers, various number of nodes, and several activation functions were applied to the dataset throughout the analysis to predict reliability and evaluate the model at the highest level of optimization.
