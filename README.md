# kaggle_satyajeet_1

## Train Dataset Opertions:

#### Missing Value Handling: 
Replaced missing values in keyword and location.

#### Cleaned Text: 
Generated a new column cleaned_text with preprocessed text.

#### Visualizations:
1. Label distribution bar chart.
2. Text length histogram.


## Test Dataset Operations : 
Read,Info,Describe,Find Null values,NLP(Remove charecter,hashtags,url's),Plot the grphs


## The preprocessing steps include:

#### Tokenization: 
Extracting individual words from the cleaned text data.

Word Frequency Count: Counting the frequency of each word using collections.Counter.

#### Visualization: 
Plotting the most common words as a bar chart using Matplotlib.

Function to Remove Stopwords: A function remove_stopwords(text) is implemented to tokenize text and remove  stopwords.

#### Applying Stopwords Removal: 
The remove_stopwords function is applied to the cleaned_text column in the DataFrame to clean the text data.


Function to Lemmatize Text : A function lemmatize_text(text) is implemented to tokenize text and apply lemmatization.

#### Applying Lemmatization: 
The lemmatize_text function is applied to the cleaned_text column in the DataFrame to further preprocess the text data.

## steps for Word2Vec Model 

#### Train Word2Vec Model
The Word2Vec model is trained on the cleaned_text column of the training dataset (data_train).

#### Compute Average Word2Vec Vector
A helper function calculates the average Word2Vec vector for each tokenized text input.

#### Generate Features
The average Word2Vec vector is computed for each entry in cleaned_text in both training and test datasets.

#### Prepare Data for Machine Learning
The feature vectors and target labels are extracted, and the data is split into training and test sets.


#### Model evaluation:
##### Logistic Regression
Trains and evaluates a logistic regression model with accuracy and classification report metrics.
A logistic regression model is trained using the training set (X_train and y_train).
The model's predictions on the test set (X_test) are evaluated using accuracy_score and classification_report.
Accuracy: 58.96%
Classification Report:
Precision (class 0): 0.59
Recall (class 0): 0.98
Precision (class 1): 0.68
Recall (class 1): 0.07

##### Random Forest Classifier
Trains and evaluates a random forest classifier for comparison.
A random forest classifier is trained on the same training set.
The predictions on the test set are evaluated with the same metrics.
Accuracy: 70.72%
Classification Report:
Precision (class 0): 0.70
Recall (class 0): 0.87
Precision (class 1): 0.73
Recall (class 1): 0.49