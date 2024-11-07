# ChatBot 
ChatBot for University purpose:
The chatbot elevates the university website, providing valuable information to users, students & parents.📚💡

IT WAS LIVE ON JAYPEE UNIVERSITY'S OFFICIAL WEBSITE (https://www.juit.ac.in/) 
<br>Currently have more than 2500+ active users.

**Chatbot Link** : https://strident-narrow-goatfish.anvil.app/ 

![image](https://github.com/TusharPaul01/ChatBot-ML-LSTM-/assets/97314846/fda8d0a2-8421-4106-8f93-7d754a2416f7)
![image](https://github.com/TusharPaul01/ChatBot-ML-LSTM-/assets/97314846/918810ce-102c-4346-9d71-a583aeacf847)

Steps & Explaination :

The code you provided appears to be a chatbot implementation using a neural network model for intent classification. It consists of two parts: training the chatbot model and using the trained model for chatbot interaction.

In the training part:
1. The code loads the training data from a JSON file (`intents.json`) containing text examples and corresponding intents.
2. The text examples and intents are extracted from the data and stored in separate lists.
3. The text data is tokenized using the `Tokenizer` class from Keras and converted to sequences.
4. The tokenizer is saved to a pickle file (`tokenizer.pickle`) for later use during chatbot interaction.
5. The sequences are padded to have equal length using the `pad_sequences` function.
6. The intents are encoded using the `LabelEncoder` from scikit-learn, and one-hot encoded using `tf.one_hot`.
7. The model architecture is defined using Keras layers, including an embedding layer, LSTM layer, and dense output layer.
8. The model is compiled with a categorical cross-entropy loss function and Adam optimizer.
9. The model is trained on the padded sequences and one-hot encoded intents for a specified number of epochs.

After training, the model is saved to a file (`chatbot_model.h5`) for later use during chatbot interaction.

In the chatbot interaction part:
1. The code loads the chatbot data from a JSON file (`intents_final.json`) containing text examples and intents.
2. The user input is obtained, and if the user types "quit," the program exits.
3. The user input is encoded using the saved tokenizer and padded to match the maximum sequence length used during training.
4. The model is loaded from the saved file (`chatbot_final.h5`).
5. The user input is passed through the model to predict the intent.
6. The predicted intent is mapped back to its original label using the label encoder.
7. A response is randomly selected from the intent's available responses and displayed as the chatbot's reply.

This model has been given an user interface by creating a web app using Anvil. That also requires web designing, building interconnection between model & webapp using python statements.
Finally, the model is deployed on AWS (Amazon Web Services) so that ML model can run 24/7 without any kind interruption. 

Note: Please make sure you have the necessary dependencies installed, such as TensorFlow and scikit-learn, before running this code. Also, ensure that you have the required JSON files (`intents.json` and `intents_final.json`) in the correct locations.



