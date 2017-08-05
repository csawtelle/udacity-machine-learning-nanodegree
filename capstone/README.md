# Machine Learning Engineer Nanodegree
## Capstone Proposal
Chris Sawtelle
July 25, 2017

## Proposal

### Domain Background

A home could quite possibly be the most important purchase a person will make in their lifetime. Generally a home purchase requires many years of planning, and many more years of financial responbility. In many cases a home's value increases naturally, but sometimes things don't go as planned. The ability to properly evaluate a home's value is critical during the purchase period. Homeowner's who improperly value thier home can spend the rest of their lives overpaying on a mortgage.

Housing prices are notoriously difficult to predit, and can be influenced by a very large quantity of factors. Companies like Redfin, Zillow, and Trulia spend millions of dollars in research and development to proprtly predict the value of real estate. As the owner of a real estate investment company, this problem hits close to home and the impact of an accurate model could be the difference between success and failure.

### Problem Statement

The problem seems simple at first glance. Every home has certain ammeneties. Maybe the house has a pool, or its 10,000 square feet. These are all quantifiable measurements that are publicly available. The solution would be to train a model to predict exactly how much these ammenteties are worth. They may have different vlaues based on location and market, but that also should be consistent on a region basis. The goal is to put together a model that can evaluate these features and produce an accurate value for that home that will be meaningful in the current market. This is a problem that is present in everyone's life that can be solved by machine learning.

### Datasets and Inputs

This problem is currently being examined as a Kaggle competition. As such, the dataset is available from Zillow on Kaggle. The dataset contains 33 features from homes including square footage, whether it has a fireplace, whether it has a pool, and many others. Since this dataset is presented as part of a competition, it is already collected and cleaned. The true data for the test set is also present so that a model may be trained on accurate data.

The training datafile contains the true sale price and features for 90,276 and the test dataset has features for over 1,000,000 homes, giving a large enough dataset to retrieve statistically significant results. Also since the competition is solving the exact problem that I have proposed, the dataset fits perfectly with the expected results. 

https://www.kaggle.com/c/zillow-prize-1/data


### Solution Statement

The goal of this project is to use a convolutional neural network to emulate the process that a human brain would go through when attempting to predict a home's value. A CNN will be trained on the available training data and predictions will be made on the available test dataset.

The CNN will be built on top of tensorflow using the keras framework to simplify the tensorflow architecture. 

### Benchmark Model

Since this problem is based on an ongoing Kaggle competion, many benchmark models will be available. Since Kaggle shows a leaderboard for all currently running models and the discussion board is available for comparing kernels, there are many ways to benchmark the model.

This project is also in line with current functionality on Zillow.com. This means that any new data could be entered and checked against Zillow to provide a baseline accuracy for the model. 

This project will attempt to emulate the functionality of Zillow's own price prediction algorithm, and potentially improve upon it. The target accuracy as it stands in the current leaderboard is measured by a log loss 0.0640 or less. Zillow's own claim states that the accuracy of their current algorithm is within 5% of the actual sale price of a home. The accuracy of the model produced will be measured by the log loss. 

### Evaluation Metrics

This project will be evaluated with regards to the model's ability to predict accurate home prices. I expect that a successful model will perform at least as well as Zillow's current model with an accuracy of 5%. The project should be able to allow the user to input all the possible variables of a home and produce an accurate sale value based on features including but not limited to geographical location and size.

### Project Design

The first step of this project is to collect all of the data from the Kaggle competition and begin designing the CNN architecture that would best suit this problem. Since the data is already labeled and preprocessed, there won't be much work to do before starting to build the model.

After the data has been gathered, the next step will be to begin deciding which layers should be part of the convolutional neural network. Since I have a rough idea of successful CNN architecture, I will begin by implementing the CNN used in the Udacity Dog Prediction Project. 

I intend to extract the weights from the trained model in order to infer as much as I can from the features intuitively. I believe that this will result in at least some direction to improving the algorithm. 

After multiple experiments and considerations taken from Deep Learning (Goodfellow, Bengio, Courville), I will begin 
to modify the CNN to improve the accuracy and reduce the log loss.


[Deep Learning](https://github.com/HFTrader/DeepLearningBook)
