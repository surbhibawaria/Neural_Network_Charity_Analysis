# Neural_Network_Charity_Analysis

## Overview of the Analysis: 

Beks is a data scientist and programmer for the nonprofit foundation, Alphabet Soup. They're a philantropic foundation dedicated to helping organizations that protect the environment, improve people's well-being, and unify the world. Alphabet Soup has raised and donated over 10 billion dollars in the past 20 years. This money has been used to invest in lifesaving technologies and organize reforestation groups around the world. 

Beks is in charge of data collection and analysis for the entire organization. Her job is to analyze the impact of each donation and vet potential recipients. This helps ensure that the foundation's money is being used effectively. Unfortunately, not every donation the company makes is impactful. In some cases an organization will take the money and disappear. As a result, Alphabet Soup's president Andy Glad has asked Beks to predict which organizations are worth donating to and which are too high risk. He wants her to create a mathematical data driven solution that can do this accurately. Beks has decided that this problem is too complex for the statistical and machine learning models she has used. Instead she will design and train a deep learning neural network. This model will evaluate all types of input data and produce a clear decision making result.

### Purpose

The purpose of this analysis is to help Beks learn about neural networks and how to design and train these models using the Python TensorFlow library. Using the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results: 

### Data Preprocessing

- The column 'IS_SUCCESSFUL' is considered the target for the model.

<img width="1012" alt="Screen Shot 2022-05-02 at 3 35 41 PM" src="https://user-images.githubusercontent.com/95826875/166313686-df6eb172-1dc9-4989-a979-66e79b37fcd7.png">

- The columns 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'INCOME_AMT', and 'SPECIAL_CONSIDERATIONS' are considered to be the features for the model.

<img width="1013" alt="Screen Shot 2022-05-02 at 3 35 57 PM" src="https://user-images.githubusercontent.com/95826875/166313741-6879de55-0457-4ecd-8aa9-d8250197c7d0.png">

- The variables 'EIN' and 'Name' are neither targets nor features, and was removed from the data.

<img width="1016" alt="Screen Shot 2022-05-02 at 3 36 16 PM" src="https://user-images.githubusercontent.com/95826875/166313775-18c922ca-a4c6-4035-91fb-78611778064a.png">

### Compiling, Training, and Evaluating the Model

- For the neural model here is made of two layers with 80 and 30 neurons respectively. The activation function used for the hidden layers is 'relu', and 'sigmoid' is used for the output layer.

<img width="1016" alt="Screen Shot 2022-05-02 at 3 45 43 PM" src="https://user-images.githubusercontent.com/95826875/166314973-0940ac57-0edc-4454-8a85-06aab9725cf5.png">

- The target model performance which was supposed to be higher than 75% coul not be achieved. It was able to achieve an acuuraccy of 72.5%.

<img width="490" alt="Screen Shot 2022-05-02 at 3 50 03 PM" src="https://user-images.githubusercontent.com/95826875/166315531-fae5156f-a6cb-4521-b7f3-11bf7299f695.png">

- Steps which were taken to try and increase model performance were:

1. Adding more Neurons to a Hidden Layer.

<img width="925" alt="Screen Shot 2022-05-02 at 3 59 59 PM" src="https://user-images.githubusercontent.com/95826875/166316916-f1e99190-6e2f-4af5-979e-2466b7ba4651.png">

2. Additional hidden layer is added as a third layer.

<img width="915" alt="Screen Shot 2022-05-02 at 3 57 22 PM" src="https://user-images.githubusercontent.com/95826875/166316661-710d9bd8-d3b0-49bc-a798-76b450978e3f.png">

3. The activation function of hidden layers is changed from 'relu' to 'tanh' for optimization.

<img width="916" alt="Screen Shot 2022-05-02 at 3 57 44 PM" src="https://user-images.githubusercontent.com/95826875/166316667-80da30c2-5223-4823-a921-a78f0fcc44b1.png">

4. Adding the number of epochs to the training regimen.

<img width="926" alt="Screen Shot 2022-05-02 at 3 58 05 PM" src="https://user-images.githubusercontent.com/95826875/166316695-1183933d-cafd-439b-b1b7-0431f5fb3d30.png">


## Summary: 

After removing noisy variables from features, ddding more neurons to a hidden layer, adding additional hidden layer, using different activation functions for the hidden layers, and adding the number of epochs to the training regimen the target predictive accuracy higher than 75% could not be achieved, since the model seems to be not outperforming.

#### Recommendation

A random forest classifier could be used instead since the targeted accuracy score was achieved with the neural networks here. Random forest model would perform faster than the neural networks and could have avoided the data from being overfitted.
