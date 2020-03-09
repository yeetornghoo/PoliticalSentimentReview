# Topic: Political Review

## Assignment 1
This assignment is to create our own Lexicon Sentiment files by simply extract the adjectve words from classified positive review and negative reviews source files. Both Spacy and NTLK to extract adjectives are used. For certain adjective words appear in both positive and negative review files will be flagged as "0". [See More](https://classroom.google.com/u/1/c/MjcxMjM5ODc3OTZa/a/NDA3ODYwODEyMTBa/details)

#### Sources
- Colab File: https://colab.research.google.com/drive/1OdQte-xd2wRt2-cj3MeBn0DmZeEMCZ8x
- Dataset: [Positive Review](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_positive_reviews.csv), [Negative Reviews](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_negative_reviews.csv)
#### Steps
- Import all needed libraries
- Load dataset files [Positive Review](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_positive_reviews.csv), [Negative Reviews](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_negative_reviews.csv)
- Text Processing
	- Extract word and make it lower case
	- Lemmatization and Remove Stop words
	- Extract Adjective word by using both SPACY and NTLK
#### Output
Generate Lexicon Files
| File  | Link | Total Words |
| ------------- | ------------- | ------------- |
| Positive File | [lexicon_political_positive.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_positive.csv) | 155 |
| Negative File | [lexicon_political_negative.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_negative.csv) | 163 |
| Combined File | [lexicon_political_master.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_master.csv) | 277 |

<br/><br/>
## Assignment 2
This assignment is to use the Lexicon Sentiment file generated from Assignment 1 and assess the review of the dataset files. [See More](https://classroom.google.com/u/1/c/MjcxMjM5ODc3OTZa/a/NDA3ODYwODEyNjFa/details)

#### Sources
- Colab File: https://colab.research.google.com/drive/1C6hEaZJ9GKdmK-GvTmAk8QsUOCfDASgb
- Dataset: [Positive Review](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_positive_reviews.csv), [Negative Reviews](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_negative_reviews.csv)
- Lexicon Master: [lexicon_political_master.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_master.csv)
#### Steps
- Import all needed libraries
- Load [lexicon_political_master.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_master.csv)
- Load the [Positive Review](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_positive_reviews.csv) and compare to the master lexicon file
- Load the [Negative Reviews](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_negative_reviews.csv)
- Verify the accurary for each
#### Output

| Type | Total Review | Classified as +ve | Classified as -ve | Classified as Neutral | Accuracy | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Positive | 46 | 38 | 0 | 8 | 82.61% |
| Negative | 54 | 2 | 39 | 13 | 72.22% |

<br/><br/>
## Assignment 3
Assignment 3 is to use BOW and TD-IDF technique to create the features of the document, and use machine learning technique to do document classification. [See More](https://classroom.google.com/u/1/c/MjcxMjM5ODc3OTZa/a/NDA3OTk0ODQ1Mjha/details)
#### Sources
- Colab File - https://colab.research.google.com/drive/1p37xim6mtTFf6FQPWinHqNjNFSkhjw3a
- Dataset: [Positive Review](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_positive_reviews.csv), [Negative Review](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/dataset/politic_issues_negative_reviews.csv)
#### Steps
- Load Positive and Negative Reviews files
- Combine both files and assign class label (0: Negative and 1: Positive)
- BOW
	- Convert Training Data and test Data to BOW
	- Run several machine Learning to compare the performance
- TF-IDF
	- Convert Training Data and test Data to TF-IDF
	- Run several machine Learning to compare the performance	
- Doc2Vec
	- Convert Training Data and test Data to DOC2VEC
	- Run several machine Learning to compare the performance	
#### Output

###### BOW

| Classifier | Accuracy | F1 | Precision | Recall | 
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Gradient Boosting | 50.00% | 45.00% | 72.00% | 58.00% |
| Random Forest | 40.00% | 29.00% | 20.00% | 50.00% |
| Multinomial NB | 60.00% | 58.00% | 75.00% | 67.00% |
| ANN | 70.00% | 70.00% | 79.00% | 75.00% |
| SVN | 40.00% | 29.00% | 20.00% | 50.00% |
| Linear | 70.00% | 70.00% | 79.00% | 75.00% |
| Logistic Regression | 60.00% | 58.00% | 75.00% | 67.00% |

###### TF-IDF

| Classifier | Accuracy | F1 | Precision | Recall | 
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Gradient Boosting | 50.00% | 49.00% | 55.00% | 54.00% |
| Random Forest | 40.00% | 29.00% | 20.00% | 50.00% |
| Multinomial NB | 50.00% | 45.00% | 72.00% | 58.00% |
| ANN | 70.00% | 70.00% | 79.00% | 75.00% |
| SVN | 40.00% | 29.00% | 20.00% | 50.00% |
| Linear | 70.00% | 70.00% | 79.00% | 75.00% |
| Logistic Regression | 50.00% | 45.00% | 72.00% | 58.00% |

###### DOC2VEC

| Classifier | Accuracy | F1 | Precision | Recall | 
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Gradient Boosting | 30.00% | 29.00% | 30.00% | 29.00% |
| Random Forest | 50.00% | 45.00% | 72.00% | 58.00% |
| Gaussian NB | 50.00% | 45.00% | 45.00% | 46.00% |
| ANN | 30.00% | 29.00% | 31.00% | 33.00% |
| SVN | 40.00% | 29.00% | 20.00% | 50.00% |
| Linear | 30.00% | 29.00% | 31.00% | 33.00% |
| Logistic Regression | 20.00% | 17.00% | 12.00% | 25.00% |

Result: ANN and Linear for BOW and TD-IDF

## Individual Assignment
- Colab File - https://colab.research.google.com/drive/1cyO8V4_lYQdoP9sPCP3Ak0TZLaMYOP-m

Following are the best performance results from Machine Learning based (BOW or TD-IDF) and Lexicon based. Where the ML based best performance is 70%, however the Lexicon based get 82.61% to predict Positive and 72.22% to predict negative (Average 77.415%)


| Approach | Feature | Classifier | Accuracy | F1 | Precision | Recall | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Machine Learning | BOW / TD-IDF | Linear | 70.00% | 70.00% | 79.00% | 75.00% |
| Lexicon Based | - | - | 77.415% | - | 82.61% | 72.22% |

# Topic: Restaurant Review
- Assignment 1 - https://colab.research.google.com/drive/1t5Wr5Oj0UNii3Vabm99SQu9wLX8LbJgD
- Assignment 2 - https://colab.research.google.com/drive/1lcj5jJxzDX2726QgjgYaKe7QfRDWyDPf
- Assignment 3 - https://colab.research.google.com/drive/1Af_oNhHVM3mbsXWjL0_RKICtd5qFT5Xv
- Individual Assignment - https://colab.research.google.com/drive/1y1GHwrAbVo-K6y1C-RbjYxFRvfM6uoNr
