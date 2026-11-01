Twitter Sentiment Analysis using DeBERTa-v3

A transformer-based Natural Language Processing (NLP) project that classifies tweets into four sentiment categories using Microsoft's DeBERTa-v3-base model.

Project Overview

This project uses a pretrained transformer model, DeBERTa-v3-base, fine-tuned on the Twitter Entity Sentiment Analysis dataset to identify the sentiment expressed in tweets.

The model predicts one of four classes:

Irrelevant

Negative

Neutral

Positive

Model

Base model: microsoft/deberta-v3-base

Task: Multi-class text classification

Number of classes: 4

Tokenizer: DeBERTa tokenizer

Maximum sequence length: 96

Dataset

Twitter Entity Sentiment Analysis

Dataset: Kaggle – Twitter Entity Sentiment Analysis

Files used:

twitter_training.csv

twitter_validation.csv

The dataset contains tweets labelled with sentiment categories.

Methodology

Load and inspect the dataset.

Clean and normalize tweet text.

Remove duplicate text entries.

Encode sentiment labels.

Split the training data into training and internal validation sets using stratification.

Tokenize text using the DeBERTa tokenizer.

Fine-tune DeBERTa-v3-base for four-class sentiment classification.

Evaluate model performance using classification metrics.

Training Configuration

Parameter

Value

Model

DeBERTa-v3-base

Epochs

4

Batch size

8

Gradient accumulation

2

Learning rate

2e-5

Optimizer

AdamW

Maximum sequence length

96

Mixed precision

FP16

GPU

NVIDIA Tesla T4

Results

Internal Validation Performance

Metric

Score

Accuracy

92.41%

Precision (weighted)

92.41%

Recall (weighted)

92.41%

F1-score (weighted)

92.39%

These metrics represent the latest four-epoch training run's internal validation results.

Project Structure

twitter-sentiment-analysis/
│
├── notebooks/
│   └── Twitter_Sentiment_Analysis.ipynb
│
├── results/
│   ├── training_history.csv
│   ├── independent_evaluation_results.csv
│   ├── independent_predictions.csv
│   └── plots/
│
├── README.md
├── requirements.txt
└── .gitignore

Technologies Used

Python

PyTorch

Hugging Face Transformers

DeBERTa-v3

Pandas

NumPy

Scikit-learn

Matplotlib

Seaborn

Kaggle Notebooks

Installation

Clone the repository:

git clone https://github.com/lalith-sky/twitter-sentiment-analysis.git
cd twitter-sentiment-analysis

Install dependencies:

pip install -r requirements.txt

Open the notebook:

jupyter notebook notebooks/Twitter_Sentiment_Analysis.ipynb

Future Improvements

Deploy the model through a REST API.

Build an interactive sentiment analysis interface.

Experiment with additional transformer architectures.

Improve generalization using larger and more diverse datasets.
