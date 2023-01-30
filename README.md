# NLP-Book Genre Classification with Naive Bayes
 Determined a book genre from its description, implemented a Naive Bayes classifier and verified its performance on the given book genre dataset
 
 # What I did?

Compile takes too long time but I did not do any delete operation on dataset.
After doing the below parameter selection. Recommended for not getting RAM error.
max_df = 0.9, min_df = 2, max_features = 1000


1. Understanding the data: I gave 3 examples of keywords with freqeuncy to predict genre by description at WordCloud section.

 2.Implement NB: I used Bag of Words (BoW) model which learns a vocabulary from all the documents, then models each document by counting the number of times each word appears. By using ngram_range parameters I used 2 options below.

  -  Unigram: The occurrences of words in a document (frequency of the word).
    
  - Bigram: The occurrences of two adjacent words in a document

  - I used CountVectorizer for obtaining BoW model.
    Implementation is at Model section with and without stopword.

3. Error Analysis: I found a few misclassified books and comment on why they were hard to classified. Since there is 6 experiment total, I gave examples for some of them.

  - Examples at Unigram NB with Stopword- Bigram NB with Stopword- Unigram without Stopword section

# Accuracy 

| Methods     	| Stop-Words 	| Accuracy (%) 	|
|-------------	|------------	|:------------:	|
| Bow-unigram 	| Yes        	|      64,42        	|
| Bow-unigram 	| No         	|         63,16     	|
| Bow-bigram  	| Yes        	|           44,76   	|
| Bow-bigram  	| No         	|       50,12       	|
| TF-IDF      	| Yes        	|        62,12      	|
| TF-IDF      	| No         	|       61,81       	|
