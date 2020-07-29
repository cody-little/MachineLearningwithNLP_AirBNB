# MachineLearningwithNLP_AirBNB
A machine learning project comparing textual feature representation methods to classify AirBNB price ranges

## Summary

This is a project that utilizes cross disciplinary approaches to understand methods of predicting price ranges on short term rentals. Using a combination of text representation methods from computational linguistics and metadata I compare how different feauture spaces effect outcome metrics along with their level of computational effeciency. If you want to see an indepth walk through check out the notebook section of the repository.As an overview this project sought to:

* Predict a multiclass price range for AirBNB short term rental spaces in New York City (low, medium, high) using the text from the rental space description 
* Compare bag-of-words and SpaCy word embeddings text feature representation for outcome metrics and computational effeciency
* Train, Validate, and optimize the best classifiers (their hyperperamters) and feature spaces for the task using a hybrid representation space of text and metadata

## Results

The best classifier found through validation was the Random Forest Algorithim below are the results across three metrics comparing text representation methods.

|Text Representation|Accuracy|F1 Score|Quadratically Weighted Cohen Kappa Score|
|-------------------|--------|--------|----------------------------------------|
|Bag of Words| 68.1% | .684| .483|
|SpaCy Word Embeddings| 65.7%| .651| .483|

Both classifiers performed significantly better than baseline majority levels and twice as well as random guessing. The Bag-of-Words representation performed marginally better across 2/3 metrics and was much faster to train and validate due to the slow speed of word embeddings coupled with the long training times of Random Forest Algorithims. Using only text representation along with three meta data feautres (number of reviews, room type, and neighborhood group within the city) the process achieved a succesful outcome in classifying price ranges. This form of automation could enable customers to better filter rental options based on this criteria, it also could give short term rental companies such as AirBNB insight into how the textual descriptions of their rental spaces either raise or lower the price in a comparable area.


#### Bag of Words Results

![](https://github.com/cody-little/MachineLearningwithNLP_AirBNB/blob/master/images/bowrepNLP.PNG)

#### Word Embedding Results

![](https://github.com/cody-little/MachineLearningwithNLP_AirBNB/blob/master/images/embeddingrepNLP.PNG)
