# Chat Bot README

Welcome to the Chat Bot project! This repository contains a Python script that implements a simple conversational bot using TensorFlow and natural language processing techniques.

## Overview

This project involves training a neural network to understand and generate responses for different user inputs. The chat bot uses a predefined set of patterns and responses to simulate a conversation with users.

## Code Structure

The main script is `chat_bot.py`, which contains the implementation of the chat bot. The code is divided into several sections:

### Data Preparation

- The script starts by importing necessary libraries, such as Pandas, NumPy, TensorFlow, and more.
- It loads the conversation data from `data.json`, which contains patterns and responses organized by labels.

### Preprocessing

- The script defines a function `cleanText` to preprocess text data by removing non-alphanumeric characters and converting text to lowercase.
- It prepares the training examples and labels by iterating through the data and extracting patterns and labels.

### Label Encoding and Tokenization

- The script uses Scikit-Learn's `LabelEncoder` to encode labels into numerical values.
- It employs TensorFlow's `Tokenizer` to convert words into numerical sequences representing their importance.

### Padding

- The sequence of tokenized words is padded to ensure consistent input sizes for the neural network using `pad_sequences`.

### Model Definition

- A sequential neural network model is defined using Keras layers, including an embedding layer, global average pooling, and several dense layers.
- The model is compiled with categorical cross-entropy loss and the Adam optimizer.

### Model Training

- The model is trained on the padded sequences and corresponding labels.

### User Interface

- A user interface function `userChat` is defined to simulate a conversation with the bot.
- Users can interact with the bot by typing messages, and the bot will respond accordingly.

## Getting Started

1. Ensure you have Python and the required libraries installed (Pandas, NumPy, TensorFlow).
2. Download the repository and navigate to its directory.
3. Run the `chat_bot.py` script to start a conversation with the bot.
4. Type your messages and enjoy the interaction!

## Notes

- To exit the conversation, type "Quit".

Feel free to explore, modify, and expand upon this project to enhance the chat bot's capabilities and user experience. Have fun chatting with your AI bot assistant!
