# NLP-Sentiment-Analysis-with-SGD
Documentation and code for a sentiment analysis project that guesses the emotion of sentences with a good degree of accuracy.

This is a personal project that takes in an excel file with sentiments and their associated sentences. Each word is stemmed and has regex rules applied to it (such as removing periods, apostraphes, and endings such as -s and -ing when applicable). Each word in a sentence is then compared with the NRC sentiment analysis datasheet to see if it holds either a shared 'sad' or 'happy' emotion (represented as 1 in the NRC sheet), and the total number of positive and negative words in a sentence are recorded. This is used for initial sentiment analysis and used in training. 

Combinations of all training sentences are made with one sentence left out for testing. Over 300 combinations for when stochastic gradient descent is applied to the training data. Each combination has its loss calculated, and the combination with the least loss is used as the primary model for sentiment analysis.

The selected combination is applied, and all results are modeled in a confusion matrix, as well as in calculations for accuracy, precision, and recall.
