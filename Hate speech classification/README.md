<h2> Hate speech classification</h2>

Dataset used: twitter hatespeech data from Kaggle

[click here to view dataset](https://www.kaggle.com/vkrahul/twitter-hate-speech)

|Column name | Column Description|
|:----------:|:-----------------:|
|id          | Serial Number     |
|Label       | Label of the text |
|            |1-> Hate text       |
|            |0-> Not hateful text|
|Tweet       | The text           |

<h2> Data Cleaning</h2>

- Dataset is a unbalanced dataset with only 7% of hateful command data
- Carried out under sampling
- As the data is a crowd source data it has abundant of non numeric and non alphabetic characters
- Cleaned greek characters
- Extracted and replaced hashtags
- Cleaned for stop words, slang words
- Tokenized
- Padded




<h3>Algorithms used: Supervised Algorithms:</h3>

- Logistic Regression
- Decision Tree
- Random forest
- Naive Bayes
<h3>deep learning model</h3>
 
- LSTM

Experiments with: TFIDF

Metric for ML algorithms
Model with best accuracy: Gradient boosting
Model with best ROC score: Logistic regression

REFERENCE:
    
NYTimes/ online https://www.nytimes.com/2019/11/12/us/hate-crimes-fbi-report.html 

dailyprinceton/ online https://www.dailyprincetonian.com/article/2018/10/hate-speech-deserves-a-second-look 

Hate Speech Classification of social media posts using Text Analysis and Machine Learning Venkateshwarlu Konduri, Sarada Padathula, Asish Pamu, and Sravani Sigadam, Oklahoma State University https://www.sas.com/content/dam/SAS/support/en/sas-global-forum-proceedings/2020/5204-2020.pdf 

Towards data science /online
https://towardsdatascience.com/detecting-hate-tweets-twitter-sentiment-analysis-780d8a82d4f6 
