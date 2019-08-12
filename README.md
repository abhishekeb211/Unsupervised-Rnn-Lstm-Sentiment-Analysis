# Unsupervised-Rnn-Lstm-Sentiment-Analysis
Customize model to highest accuracy and used to label unsupervised data  


Setup Virtual Environment(Sentiment_requirements)

Setup Virtual Environment(nlp_requirements.txt)
env to install all files in the requirements.txt file.
1.	cd to the directory where requirements.txt is located
2.	activate your virtualenv eg.-	source bin/activate
3.	run: pip install -r nlp_requirements.txt in your shell


Building Model with labelled dataset (IMDB):
Using IMDB dataset containing tweets word-embedding value and Sentiment value (0 or 1 format). On this two inputs model going to be trained and afterwards it should be test. Now we can use the train_test_split function in order to make the split. The test_size=0.2 inside the function indicates the percentage of the data that should be held over for testing. It’s usually around 80/20 or 70/30.
Eg.
X_train, X_test, y_train, y_test = train_test_split(df[df as tweets word-embedding value], y[y as Sentiment value], test_size=0.2)


Designing Model layers:
Deciding the input in batch process with number of dropout and recurrent network nodes. Need to define number of Lstm layers and activation function as need of dataset  


_____________________________________________________________
Layer (type)                 	Output Shape              Param #   
=================================================================
embedding_1 (Embedding)      (None, 80, 128)           2560000   
_________________________________________________________________
lstm_1 (LSTM)                (None, 80, 64)             49408     
_________________________________________________________________
lstm_2 (LSTM)                (None, 32)                12416     
_________________________________________________________________
dense_1 (Dense)               (None, 1)                 33        
=================================================================


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

