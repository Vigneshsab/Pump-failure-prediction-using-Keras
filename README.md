# Predicting-failure-of-a-Pump-using-Keras
This project aims to analyze and implement a model for a pump dataset, which consists of 50 sensors and 2,00,000 datapoints. This model predicts whether the pump will fail in the next 24 hours using sampled data from the original dataset. The model achieved an accuracy of 95%.

# Purpose of Project
The main purpose of this project was to predict the failure of pump before 24 hours and alert the plant users to take necessary action to repair it. For example, if the plant users do not know when the pumps will fail, they will need to spend a lot of time and energy to fix the pump after it has failed. This could reduce the efficiency and the production rate of the pump. To solve this problem, we try to predict the failure of a pump before 24 hours. This will help the plant users to keep necessary things ready to fix the pump. This could also improve the productivity of the pump and reduce costs for repair.

# Methodology
A MLP model accepts an input in a single vector format and gives an output for the respective vector. Out of these sample data, we take a particular number of samples for the training of this model. Since our aim is to predict the failure of a pump in the next 24 hours, we take inputs where the pump did not fail at all. 
For example, for one input window we will take 60 points(1 hour) as the input window. We have to make sure that the pump doesnt fail in this input window. After this step is done, then we will check the next 60X24 points ( 24 hours), as the output window. We will check whether the pump has failed in this output window and assign a label accordingly. This will create a new dataset with inputs and respective outputs for the MLP model. Below is a flowchart of the process.

![Flowchart](https://github.com/Vigneshsab/Pump-failure-prediction-using-Keras/blob/master/flowchart.png)


