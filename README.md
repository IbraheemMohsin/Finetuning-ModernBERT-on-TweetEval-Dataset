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
33 CSV files:
- emoji_train.csv, emotion_train.csv, hate_train.csv etc.


## Training
- CrossEntropyLoss per task

## Validation
- Separate validation loop

## 🔮 Inference
Example:
predict("I love this 😁")

Output:
{'emoji': 16 - "😁 (beaming)", 'sentiment': 1 - "neutral", 'emotion': 1 - "joy" .... and so on for every task}

## Installation
pip install torch transformers pandas tqdm

## ⚙️ Usage
1. Load data
2. Train model
3. Validate
4. Predict


## 📄 License
MIT
