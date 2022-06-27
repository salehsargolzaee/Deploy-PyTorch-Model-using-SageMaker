<h1 align="center">LSTM-for-Sentiment-Analysis</h1>

## About the project

I completed this guided project during my Udacity Deep Learning Nano-Degree. The project goal is to have a simple web page that users can use to enter a movie review. The web page will then send the review off to the deployed model, which will predict the sentiment of the entered review.

The notebook is divided into several parts, which are outlined below:

1. Download or otherwise retrieve the data.
2. Process / Prepare the data.
3. Upload the processed data to S3.
4. Train a chosen model.
5. Test the trained model (typically using a batch transform job).
6. Deploy the trained model.
7. Use the deployed model.



## Getting Started


The first thing needed is an AWS account to use SageMaker. You can find instructions and payment details on [the site](https://aws.amazon.com/sagemaker/).

After you get a valid account, you can go to notebook instances and create a new notebook instance. While creating, you will be asked if you want to clone a GitHub repository. You can copy the URL from below and paste it there:


	https://github.com/salehsargolzaee/Deploy-PyTorch-Model-using-SageMaker.git
    
After that, since it was a guided project, you can jump to the notebook (SageMaker Project.ipynb) and follow the instructions.

**Because I was being charged based on the time an endpoint was in service, I had to delete the endpoint and the API after the project was completed.**







#### Caveat:

**Make sure that you stop or delete any resources that you will be charged for.**


## How does it work?

<img src="Web App Diagram.svg">

The diagram above gives an overview of how the various services will work together. On the far right is the model which we trained above and which is deployed using SageMaker. On the far left is our web app that collects a user's movie review, sends it off, and expects a positive or negative sentiment in return.

In the middle is where some of the magic happens. We will construct a Lambda function, which you can think of as a straightforward Python function that can be executed whenever a specified event occurs. We will give this function permission to send and receive data from a SageMaker endpoint.

Lastly, the method we will use to execute the Lambda function is a new endpoint that we will create using API Gateway. This endpoint will be a URL that listens for data to be sent to it. Once it gets some data, it will pass that data on to the Lambda function and then return whatever the Lambda function returns. Essentially it will act as an interface that lets our web app communicate with the Lambda function.

## Contact 
<a id = "contact"></a>

Saleh Sargolzaee - [LinkedIn](https://www.linkedin.com/in/saleh-sargolzaee) - salehsargolzaee@gmail.com

Project Link: [	https://github.com/salehsargolzaee/Deploy-PyTorch-Model-using-SageMaker.git](	https://github.com/salehsargolzaee/Deploy-PyTorch-Model-using-SageMaker.git)

<p align="right">(<a href="#top">back to top</a>)</p>

## :man_astronaut: Show your support

Give a ⭐️ if you liked the project!




