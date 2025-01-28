## Sentiment Analysis - NLP Text Mining

[Dataset](https://www.kaggle.com/datasets/pashupatigupta/emotion-detection-from-text)


Sumbitted on 27 Oct 2023 Paper name: Data Mining and Knowledge Engineering


**Project Objective:**
To compare the performance of three classification algorithms Multinomial Naive Bayes, Multilayer Perceptron, and Support Vector Machine.

<br>

**Tools used**
Python (NLP libraries like NLTK, and Machine Learning libraries like scikit-learn).

<br>

**Algorithms and parameters used:**
Multinomial Naive Bayes (MNB), Param: default
Multilayer Perceptron (MLP), Param: 100,100, a=0.01
Support Vector Machine (SVM), Param: default

<br>

**Results (accuracy):**
**MNB:** 0.533
**MLP:** 0.53
**SVM:** 0.59

<br>

**Best-performing algorithm and why:**
Support Vector Machine.

**Reason:** SVM demonstrated the highest Accuracy, Precision and Recall rates. It also exhibited robustness to noise and changes in input data, making it the ideal choice for the this particular dataset. Additionaly, it does not require significant computational resources, making it an approachable option.

<br>

**Details about the dataset:**
This public domain dataset is collected from data.world platform, shared by @crowdflower, a data enrichment, mining and crowdsourcing company based in the US.
The dataset consists of 40000 records of tweets labelled with 13 different sentiments, followed by Tweet ID number.
All data types are strings, except for the 'tweet ID' column, which is an integer.
There is a class imbalance of <21.32%. Tweets primarily convey neutral and negative sentiments.
Contains 172 duplicate rows (tweets) but categorised with different sentiment labels.
Word lengths vary, ranging from a minimum of 1 word to a maximum of 16 words.
The data exhibits some degree of disorder and lack of cohesion. Various linguistic patterns used to express sentiment.
Some information contains only special characters or hyperlinks.
Contains informal and colloquial terms. For instance, “peeps” is a friendly term for “People”.
Contains self-made terms, slangs or misspellings such as “Humpalow”.

<br>

**Four things I did to maximise accuracy and why:**

**One:** Cleaned special characters

**Rationale:** Tweets contain dynamic ways of conveying emotions through text. I retained punctuation marks ('!' and '?') to capture emotional tones during text cleaning. However, as there was no significant difference in the results - I proceeded to remove these characters.

**Two:** Lemmatisation
Rationale: Experimented stemming and lemmatisation, using both and interchangeably. Neither had zero to minimal impact on accuracy. Stemming showed no effect, while lemmatisation produced slight changes of 0.001.

**Three:** Retained stopword
**Rationale:** Retaining stopwords improved precision. There's a possibility that removing stopwords could result in the loss of valuable information, especially in rows where a high number of stopwords, accounting for over 50% of the sentence.

**Four:** TF-IDF as Feature Engineering method
**Rationale:** TF-IDF exhibited higher accuracy compared to GloVe. Accuracy rates dropped by up to 20% after embedding text using GloVe.
