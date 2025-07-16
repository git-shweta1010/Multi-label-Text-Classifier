# Multi-label Text Classifier (Emotion, Violence, Hate Speech)

This project is a multi-task text classification tool that identifies the **major category** (Emotion, Violence, or Hate Speech) and predicts a **sub-label** specific to that category using deep learning.

## 🚀 Features

- Classifies user input into:
  - **Emotion**: sadness, joy, love, anger, fear, surprise
  - **Violence**: sexual, physical, emotional, harmful traditional practices, economic
  - **Hate Speech**: offensive speech, hate speech, or neither
- Interactive text input using `ipywidgets`
- Built using a multi-branch deep learning model (Keras/TensorFlow)
- Preprocessing with stopword removal and tokenization

## 🧠 Model Architecture

The project uses a shared input pipeline with three output heads corresponding to the emotion, violence, and hate detection tasks. Each branch outputs a softmax probability distribution, from which the most confident prediction is selected.

## 🛠️ Tech Stack

- Python 3.x
- Jupyter Notebook
- TensorFlow / Keras
- NumPy
- ipywidgets
- NLTK / custom preprocessing

## 💡 How It Works

1. User inputs text via a widget interface
2. Text is cleaned, tokenized, and padded
3. Model predicts all three label sets simultaneously
4. The model outputs the most confident **major label**, and the corresponding **sub-label** is displayed


