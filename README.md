# Restaurant Review Analysis using NLP and Clustering

## Project Overview

This project analyzes restaurant reviews using **Natural Language Processing (NLP)** and clusters restaurants based on **rating, cost, and sentiment**. The goal is to extract meaningful insights, visualize customer sentiments, and provide actionable business recommendations.

---

## Features

- **Text Cleaning & Preprocessing**
  - Lowercasing
  - Removal of non-alphabetic characters
  - Stopword removal
  - Tokenization
  - Lemmatization

- **Sentiment Analysis**
  - Calculate polarity using `TextBlob`
  - Assign sentiment labels: `positive`, `negative`, or `neutral`

- **Clustering**
  - Aggregate features per restaurant: average rating, cost, and sentiment
  - Feature scaling using `StandardScaler`
  - **KMeans Clustering** for grouping restaurants
  - Optional: Elbow method & dendrogram for determining optimal clusters

- **Visualization**
  - Scatter plot of restaurant clusters
  - Word clouds for positive, negative, and neutral reviews

- **Business Insights**
  - Identify high-rated affordable restaurants
  - Identify premium restaurants
  - Highlight restaurants that need improvement
  - Metrics: Avg Rating, Avg Cost, Avg Sentiment per cluster

---

## Project Workflow

1. **Data Merge**
   - Merge `restaurants` and `reviews` datasets on `Restaurant Key` using an inner join.

2. **Data Cleaning**
   - Clean and preprocess reviews using regex, NLTK tokenization, stopword removal, and lemmatization.

3. **Sentiment Analysis**
   - Compute `sentiment_score` using `TextBlob`
   - Label reviews as positive, negative, or neutral

4. **Feature Preparation**
   - Aggregate numerical features per restaurant (`Rating`, `Cost`, `sentiment_score`)
   - Scale features using `StandardScaler`

5. **Clustering**
   - Apply KMeans to group restaurants
   - Visualize clusters using scatter plots
   - Optional: Use Elbow method and hierarchical dendrogram to determine the optimal number of clusters

6. **Word Cloud Visualization**
   - Generate word clouds for positive, negative, and neutral reviews to understand frequent keywords

7. **Business Insights**
   - Provide cluster-wise recommendations
   - Present key metrics: Avg Rating, Avg Cost, Avg Sentiment

---

## Libraries Used

- `pandas` – Data manipulation and aggregation
- `numpy` – Numerical operations
- `matplotlib` & `seaborn` – Data visualization
- `nltk` – NLP preprocessing (tokenization, stopwords, lemmatization)
- `TextBlob` – Sentiment analysis
- `WordCloud` – Word cloud visualization
- `scikit-learn` – Feature scaling and KMeans clustering
- `scipy` – Hierarchical clustering (dendrogram)

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/restaurant-nlp-clustering.git
cd restaurant-nlp-clustering
