# TweetAuth

## Project Overview

*TweetAuth* is an authorship attribution project that classifies whether a tweet from Donald Trump's Twitter account was written by Trump himself or by one of his staffers. The ground truth is derived from the device metadata: tweets from Android devices are attributed to Trump, while others (e.g., iPhone) are attributed to staff.

## Dataset

* *Source*: A cleaned TSV file with \~2,000 labeled tweets and an unlabeled test set of 200 tweets.
* *Features used*:

  * Tweet text (tokens, embeddings)
  * Timestamp (converted to numeric features)
  * Device type (label)
  * Uppercase character count
  * Tweet length, word count, and more

## Models Implemented

The project compares five classification approaches:

1. *Logistic Regression* (scikit-learn)
2. *Support Vector Machine* (linear and RBF kernels)
3. *Feedforward Neural Network (FFNN)* built in PyTorch
4. *Random Forest* with engineered features
5. *Transformer-based model* (BERT)

Each model uses a standardized pipeline with preprocessing, feature extraction, training, and prediction steps.

## Evaluation

* Accuracy and confusion matrix plotted for each model
* Best-performing model selected based on validation accuracy
* Predictions on the test set saved in the required .txt format
