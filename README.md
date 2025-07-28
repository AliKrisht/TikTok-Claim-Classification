# 🎯 TikTok Claim Classification with XGBoost

This project uses machine learning to classify TikTok videos as either **claims** or **opinions** based on video metadata, engagement metrics, and text length. It is designed to support content moderation and misinformation detection on social media platforms.

---

## ✅ Objective

To build a robust classification model that distinguishes between claims and opinions in TikTok video captions, using structured metadata and engagement features.

---

## 📦 Methods Used

### 1. Data Cleaning
- Filtered a dataset of over 19,000 TikTok videos
- Removed outliers in features like views, likes, comments, and shares
- Handled missing and malformed records

### 2. Feature Engineering
- Created `video_transcription_text_length` and `len_text` for NLP-based features
- Encoded target variable `claim_status` to binary (0 = opinion, 1 = claim)
- One-hot encoded categorical features (e.g., verified_status, author_ban_status)

### 3. Modeling
- Split data into training, validation, and test sets
- Evaluated Logistic Regression, Random Forest, and XGBoost models
- Tuned XGBoost with GridSearchCV for best performance

---

## 🔑 Key Findings

- Verified users are more likely to post **opinions**, while unverified users post more **claims**
- **Text length**, **comment count**, and **share count** are strong predictors
- No additional feature engineering was needed once key features were included
- XGBoost performed exceptionally well with the current features

---

## 🏆 Best Model Results (XGBoost Classifier)

| Metric     | Score |
|------------|-------|
| Accuracy   | 1.00  |
| Precision  | 0.99  |
| Recall     | 1.00  |
| F1 Score   | 1.00  |

The model achieved **perfect classification** performance on both validation and test datasets.

---

## 👤 Author

**Ali Krisht**  
