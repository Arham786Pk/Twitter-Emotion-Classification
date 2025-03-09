Working of the Twitter Emotion Classification - BERT Model
Load the Dataset

Reads training, validation, and test datasets containing tweets and their corresponding emotions.
Tokenization with BERT

Converts tweets into token IDs using BertTokenizer.
Pads/truncates sequences to a max length of 128.
Generates attention masks (to distinguish real words from padding).
Convert Labels to Numerical Format

Maps emotion labels to numeric indices for model training.
Build the BERT-Based Model

Uses a pre-trained bert-base-uncased model to extract meaningful features.
Takes input IDs and attention masks as inputs.
Uses the [CLS] token output as the sentence representation.
Applies:
Dropout layers (to prevent overfitting).
Dense layers for classification.
Softmax activation (to predict emotion categories).
Train the Model

Trains for 3 epochs with a batch size of 16.
Uses Adam optimizer with a learning rate of 2e-5.
Computes sparse categorical cross-entropy loss.
Evaluate the Model

Predicts emotions for the test set.
Computes accuracy and generates a classification report.
Purpose
This model classifies tweets into different emotions using a powerful BERT-based deep learning approach. 🚀
