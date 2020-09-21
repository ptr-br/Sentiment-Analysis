# Sentiment Analysis
In this project Amazon SageMaker is used to create and deploy a WebApp that is able to predict whether movie reviews are positive or negative.
Unfortunately the WebApp can not be used, since deploying the model on AWS servers would cause permanent costs.
The general use of the App with a running server can be seen in the gif below.

# WebApp architecture 
- user enters a review on website.
- website sends that data off to an endpoint, created using API Gateway.
- endpoint acts as an interface to Lambda function (user data gets sent to the Lambda function).
- Lambda function processes the user data and sends it off to the deployed model's endpoint.
- deployed model performs inference on the processed data and returns the inference results to the Lambda function.
- Lambda function returns the results to the original caller using the endpoint constructed using API Gateway.
- website receives the inference results and displays those results to the user.

![WebAppArchitecturePicture](/Web_App_Diagram.svg)

# Example of the deployed WebApp

<img src="/WebApp_example.gif" width="600" />
