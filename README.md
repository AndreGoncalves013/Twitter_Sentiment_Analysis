# Twitter Sentiment Analysis

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

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

Also, by doing some exploratory analysis I could answer the following questions:

1. What are the most common words in POSITIVE sentiment tweets? And what words is shown more often in the NEGATIVES ones?
2. Do users who tweet the most tend to have positive or negative sentiments? Who are these users?
3. Does the NUMBER OF WORDS in a tweet help determine whether it has positive or negative sentiment?
4. Does the TWEET LENGHT in a tweet help determine whether it has positive or negative sentiment?



## File Descriptions <a name="files"></a>

There is one Jupyter notebook available used to do the exploratory analysis to answer the above questions and train the deep learning models used on the project.  

There are also some PNG files with recent tweets of famous people that we tried to predict its sentiment using the developed models.

The images folder contains the main visualizations used in the exploratory analysis.

## Results<a name="results"></a>

The main insights found in the exploratory analysis and a brief explanation of how the Deep Learning models used in the project works are available this [blog post](https://medium.com/@andredesouzag/twitter-sentiment-analysis-in-way-you-probably-never-seen-before-8e0f1553629e).

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

You can find the Licensing for the data and other descriptive information at the Kaggle link available [here](https://www.kaggle.com/kazanova/sentiment140). All the credits and acknowledgements are for the dataset owner. Otherwise, anyone can use the code available.

