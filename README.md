# 🧠 Multi-Task Tweet Classification using ModernBERT

This project implements a multi-task learning framework using ModernBERT to classify tweets across multiple TweetEval tasks.

## Tasks Covered
- Emoji Classification
- Emotion Detection
- Sentiment Analysis
- Irony Detection
- Hate Speech Detection
- Offensive Language Detection
- Stance Detection

## Problem Formulation
Multi-task, single-label classification:
- One task per sample
- One label per task
- Missing labels masked with -100

## Dataset
I used the **TweetEval dataset**:

🔗 https://huggingface.co/datasets/cardiffnlp/tweet_eval

Dataset Structure:
- 33 CSV files:
- emoji_train.csv,&nbsp;&nbsp;&nbsp;emotion_train.csv,&nbsp;&nbsp;&nbsp;hate_train.csv .... etc.


## Training
- Trained ModernBERT using CrossEntropyLoss per task

## 🔮 Inference
Example:
predict("I love this 😁")

Output:
{'emoji': 16 - "😁 (beaming)",&nbsp;&nbsp;&nbsp;'sentiment': 1 - "neutral",&nbsp;&nbsp;&nbsp;'emotion': 1 - "joy" .... and so on for every task}

## Installation
pip install torch transformers pandas tqdm

## ⚙️ Usage
1. Load data
2. Train model
3. Validate
4. Predict


## 📄 License
MIT
