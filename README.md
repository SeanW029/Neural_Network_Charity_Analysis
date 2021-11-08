# Neural_Network_Charity_Analysis

## Overview of Project

To create a deep-learning neural network to analyze the success of charitable donations using Python, Pandas Jupyter notebook and TensorFlow.

## Steps of analysis

1.Preprocess data for a Neural Network model.
2.Compile, Train and Evaluate the model.
3.Optimize the model to achieve a target predictive accuracy higher than 75%.


## Results

Target and feature variables were identified. Columns EIN and NAME were removed, a density plot was created to determine binning and using one-hot encoding to encode the categorical variables before placing it in a new dataframe. The one-hot encoding dataframe was merged to the original dataframe and the original values were dropped.

![image](https://user-images.githubusercontent.com/83438418/140686658-2d4a2e80-60bc-47f7-9499-9418840a4d5a.png)

A neural network was then created with two hidden layers using TensorFlow.

![image](https://user-images.githubusercontent.com/83438418/140686901-e3b5167f-57d5-48ee-b4fd-d4d0fefe8276.png)

The model was compiled and trained with 100 epochs; the accuracy test result was 72.5%.

![image](https://user-images.githubusercontent.com/83438418/140686957-3f67717f-2f91-416b-a857-7dc1fe4ed7e7.png)

Optimizing the model to achieve a higher than 75% target predictive accuracy.

1st optimization - a third hidden layer with 30 nodes was added with the same number of epochs giving us 72.6% accuracy, not a siginificant improvement.

![image](https://user-images.githubusercontent.com/83438418/140687172-ee6599bc-35eb-41e7-badc-50b249006515.png)

2nd optimization – using same set up as the 1st try and changing the binning on the column APPLICATION_TYPE based on the results of a density plot.

![image](https://user-images.githubusercontent.com/83438418/140687346-bfd9f6e8-2645-4bf6-a746-a03eb3cc0185.png)

The result was a mere 72.4%, even lower than the 1st try.

![image](https://user-images.githubusercontent.com/83438418/140687433-fa09d57b-18a1-4176-9346-d53f9151f9f2.png)

3rd Optimization – using the same set up as before but changing the binning on the column AFFILIATION and NAME, the accuracy reached 75%.

![image](https://user-images.githubusercontent.com/83438418/140687642-94d078cb-31b5-4fef-8e26-65d7526b4c6c.png)


## Summary.

When trying to manipulate data using different number of layers, there were no significant improvement in the accuracy. However, when dropout layer was used, the result was satisfactory, reaching 75% immediately. Hence we could conclude that if 25% of neurons were dropped, the model's randomness increased resulting in a better pattern reading hence better result in accuracy.
