# LA-Reddit-Text-Mining-Analysis
Text mining and NLP analysis of r/LosAngeles discussions using Python, classification, clustering, topic modeling, and sentiment analysis.
# Los Angeles Reddit Text Mining & NLP Analysis

## Project Overview

This project analyzes discussions from **r/LosAngeles** and **r/AskLosAngeles** to identify the major topics discussed by the Los Angeles Reddit community and examine how those topics differ in **sentiment and community engagement**.

The analysis covers approximately **300 days of Reddit activity**, from August 28, 2025, through June 24, 2026.

After data cleaning and preprocessing, the final dataset contained:

* **498,147 comments**
* **9,070 posts**

The project applies Natural Language Processing (NLP), text mining, topic modeling, clustering, sentiment analysis, and engagement analysis to transform large-scale unstructured Reddit conversations into interpretable insights.

---

## Research Question

**What are the dominant themes in Los Angeles-focused Reddit discussions over the past 300 days, and how do these themes differ in sentiment and community engagement?**

The analysis addressed four questions:

1. What are the most common discussion themes in r/LosAngeles and r/AskLosAngeles?
2. How does sentiment differ across these themes?
3. Which themes generate the highest levels of community engagement?
4. Are highly negative themes also the themes that receive the highest engagement?

---

## Data

Publicly available Reddit posts and comments were collected from:

* **r/LosAngeles**
* **r/AskLosAngeles**

Data sources included the Reddit API and Arctic Shift historical archive.

The raw data included post titles, post text, comments, timestamps, Reddit scores, comment counts, and post flairs.

A two-stage preprocessing pipeline was used to remove deleted or removed content, automated bot posts, duplicates, URLs, formatting artifacts, emojis, and non-English content. Text was also normalized and prepared for NLP and frequency-based modeling.

---

## Analytical Methods

The project combined multiple text analytics techniques:

### Exploratory Data Analysis

* Word-frequency analysis
* Bigrams and trigrams
* Word clouds
* Part-of-speech analysis
* Named Entity Recognition

### Topic Modeling

Three topic modeling approaches were evaluated:

* **Latent Dirichlet Allocation (LDA)**
* **Non-negative Matrix Factorization (NMF)**
* **BERTopic**

LDA provided the best balance between topic coherence, diversity, and interpretability and was selected as the primary topic model.

### Clustering

K-Means clustering was applied using:

* TF-IDF text representation
* Truncated SVD for dimensionality reduction
* Silhouette scores for cluster selection

### Sentiment Analysis

Multiple sentiment approaches were evaluated, including:

* TextBlob
* VADER
* Multilingual BERT
* Twitter-RoBERTa

Twitter-RoBERTa was selected for the final sentiment analysis.

### Engagement Analysis

Reddit metadata such as scores, comment counts, and topic-level comment volume were used to examine how community engagement differed across discussion themes.

---

## Key Findings

### 1. Housing was the dominant discussion theme

The selected LDA model identified five major themes in the comments:

* **Housing Affordability & Urban Issues — 25.5%**
* **Neighborhoods & Living Conditions — 21.0%**
* **Politics & Public Policy — 19.0%**
* **General Discussions & Everyday Experiences — 18.4%**
* **Community & Local Events — 16.3%**

Housing affordability and urban issues therefore represented more than one-quarter of analyzed comment activity.

### 2. Sentiment differed substantially by topic

All five major themes had net-negative sentiment.

**Politics & Public Policy** showed the strongest negative sentiment, followed closely by **Housing Affordability & Urban Issues**.

In contrast, **Neighborhoods & Living Conditions** was substantially less negative and contained a larger proportion of neutral discussion.

### 3. Reddit discussions behaved like an integrated civic forum

K-Means clustering identified three clusters within a 30,000-comment sample.

The largest cluster contained approximately **86.9% of sampled comments**, suggesting that housing, politics, transportation, safety, and other civic issues frequently overlap within the same conversations rather than forming completely separate discussion communities.

### 4. Negativity did not predict engagement

One of the most important findings was that **the most negative topics were not necessarily the most highly discussed topics**.

Politics & Public Policy was the most negative theme but ranked only third in comment volume. Neighborhoods & Living Conditions was the least negative theme but ranked second in discussion volume.

This suggests that **what the community discusses most and what it criticizes most are influenced by different factors**.

---

## Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* NLP / Text Mining
* TF-IDF
* Truncated SVD
* K-Means Clustering
* LDA
* NMF
* BERTopic
* spaCy
* VADER
* TextBlob
* BERT / RoBERTa
* Matplotlib
* Data Visualization

---

## Repository Contents

`LA_Reddit_Text_Mining_Analysis.ipynb` — Python notebook containing the project's analysis, modeling, visualizations, and results.

---

## Skills Demonstrated

This project demonstrates experience with:

* Natural Language Processing (NLP)
* Large-scale text data preprocessing
* Exploratory Data Analysis
* Unsupervised Machine Learning
* Topic Modeling
* Clustering
* Sentiment Analysis
* Model Comparison and Evaluation
* Data Visualization
* Translating unstructured data into interpretable insights

---

## Project Context & My Contribution

This project was completed as a collaborative team project for **GBA 6410 — Social Media Analytics and Text Mining** during Summer 2026.

### My Contribution

My primary contributions to the project included:

- Contributing to the **Exploratory Data Analysis (EDA)** of the Reddit dataset.
- Developing the complete **Topic Modeling analysis** for both Reddit posts and comments.
- Implementing and evaluating **Latent Dirichlet Allocation (LDA)**.
- Implementing and evaluating **Non-negative Matrix Factorization (NMF)**.
- Implementing and evaluating **BERTopic**.
- Comparing topic modeling approaches using metrics such as **topic coherence, topic diversity, perplexity, and model interpretability**.
- Identifying and interpreting the major discussion themes within the Los Angeles Reddit community.
- Contributing to the interpretation and presentation of the project's findings.

The remaining components of the project were completed collaboratively by the research team.
