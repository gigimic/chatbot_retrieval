# Chatbot
----------------

There are two types of chatbots.
1. retrieval based models
2. generative nodels

Retrieval based chatbots use pre-defined input patterns and responses. 

Generative models are not based on some predefined responses.
They are based on seq 2 seq neural networks. It is the same idea as machine translation. 
In machine translation, we translate the source code from one language to another language 
but here, input is transformed to an output. It needs a large amount of data and 
it is based on Deep Neural networks.

Here we make a retrieval based chatbot.

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

