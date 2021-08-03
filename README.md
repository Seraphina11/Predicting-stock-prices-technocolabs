<h1 align="center"> Predicting-stock-prices-technocolabs</h1>

## Problem statement:

**<font size="4.5"> Given data of News Title and Headline along with some other features, predict the sentiment of News Title and Headline. </font>**

<font size="4"><span style="color:Black;font-family: Arial"> Sentiment Analysis or Opinion Mining is a way of finding out the polarity or strength of the opinion (positive or negative) that is expressed in written text, in the case of this project – stock news articles. According to the principle of document level sentiment analysis, each individual document is tagged with its respective polarity. This is generally done by finding polarities of each individual words/phrases and sentences and combining them to predict the polarity of whole document. </span></font>**

### Modelling

* <font size="4.5">We have applied  Machine Learning techniques such as logistic regression,Naïve bayes model to predict the target variable.
 </font>
* <font size="4.5">We have quantified the sentiment  of news headlines with a positive or negative value, called **polarity**.For sentiment analysis  calculation of overall polarity of headline of each date  is required ,for which sentiment function of textblob  is used.  The overall sentiment is inferred/labelled as positive, neutral or negative based on the sign of the polarity score. 
 </font>
* <font size="4.5">The **compound score** is the sum of positive, negative & neutral scores which is then normalized between -1(most extreme negative) and +1 (most extreme positive).The more Compound score closer to **+1**, the **higher** the positivity of the text. 
 </font>
* <font size="4.5">**VADER** is used to quantify how much of ***positive or negative emotion*** the text has and also the intensity of emotion. Vader SentimentIntensityAnalyzer is used in this program to calculate the news headline compound value for a given day.  
 </font>
 

 ### <p> Step 1) Defining the model</p>

<font size="4.5"><span style="color:Black;font-family: Arial">In this step, we generate our model-fitting our dataset in the MultinomialNB.
We will use one of the Naive Bayes (NB) classifier for defining the model. Specifically, we will use 
MultinomialNB classifier. 
We used Naïve Bayes model because it works particularly well with text classification and spam filtering. Advantages of working with NB algorithm are:
    
*	Requires a small amount of training data to learn the parameters
*	Can be trained relatively fast compared to sophisticated models

</span></font>

![image.png](attachment:image.png)
![image-2.png](attachment:image-2.png)

### <p> Step 2) Splitting the Dataset</p>

<font size="4.5"><span style="color:Black;font-family: Arial">We do the train/test split before the CountVectorizer to properly simulate the real world where our future data contains words we have not seen before.Split then vectorize is considered the correct way.

</span></font>  

### <p> Step 3) Applying tf vectorizer (count vectorizer)</p>

<font size="4.5"><span style="color:Black;font-family: Arial">If we want to use text in machine learning algorithms, we’ll have to convert them to a numerical representation.   One of the methods is called bag-of-words approach. The bag of words model ignores grammar and order of words. 
Here, we use CountVectorizer (another term of TfVectorizer).it will basically convert these sentences into vectors. That is what bag of words means.
</span></font>

### Now we have the training and testing data. We should start the analysis. 


### <p> Step 4) Applying Naive Bayes</p>

<font size="4.5"><span style="color:Black;font-family: Arial">Training Naive Bayes classifier with train data.Since we are using sklearn’s modules and classes we just need to import the precompiled classes.we generate our model-fitting our dataset in the MultinomialNB.Naive Bayes using bag of words (unigrams of words) and character level n-grams. N-gram  is  a  tokenization  process  to  separate  words  based on the type of token used. In this study mainly bigram was used. Bigram  is  a  n-word  solution  in  a  review  sentence  with  n  =  2. ngram_range=(2,2)
</span></font>

### <p> Step 5) Evaluation</p>

<font size="4.5"><span style="color:Black;font-family: Arial">The performance evaluation of the Naive Bayes algorithm in this study was carried out by calculating the value of Precision, Recall, Accuracy and Error Rate by using confusion matrix. Here we are applying the classification report, confusion matrix, and accuracy score to check the accuracy of our model.Cross-validation is a statistical method used to estimate the skill of machine learning models.
</span></font>

### <p> Step 5)  Improving the model and handling unbalanced data</p>

<font size="4.5"><span style="color:Black;font-family: Arial">As is known to us, Naive Bayes algorithm is a simple and efficient categorization algorithm. However, the assumption of conditional independence in this algorithm does not conform to objective reality which affects its categorization performance to some extent. In order to improve the categorization performance of Naive Bayes algorithm in text categorization, a Naive Bayes text categorization algorithm based on TF-IDF attribute weighting  is used. Let’s use TF-IDF, which takes in account the product of term frequency and inverse document frequency. TF-IDF shows the rarity of a word in the corpus. If a word is rare then probably its a signature word for a particular sentiment/information.

</span></font> 


## RESULT:- 

### After calculation of accuracy and generation of classification report for sentiment analysis, from test data from  Naive Bayes classifier model ; We got the accuracy of 91.54% .





  
