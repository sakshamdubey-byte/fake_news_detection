# Fake News Detection

A machine learning project designed to detect and classify fake news articles.

## Run on Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sakshamdubey-byte/fake_news_detection/blob/main/Fake_News_Prediction.ipynb)

# 📰 Fake News Prediction using Machine Learning

Hey there! This is a personal machine learning project where I built a Python model to classify news articles as either **Real** or **Fake**. 

With misinformation spreading so quickly online, I wanted to see how text preprocessing and classification algorithms could be used to flag untrustworthy articles automatically based on their text content.

---

## 🗺️ What's Inside?

- [What This Project Does](#-what-this-project-does)
- [The Data I Used](#-the-data-i-used)
- [How I Built It](#-how-i-built-it)
- [How to Run It Yourself](#-how-to-run-it-yourself)
- [Required Packages](#-required-packages)

---

## 🔍 What This Project Does

The core objective here is **binary text classification**. The system takes raw text data (like a news headline or the full article body), processes the language, and uses a trained machine learning model to predict whether the news is legitimate or completely fabricated.

---

## 📊 The Data I Used

For this project, I used a standard Fake News dataset containing thousands of flagged articles. The key features processed from the data include:
* **Title:** The headline of the news article.
* **Author:** The person who wrote the article.
* **Text:** The main body text of the article.
* **Label:** The ground truth (e.g., `0` for Real news, `1` for Fake news).

---

## ⚙️ How I Built It

Here is the step-by-step workflow followed inside the Jupyter notebook:

1. **Data Cleaning:** Handled missing values by replacing blank author or title fields with empty strings.
2. **Text Preprocessing (The Crucial Part):** 
   * Combined the `Author` and `Title` fields to create a unique text signature for each article.
   * **Stemming:** Reduced words to their root forms (e.g., "running", "runs" $\rightarrow$ "run") using NLTK's `PorterStemmer` to cut down on noise.
   * **Stopwords Removal:** Stripped out common filler words ("the", "is", "and") that don't add actual meaning to the classification.
3. **Feature Extraction:** Converted the cleaned text into numerical data using `TfidfVectorizer` (Term Frequency-Inverse Document Frequency) so the model could interpret the text patterns.
4. **Model Training:** Split the data into training/testing sets and trained a **Logistic Regression** model (or your specific model, e.g., PassiveAggressiveClassifier) on the vectors.
5. **Evaluation:** Checked performance using accuracy scores to ensure it successfully differentiates between real and fake reporting.

---

## 🚀 How to Run It Yourself

### 1. Run Instantly on Google Colab
The absolute easiest way to see this code in action without installing anything on your computer is to click the badge below:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sakshamdubey-byte/fake_news_detection/blob/main/Fake_News_Prediction.ipynb)

### 2. Run Locally
If you prefer to run it on your own machine:

1. Clone this repository:
```bash
   git clone [https://github.com/sakshamdubey-byte/fake_news_detection.git](https://github.com/sakshamdubey-byte/fake_news_detection.git)
