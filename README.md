# ✈️ Airline Tweet Sentiment Analysis using Machine Learning

This project builds a **sentiment classification model** for airline-related tweets using multiple **text representation techniques** and a **Random Forest Classifier**.  
The dataset used is the [Twitter Airline Sentiment dataset](https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment/data) from Kaggle.

---

## 📘 Project Overview
The goal of this project is to analyze public sentiment toward airlines on Twitter.  
We experiment with five text representation methods to understand which one performs best for tweet data:

1. **Bag-of-Words (BoW)**
2. **TF-IDF**
3. **Word2Vec** (trained myself)
4. **GloVe** (pre-trained embedding)
5. **FastText** (pre-trained embedding)

A **Random Forest classifier** is used as the main model, with **hyperparameter tuning** and **stratified 10-fold cross-validation**.

---

## 🧹 Text Preprocessing
Tweets are preprocessed before modeling to ensure text consistency and clarity:
- Lowercasing  
- Removing punctuation, numbers, mentions, hashtags, and URLs  
- Removing stopwords  
- Tokenization and lemmatization  

These steps help improve text quality and representation performance.

---

## ⚖️ Handling Imbalanced Data
The dataset showed imbalance across sentiment classes (negative, neutral, positive).  
To fix this, we applied **SMOTE (Synthetic Minority Oversampling Technique)** to oversample the minority classes.

This balancing step led to a more stable model and improved recall and F1-scores for underrepresented sentiments.

---

## 🤖 Model & Training
Algorithm used: **Random Forest Classifier**

### 🔧 Hyperparameter Tuning
Two main parameters were tuned using **GridSearchCV**:
- `n_estimators` (number of trees)
- `max_depth` (maximum tree depth)

Evaluation was performed using **Stratified 10-Fold Cross-Validation** to preserve class balance during model training and validation.

---

## 🧠 Tech Used
- **Python 3.12**
- **scikit-learn**
- **gensim**
- **imbalanced-learn**
- **pandas**, **numpy**
- **matplotlib**, **seaborn**

---

## 📎 Dataset Source
> [Twitter Airline Sentiment Dataset – Kaggle](https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment/data)

---

## 👩‍💻 Author
**Reamy Pie**  
Undergraduate Project – Sentiment Analysis using Machine Learning  
Data Science Major | 2025
