# Sentiment-Analysis-of-US-Election-2020-by-Analyzing-Tweeter-Trends
The 2020 US election is happening on the 3rd of November 2020, and the resulting impact on the world will no doubt be large, irrespective of which candidate is elected! After reading the dataset, I was inspired to attempt a sentiment analysis to understand the US Election vs. Twitter Trends.


# 🗳️ Sentiment Analysis of US Election 2020 Using Twitter Data

This project performs sentiment analysis on tweets related to the 2020 US Presidential Election, focusing on public opinion toward candidates Donald Trump and Joe Biden. By leveraging Natural Language Processing (NLP) techniques, we analyze tweet sentiments to understand voter inclinations and predict election outcomes.

## 📊 Project Overview

- **Goal**: Predict election trends using sentiment analysis of tweets.
- **Data Source**: [US Election 2020 Tweets Dataset](https://www.kaggle.com/datasets/manchunhui/us-election-2020-tweets/discussion?sort=hotness) from Kaggle.
- **Tech Stack**: Python, Pandas, NLTK, TextBlob, Plotly, WordCloud.

## 🧠 Key Concepts

- **Sentiment Analysis**: Classify tweets as Positive, Negative, or Neutral.
- **Polarity & Subjectivity**: Measure emotional tone and objectivity.
- **EDA**: Visualize tweet volume, likes, and country-wise activity.
- **Word Clouds**: Highlight dominant themes in candidate-related tweets.

## 📁 Dataset Features

Each tweet includes:
- `tweet_id`, `created_at`, `tweet`, `likes`, `retweet_count`
- User metadata: `user_name`, `user_location`, `followers_count`
- Geolocation: `lat`, `long`, `city`, `state`, `country`
- `candidate`: Trump or Biden (added during preprocessing)

## ⚙️ Installation

```bash
pip install nltk wordcloud textblob plotly pandas numpy matplotlib
```

Download NLTK resources:

```python
import nltk
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('omw-1.4')
```

## 🧹 Data Preprocessing

- Clean tweets using regex and lemmatization.
- Normalize country names (e.g., "United States" → "US").
- Merge Trump and Biden datasets with a `candidate` label.
- Drop missing values for reliable analysis.

## 📈 Exploratory Data Analysis

- Bar charts for tweet volume and likes per candidate.
- Country-wise tweet distribution.
- Sentiment breakdown (positive, neutral, negative).

## 🧪 Sentiment Analysis

Using TextBlob:
- `polarity`: Float between -1 (negative) and 1 (positive)
- `subjectivity`: Float between 0 (objective) and 1 (subjective)
- `analysis`: Categorized sentiment label

## 🌎 Insights

- Trump received more tweets but also more negative sentiment.
- Biden had a higher percentage of positive tweets.
- India showed more support for Biden, while most other countries tweeted more about Trump.

## 📌 Results

| Candidate | Positive (%) | Neutral (%) | Negative (%) |
|-----------|--------------|--------------|---------------|
| Trump     | 33.99        | 43.22        | 22.78         |
| Biden     | 36.43        | 46.83        | 16.73         |

## 📚 References
- [Kaggle Dataset](https://www.kaggle.com/datasets/manchunhui/us-election-2020-tweets/discussion?sort=hotness)
- [Kaggle Notebook](https://www.kaggle.com/code/mdusmanansari/sentiment-analysis-of-us-election-2020/edit)

## 👨‍💻 Author

Project inspired and adapted from [Manch Hui](https://www.kaggle.com/datasets/manchunhui/us-election-2020-tweets/data). Extended and refined by MD Usman Ansari for academic and research purposes.
