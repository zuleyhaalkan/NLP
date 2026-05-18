Sentiment Analysis with Bidirectional LSTM
Course Project — Artificial Intelligence | Ege University, Dept. of Computer Engineering

Overview
This project implements a sentiment analysis pipeline using a Bidirectional LSTM neural network with pre-trained GloVe word embeddings. The model is trained on the IMDB movie reviews dataset (50,000 reviews) to classify text as positive or negative. The project is then extended to a real-world application: live Twitter sentiment analysis using the Twitter API.

Project Structure
Part 1 — IMDB Sentiment Classifier

Text preprocessing: HTML tag removal, URL normalization, lowercasing (BeautifulSoup, regex)
Tokenization and sequence padding (Keras Tokenizer, max length 200)
GloVe 200-dimensional pre-trained word embeddings (6B tokens)
Bidirectional LSTM (64 units) with Dropout regularization
Dense layers (256 → 128 → 1) with sigmoid output
Training: 30 epochs, Adam optimizer, binary cross-entropy loss

Part 2 — Live Twitter Analysis

Twitter Developer API integration
Real-time tweet collection by hashtag or keyword (last 24 hours, English only)
Sentiment classification using the trained model
Results visualized as positive/negative percentage breakdown


Tech Stack

Python, Jupyter Notebook
TensorFlow / Keras
NLTK, BeautifulSoup, scikit-learn
GloVe embeddings (glove.6B.200d)
Tweepy (Twitter API)
Matplotlib, Seaborn


Dataset

IMDB Dataset: 50,000 movie reviews (25,000 positive / 25,000 negative)
Twitter: Live data collected via API at runtime


Results
The model achieves strong validation accuracy on the IMDB test set, with performance improving consistently across 30 training epochs. Training and validation accuracy/loss curves are plotted for evaluation.

Context
Developed as the final project for the Artificial Intelligence course at Ege University, Department of Computer Engineering, Spring 2021. The project extends a standard sentiment classification task into a real-time social media analysis tool, demonstrating end-to-end NLP pipeline design from data collection through model inference.
