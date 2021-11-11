# Chatbot
----------------

This chatbot will be trained on the dataset which contains categories (intents), pattern and responses. Recurrent neural network (LSTM) is used to classify the user’s message to the category it belongs to and then a response will be selected.

The dataset is ‘intents.json’. This is a JSON file that contains the patterns we need to find and the responses we want to return to the user.

Pre-process data

Tokenizing  the text. Here we iterate through the patterns and tokenize the sentence using nltk.word_tokenize() function and append each word in the words list. We also create a list of classes for our tags.

lemmatize each word and remove duplicate words from the list
create a pickle file to store the Python objects which we will use while predicting

Create training and testing data

create the training data. input is the pattern and output is the class our input pattern belongs to. text is converted into numbers.

Build the model

Now build a deep neural network that has 3 layers. We use the Keras sequential API for this. After training the model for 200 epochs, we achieved 100% accuracy on our model. Save the model as ‘chatbot_model.h5’.

