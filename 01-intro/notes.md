# 01 Introduction to machine learning notes

### 01 What is machine learning?

Machine learning is software that builds mathematical models from data to make predictions without traditional programming. 

For example a model for predicting a used car price can be made using older data about a variety of old cars, their data and prices. The model is trained by taking features (what we know about the object) and the target (the price) and giving them to a machine learning algorithm. This algorithm produces some model that can predict the target (price) of a previously unknown object (car) and it's features.

### 02 Machine learning vs Rule-Based Systems
Traditional rule-based systems can be hard to set up, expand and maintain, when there are many variables.

Using machine learning, a model can be created can handle all these rules, simply by training a model based on previous data.

This differnece is explained using an analogy of the creation of a email spam filter.
It's very difficult to write out all rules to define what is spam and what is not. In fact in can be an ever changing process.

ML can solve this issue using the following steps:
1. Collecting the data. Users define what is spam and non-spam.

2. Define the features. Each feature is defined, and each email can be encoded to the values of its features. This encoding is portrayed as an n-dimensional vector for the algorithm. The target here is defined by the user. (For example defining the target is 1, if marked spam by the user, 0 if not.)

3. Train and use the model
Some machine learning algorithm can be applied to the encoded emails (features) to create some model that can predict whetere a new email is spam or not.

Note: These predicitons are probabilities, and thus to make a decision it will be necessary to define a threshold that classifies if the email is spam.

### 03 Supervised Machine Learning
Supervised Machine Learning is all about training a model by example. A model is trained from previous data to learn how to predict new unknown objects. The machine learns patterns and uses them.

We show the data to model in two parts.
A feature matrix, usually written as capital X.
A target variable, usuaully written as lowercase y. It is a vector.

This X and y is put into our ML algorithm. 
In this context, the model is usually denoted as g, a function that takes our feature matrix X and produces something that is approximately close to the target Y.

g(X) ≈ y

We want our g(X) to be as close to y as possible.

The process of finding g is called training.

Types of machine learning:

Regression
g returns a number, in whatever range that make sense for the problem. Like the car price case.

Classification
We output a category. Binary classification, has excactly two categories, 0 or 1. Multiclasss classification: more than two categories. Like classifying images into cats, dogs or cars. 

Ranking:
Usually shows in recommender systems. Like on Amazon.
Every item is ranked by probability. Like google search or amazon product recommendations.

### 04 CRISP-DM
CRISP-DM(Cross-Industry Standard Process for Data Mining) is a methodlogy, that describes the entire process from understaning a problem to deploying the solution.
According to a google search it is the de facto industry standard for traditional data science projects and analytics.

CRISP-DM helps organize the steps of a machine learning problem.

The high-level workflow of a machine learning project:
1. Understand the problem
2. Collect the data
3. Train the model
4. Use it.

CRISP-DM:
Step 1: Business understanding
Identify the problem to solve. What is the problem, to what extend is it a problem, how is it experienced? Do we need machine learning to solve it?

"If we have a hammer, everything looks like a nail".

If ML is used, define KPI's.

Step 2: Data undetstanding.
Find and collect data. Be critical of data. Does the source work? Is the data reliable? And is the data set large enough?

Step 3: Data prep.:
Extracting features from raw data, cleaning data, building pipelines, converting the data to a tabular format.

Step 4: Modelling
Train the model. Try different ones and select the best.

Step 5. Evaulation
Evaluate the model against the KPI. If goal is not met iterate or reconsider project.

Step 6. Deployment
If goal is met. Deploy; roll out the model to production.
Note: Today models are ofte evaluted through deployment. Online evalution: We test hte model on a selected group of real users.

Iterate:
Start simple, learn from the feedback, improve.

### 05 Model Selection Process
When we model, that is, in the context of CRISP-DM, step 4, we must try different models and choose the best one.

Deciding if a model fits:
Our model is trained on old, but during the process of trying and evaluating differnt models, we cannot compare it to future data.

So we split our dataset into a training set and a validation set, say a 80/20 ratio.

Training set: We extract our feature matrix X and target y and train g using only these.

From the validation set we extract another matrix Xv, and its target yv.

We can then apply g to Xv and get predictions. We can then count how many cases the model was correct.

We can repeat this process for different models, and compare their accuracy, and pick the best fit.

Multiple comaprisons problem:
Models can get lucky on parituclar subsets of data, and might not actually be the best fit. 

To guard against this we can define three non-overallping subests, training data, validation data, and test data. (Test data is like one extra round of validation). Our best model from validation can be measured against the test set to validate whether it got lucky on the validation dataset.

NB: It is possible to reuse validation data. After selecting the best model, the validation and training datasets can be combined to forma. signle training dataset before testing it on the test set.

### 06 - 07 - 08 - 09 
Enviroment setup, introduction to numpy and pandas. Linear algebra refresher.
No notes.
