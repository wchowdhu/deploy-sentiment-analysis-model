# End-to-End Sentiment Analysis of IMDb Movie Reviews

The goal of this project is to build a simple web application to predict the sentiment of movie reviews in real-time. The web page will send new reviews off to a deployed Recurrent Neural Network model using [Amazon SageMaker](https://aws.amazon.com/sagemaker/) to predict the sentiment of entered reviews. 

<img src="website/website.png">

# Install

The project requires Python 3.6 and the following Python libraries installed   
  - [numpy](https://numpy.org/)
  - [pandas](https://pandas.pydata.org/)
  - [scikit-learn](https://scikit-learn.org/stable/)

The latest version of [PyTorch](https://pytorch.org/) library also needs to be installed to implement the Neural Network model.

# Data

The dataset used for the task of binary sentiment classification is the [IMDb dataset](http://ai.stanford.edu/~amaas/data/sentiment/). The corpus consists of 25,000 highly polar movie reviews for training and 25,000 for testing. 

# Code

The notebook and Python files are provided in the project directory to get started with the project. 

# Run

To open the .ipynb files in your browser and look at the output of the completed cells, use the following command in your terminal after changing the working directory to the project directory `deploy-sentiment-analysis-model`:
```
jupyter notebook <file_name>.ipynb
```

To run and execute all the cells from scratch, you need to create a Jupyter notebook instance in the Amazon Sagemaker service, configure the lifecycle of the notebook, and attache the [Github repository](https://github.com/wchowdhu/deploy-sentiment-analysis-model) to the instance. Once set up, you can run the cells to upload the data and save any model artifacts of the trained model in [AWS S3](https://aws.amazon.com/s3/) service

To deploy the model and make the web app interact with the deployed model, you need to implement SageMaker's additional functionalities like Amazon Lambda and API Gateway. The structure for the web app is provided in the diagram `Web App Diagram.svg`.




