# Twitter Sentiment Analysis

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Main results](#results)
5. [Methodology](#methodology)
6. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

Most of the libraries used on the project, such as pandas, numpy, matplotlib and tensorflow can be installed using the Anaconda distribution of Python.

You will need to install the following libraries used for dowload and read the data, do natural language preprocessing and use the BERT Neural Nertork model:
 * kaggle==1.5.6
 * zipfile
 * wordcloud
 * nltk
 * gensim
 * ktrain

The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

My goal's to solve most of the machine learning projects of this [Medium artcile](https://medium.com/projectpro/20-machine-learning-projects-that-will-get-you-hired-in-2021-a89473f2d2c7). I'm not following any sequential order, but instead, I'm focusing on projects that make me experiment and try as many different techniques as possible.

For this project, my focus was to apply some natural language processing techniques and apply LSTM Neural Networks and fine-tune pre-trained Transformers Neural Networks.


## File Descriptions <a name="files"></a>

There is one Jupyter notebook available used to do the exploratory analysis to answer the above questions and train the deep learning models used on the project.  

There are also some PNG files with recent tweets of famous people that we tried to predict its sentiment using the developed models.

The images folder contains the main visualizations used in the exploratory analysis.

## CRISP-DM Methodology <a name="methodology"></a>

### Business Understanding

Sentiment analysis on text data has much application for companies nowadays. It can be used for example:
 * Customer satisfaction by measuring if the recent mentions, tweets, posts, and commentaries on companies' social media are more positive than negatives;
 * Evaluate how good or bad people are talking about some companies and incorporate it into your stock purchase strategy;
 * And many more use cases.

 For the project, I develop a Deep Learning model to predict if a given tweet has a positive or negative sentiment that can be used for the use cases above.


### Data Understanding

The data used is from the [Sentiment140](https://www.kaggle.com/kazanova/sentiment140) dataset available on Kaggle. This dataset has 1.6 million tweets, each one classified as either “positive” or “negative” sentiment. 

In the dataset we have three main columns to focus on:
* user: who made the tweet;
* text: the content of the tweet ;
* sentiment: the sentiment classification (1 for positive and 0 for negative).

Also, by doing some exploratory analysis I could answer the following questions:

1. What are the most common words in POSITIVE sentiment tweets? And what words is shown more often in the NEGATIVES ones?
2. Do users who tweet the most tend to have positive or negative sentiments? Who are these users?
3. Does the NUMBER OF WORDS in a tweet help determine whether it has positive or negative sentiment?
4. Does the TWEET LENGHT in a tweet help determine whether it has positive or negative sentiment?

### Data Preparation

Since we are using text from tweets, we must remove mentions, hashtags, and URLs. They were removed by using regular expressions.

Also, I removed punctuations and removed stop words. These are the most common words in any language and do not add much information to the text because they can appear in both positive and negative examples. Examples of a few stop words in English are “the”, “I”, “me”, “so”, “what”.

After that, I used the Tokenizer class from Keras preprocessing to create a dictionary of words where every word has its number to represent it.

### Modelling

The Deep Learning models used on the project were:
* Long Short-Term Memory (LSTM) Neural Networks;
* BERT, a type of Transformer Neural Network.

### Evaluation

The data was split into training, validation, and test sets. The accuracy for each model on training and validation sets were:

Model  | Training Set | Validation Set
------------- | ------------- | -------------
LSTM model  | 82% | 76%
BERT model  | 98% | 78%

Since the BERT model got better accuracy on the validation set over the LSTM model, I used the BERT model to predict the test data and it got the same 78% of accuracy.

### Deployment

The model was not deployed in any application but the code is available on the _twitter_sentiment_analysis.ipynb_ file on this repository.

Also, the main insights of the project can be found in the blog post at the [Main results](#results) section.



## Main Results<a name="results"></a>

The main insights found in the exploratory analysis and a brief explanation of how the Deep Learning models used in the project works are available this [blog post](https://medium.com/@andredesouzag/twitter-sentiment-analysis-in-way-you-probably-never-seen-before-8e0f1553629e).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

You can find the Licensing for the data and other descriptive information at the Kaggle link available [here](https://www.kaggle.com/kazanova/sentiment140). All the credits and acknowledgements are for the dataset owner. Otherwise, anyone can use the code available.

