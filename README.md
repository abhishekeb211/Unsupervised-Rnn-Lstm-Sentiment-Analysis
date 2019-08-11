# Unsupervised-Rnn-Lstm-Sentiment-Analysis
Customize model to highest accuracy and used to label unsupervised data  


Setup Virtual Environment(Sentiment_requirements)

env to install all files in the requirements.txt file.
1.	cd to the directory where Sentiment_requirements.txt is located
2.	activate your virtualenv eg.-	source bin/activate
3.	run: pip install -r Sentiment_requirements.txt in your shell



PRE-PROCESSING :
1.	Batch Processing (Time Series Preprocessing.py)
Dataset in different format including huge continuous text and time series data.
(Sometimes data format conversion requires as core panda series , Big-query data and various databases )*
•	Text data can be split into lesser than 1 Lac words in different files
•	Time Series data divide into year, month, week and days according to data size.

2.	NLP (Word Processing.py)
•	Tokenization: Divide sentence into smaller parts and removing punctuations.
•	Lemmatization: Stemming means cutting ends and beginnings of words into root form
•	Removing Stop-Words: Removing prepositions from Tokens




