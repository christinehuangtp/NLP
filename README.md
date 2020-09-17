# NLP
Use Python’s natural language toolkit (NLTK) and the TextBlob library which is built on the NLTK and text pattern NLP libraries.

### Introduction.
The goal of this assignment is to perform natural language programming and Python’s natural language toolkit (NLTK) and the TextBlob library which is built on the NLTK and text pattern NLP libraries. The two main tasks performed here are sentiment analysis and similarity analysis. I used web scraper to extract the book review data sets from amazon website.

### Dataset
#### first data source: https://www.amazon.com/Girl-Dragon-Tattoo-Millennium-Book-ebook/product-reviews/B0015DROBO/ref=cm_cr_dp_d_show_all_btm?ie=UTF8&reviewerType=all_reviews

#### Second data source: https://www.amazon.com/Girl-Played-Fire-Millennium-Book-ebook/dp/B001NLKT60/ref=sr_1_2?dchild=1&qid=1587526251&refinements=p_27%3AStieg+Larsson&s=digital-text&sr=1-2

The two data sets are extracted from the amazon website using data miner built in google chrome extension, that will return the datasets containing 200-300 rows(decided by the users), with attributes including review titles, review text and stars. Even though there are missing values within the data, as we only need review texts and stars in this assignment, this time I'll skip the data cleaning process.

#### 1. Sentiment analysis
- from textblob import TextBlob
- from textblob.sentiments import NaiveBayesAnalyzer
- import nltk
- nltk.download('movie_reviews')

#### Summary: 
By using Naïve Bayes analyzer for NLP sentiment analysis, we found that the prediction accuracy of sentiment rating for girl with the dragon tatoo is 0.64 from the first book and 0.56 from secound book based on 50 reveiw data.

#### 2. Similarity analysis
##### Compute the similarity on each data point in two review sets
- import spacy
- nlp = spacy.load('en')  

#### Summary: 
The overall similarity between two books with the same reviewer are around 0.9 to 1.0. The average of similarity is 0.93+, providing high similarity between two book reviews. when we shuffle two reviews by different username, the average of similarity is 0.90. It still providing high similarity even they are different reviewers. It might because the writing way that reviewers used for a same series book is very similar. Or the similarity from this model is not very accurate when detect book reviews.

#### 3. Visualizing Word Frequencie
- from pathlib import Path
- from textblob import TextBlob

Eliminating the Stop Words
- import nltk
- from nltk.corpus import stopwords
- nltk.download('stopwords')
- stop_words = stopwords.words('english')

##### Sorting the Words by Frequency
##### Displayed the TOP 20 frequency words by graph

##### Comparing the top 100 frequency words from reviewers in two books
#### Summary: Compute the same high frequency words between two books: 0.65
