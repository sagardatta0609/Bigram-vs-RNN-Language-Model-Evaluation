## Bigram vs RNN Language Model
Evaluation using Perplexity and BLEU Score

This project demonstrates a comparison between:

## Bigram (n-gram) Language Model

 Recurrent Neural Network (LSTM) Language Model

The evaluation is performed using:

 Perplexity (PPL) → measures prediction confidence

 BLEU Score → measures text generation quality

The entire implementation is designed to run inside one Google Colab cell for simplicity.

## Objective

To understand the difference between:

Traditional statistical language models (n-gram)

Neural language models (RNN / LSTM)

And compare them using standard NLP evaluation metrics.

## Models Implemented
1️⃣ Bigram Language Model
🔹 Features

Uses conditional probability:

P(word_t | word_{t-1})

Implements Add-k smoothing

Computes:

Sentence log probability

Perplexity

Random sentence generation

 Perplexity Formula
Perplexity = exp(- log_probability / N)

Lower perplexity = better model

2️⃣ RNN Language Model (LSTM)
🔹 Architecture

Embedding Layer

LSTM Layer

Fully Connected Layer

Cross-Entropy Loss

🔹 Training

Trained for 3 small epochs

Predicts next token

Evaluated on test perplexity

## Evaluation Metrics
🔹 1. Perplexity (PPL)

Measures how well the model predicts the next word.

Lower = Better

Used for:

Bigram model

RNN model

🔹 2. BLEU Score

Measures similarity between:

Generated sentences

Reference test sentences

Range:

0 → Completely different
1 → Perfect match
## Dataset

A small toy corpus is used:

"The quick brown fox jumps over the lazy dog"
"I love natural language processing"
"Language models predict the next word"
"RNNs and n-gram models are classic"
"This is a small test corpus"

Split into:

Training set

Validation set

Test set

## Installation

If needed, install dependencies:

pip install torch nltk
▶️ How to Run

Open Google Colab

Paste entire script into one cell

Run cell

Observe:

Bigram perplexity

RNN training loss

RNN test perplexity

Generated sentences

BLEU scores

## Example Output
Bigram perplexity on test: 45.321

Epoch 1 train_loss=...
Epoch 2 train_loss=...
Epoch 3 train_loss=...
test_ppl=...

Bigram BLEU: 0.05
RNN BLEU: 0.12
🔍 Key Differences Observed
Feature	Bigram	RNN
Context size	1 previous word	Long sequence
Memory	No	Yes (LSTM hidden state)
Perplexity	Higher	Lower
BLEU	Lower	Higher
Flexibility	Limited	More powerful
## Concepts Demonstrated

N-gram language modeling

Add-k smoothing

LSTM networks

Tokenization

Vocabulary building

Sequence modeling

Cross-entropy loss

Perplexity

BLEU score

Text generation

## Educational Use

Ideal for:

NLP Lab Experiments

Language Modeling coursework

Understanding perplexity

Comparing classical vs neural models

Viva preparation

## Possible Improvements

Increase dataset size

Add Trigram model

Add GRU comparison

Train longer epochs

Add Transformer model comparison

Plot loss vs epoch graph

Use larger real dataset (WikiText)
