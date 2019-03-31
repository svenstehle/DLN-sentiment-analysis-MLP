# Sentiment classification with a MLP from Udacity Deep Learning Nanodegree
Sentiment classification & how To "frame problems" for a neural network. 

### Problem statement:
Sentiment classification of movie reviews as positive or negative. Reviews have many words each, resulting in huge input vectors and training/convergence takes a long time. Goal is to improve both training time and accuracy.

### Install and use:
* Clone repo
* Setup virtual environment
* Follow `Sentiment_Classification_Projects.ipynb`

### Approach:
* Get an overview of most common words/characters in the movie reviews
* Create unique vocabulary and map words to indices 
* Create input vector for a review with size of unique vocabulary and assign count of words used in the review on mapped index 
* Build a neural network from the ground up
* Adjust learning rate to allow the network to improve accuracy while training
* Reduce training time / improved accuracy by reducing noise and improve upon our input vector creating function. We now only store whether or not a word was used at all and reduce the impact/weight of high-count words without predictive information like "the". Thus, an input vector with only `0's` and `1's` results. 
* Improve upon the internal network structure and eliminate unnecessary multiplications and additions (with `0's` in the input vector) during forward and backward propagation
* Strategically reduce the vocabulary size by a) remove outlier words with low counts b) remove words that have low correlation with either positive or negative reviews  

### Possible improvements:
* Could have preprocessed the reviews differently altogether (remove filler words, stemming, tokenization) to improve performance

### Thoughts and lessons learned:
* Build a MLP from the ground up
* Improve structure of input data and remove noise
* We can improve performance while training with gradient descent a lot by eliminating unnecessary calculations
* Fine tuning of input data to improve accuracy and training time of our network 

