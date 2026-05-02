# 📧 SMS Spam Classification: Applying SMS Detection Techniques to Email Datasets



## 📖 Overview

This project develops a \*\*text classification model\*\* to detect spam emails using Natural Language Processing (NLP) and Machine Learning. It applies techniques originally used in SMS spam detection to an email dataset, aiming to filter unwanted communication and protect users from phishing and scam attempts.



The project compares two classifiers — \*\*Multinomial Naive Bayes\*\* and \*\*Decision Tree\*\* — and evaluates them using Precision, Recall, F1-score, and Confusion Matrix.



\---



## 📁 Project Structure

spam-classification/

│

├── Project2\_SMS\_Spam\_Classification.ipynb  

├── requirements.txt           

├── .gitignore                             

└── README.md     



\---



## 🗂️ Dataset

\- \*\*Source:\*\* \[SetFit/enron\_spam](https://huggingface.co/datasets/SetFit/enron\_spam) via HuggingFace `datasets`

\- \*\*Description:\*\* A real-world email dataset with spam (1) and ham (0) labels

\- \*\*Preprocessing:\*\* Duplicates removed, missing values filled, label/text columns retained



\---



## 🔍 Project Workflow



### 1. Exploratory Data Analysis

\- Class distribution visualization (Spam vs Ham)

\- Feature engineering: `word\_count`, `contains\_currency\_symbols`, `contains\_number`

\- Analysis of spam indicators through countplots and histograms



### 2. Text Preprocessing

\- Removal of non-alphabetic characters using regex

\- Lowercasing and stopword removal (NLTK)

\- Lemmatization using `WordNetLemmatizer`

\- TF-IDF Vectorization (`max\_features=10000`, bigrams)



### 3. Model Training \& Evaluation

| Model | Accuracy | F1-Score (CV) |

|---|---|---|

| Multinomial Naive Bayes | \~98% | Higher \& consistent |

| Decision Tree | \~92% | Lower \& more variance |



> ✅ \*\*Naive Bayes\*\* outperforms Decision Tree in both accuracy and consistency, making it the preferred model for real-time spam filtering.



### 4. Live Prediction

A `predict\_spam(subject, body)` function applies the full preprocessing pipeline and returns whether an email is spam or ham.



\---



## 🛠️ Requirements



\- Python 3.8+

\- Jupyter Notebook / JupyterLab



Install all dependencies:

```bash

pip install -r requirements.txt

```



Key libraries:

\- `datasets` — Load the Enron spam dataset from HuggingFace

\- `pandas`, `numpy` — Data manipulation

\- `matplotlib`, `seaborn` — Visualization

\- `nltk` — Stopwords and lemmatization

\- `scikit-learn` — TF-IDF, model training, and evaluation



\---



## 🚀 Getting Started



1\. \*\*Clone the repository\*\*

```bash

&#x20;  git clone https://github.com/yourusername/spam-classification.git

&#x20;  cd spam-classification

```



2\. \*\*Install dependencies\*\*

```bash

&#x20;  pip install -r requirements.txt

```



3\. \*\*Launch Jupyter\*\*

```bash

&#x20;  jupyter notebook

```



4\. \*\*Open and run\*\* `Project2\_SMS\_Spam\_Classification.ipynb`



\---



## 📊 Results



\- \*\*Multinomial Naive Bayes\*\* achieved \~98% accuracy with very few false negatives (missed spam), making it highly reliable for spam detection.

\- \*\*Decision Tree\*\* achieved \~92% accuracy but showed more misclassifications, particularly misidentifying ham as spam.

\- Naive Bayes was selected as the final model due to its higher F1-score, consistency, and speed.

&#x20;                         

