# Topic: Political Review

## Assignment 1
This assignment is to create our own Lexicon Sentiment files by simply extract the adjectve words from classified positive review and negative reviews source files. Both Spacy and NTLK to extract adjectives are used. For certain adjective words appear in both positive and negative review files will be flagged as "0". 

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
#### output
Generate Lexicon File
- Positive File: [lexicon_political_positive.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_negative.csv)
- Negatice File: [lexicon_political_negative.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_negative.csv)
- Combined: [lexicon_political_master.csv](https://github.com/yeetornghoo/UD_PoliticalReview/blob/master/lexicon_sentiment/lexicon_political_master.csv)

## Assignment 2
This assignment is to use the Lexicon Sentiment file generated from Assignment 1 and assess the review of the dataset files

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

## Assignment 3

## Individual Assignment
