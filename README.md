# 📰 Fake News Classifier using LSTM

This project implements a **Fake News Detection** system using **Deep Learning (LSTM)**.  
The goal is to classify news articles as **Real** or **Fake** based on their textual content.

---

## 📘 Project Overview

In an era where misinformation spreads rapidly, fake news detection has become essential.  
This project uses **Natural Language Processing (NLP)** techniques and a **Long Short-Term Memory (LSTM)** network to identify fake news articles.  
The model learns semantic patterns from the text to make accurate predictions.

---

## 📊 Dataset

**Source:** [Kaggle Fake News Dataset](https://www.kaggle.com/c/fake-news/data)

**Description:**  
The dataset contains labeled news articles, each tagged as **real (0)** or **fake (1)**.

| Column | Description |
|---------|--------------|
| `title` | Title of the news article |
| `text` | Main content of the article |
| `subject` | Topic category |
| `date` | Publication date |
| `label` | 0 = Real, 1 = Fake |

---

## ⚙️ Project Workflow

### 1. Data Preprocessing
- Removed missing and duplicate values  
- Combined `title` and `text` for context  
- Lowercased and cleaned text (punctuation, stopwords, special chars)  
- Tokenized and padded sequences for model input  

### 2. Feature Representation
Two text representations were compared:
- **One-Hot Encoding** – assigns a unique integer to each word.  
- **Word Embedding** – learns dense vector representations during training.

### 3. Model Architecture (LSTM)
- **Embedding Layer** – converts input words into dense vectors  
- **LSTM Layer** – captures long-term word dependencies  
- **Dense Layers** – classifies news as real or fake  
- **Activation:** Sigmoid  
- **Loss Function:** Binary Crossentropy  
- **Optimizer:** Adam  

---

## 🧠 Model Evaluation

| Metric | Real (0) | Fake (1) |
|---------|-----------|-----------|
| **Precision** | 0.91 | 0.89 |
| **Recall** | 0.92 | 0.89 |
| **F1-Score** | 0.92 | 0.89 |
| **Support** | 3419 | 2616 |

**Overall Accuracy:** 🎯 **90%**  
**Macro Avg F1-Score:** 0.90  
**Weighted Avg F1-Score:** 0.90  

---

## 🧩 Technologies Used

| Library / Tool | Purpose |
|----------------|----------|
| Python | Programming language |
| pandas, numpy | Data processing |
| nltk | Text preprocessing |
| TensorFlow / Keras | LSTM model building |
| scikit-learn | Evaluation metrics |
| matplotlib, seaborn | Visualization |# FakeNewsClassifierUsingLSTM
