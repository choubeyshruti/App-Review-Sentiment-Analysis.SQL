# App-Review-Sentiment-Analysis.SQL
AppPulse: Deep Dive into Google Play Store Reviews
## 📝 Project Description
This project is a complete data analytics pipeline that performs deep sentiment analysis on Google Play Store app reviews, combining raw data cleaning, SQL database modeling, NLP-based sentiment tagging, and Power BI dashboard visualizations.

I built this project to simulate real-world end-to-end data analysis, where raw, unstructured data from Kaggle  is transformed into actionable insights through advanced analytics and business intelligence tools.


## 🧠 My Approach :-

## ✅ Phase 1: Data Extraction & Cleaning
Imported large datasets from Kaggle:
**googleplaystore.csv
user_reviews.csv**
Loaded them into MySQL database named app_reviews_analysis.
Cleaned:
Ratings (ensuring values between 0–5)
Review text (removed noise, handled missing values)
Dates, prices, installs (converted and standardized)
Created cleaned tables: googleplaystore_cleaned, reviews_cleaned

## ✅ Phase 2: Text Analysis & Sentiment Classification (Python in Jupyter)
Used TextBlob and VADER to assign sentiment labels (Positive, Negative, Neutral)
Preprocessed text:
Removed stopwords
Lowercased text
Tokenized and lemmatized for better analysis
Matched review text to apps using fuzzy matching (via fuzzywuzzy)
Joined final sentiment-tagged reviews to store metadata
Created final_review_store_joined table

## ✅ Phase 3: Power BI Dashboard Development
Designed a 4-page interactive dashboard in Power BI with deep analytical visuals:

## 📊 Power BI Pages & Insights
## 📌 Page 1: App Market View
a).KPIs: Total apps, total installs, average price, average rating
b).Tree Map: Most installed categories
c).Bar Chart: Top 10 most downloaded apps
d).Donut Chart: Free vs Paid app distribution
e).Line Chart: App update trend over time
## App Market View Snapshot (Dashboard) :- 
![Screenshot (150)](https://github.com/user-attachments/assets/629ef93e-cc4b-4fb3-8d26-60af6c686254)

## 📌 Page 2: Sentiment Overview
a).Pie Chart: Sentiment distribution (Positive, Neutral, Negative)
b).Bar Chart: Top 10 apps with most negative reviews
c).Table: Real user reviews + visual data bars
d).Conditional formatting: Color-coded sentiment
## Sentiment Overview Snapshot (Dashboard) :-
![Screenshot (151)](https://github.com/user-attachments/assets/99f9c983-b139-4d3f-ad3e-27a5fa5bfdcc)

## 📌 Page 3: Ratings Mismatch
a).Scatter Chart: Official Play Store Rating vs User Sentiment
b).Bar Chart: Apps with the highest rating mismatch
c).Stacked Column: Review count by content rating
## Ratings Mismatch Snapshot (Dashboard) :- 
![Screenshot (152)](https://github.com/user-attachments/assets/c719a3e7-44e7-49f6-8dcb-8c93a7913b97)

## 📌 Page 4: Price Vs Experience
a).Box Plot: Price range vs user sentiment
b).Donut Chart: Review volume by app pricing
c).Clustered Bar: Top-rated paid apps
d).Card Visual: Average price of paid apps
e).Combo Chart: Installs vs Ratings (for paid apps)
## Price Vs Experience Snapshot (Dashboard) :-
![Screenshot (153)](https://github.com/user-attachments/assets/5cb9bde9-b392-435e-a24a-6e314a88d9a4)

## 💡 Tools & Tech Stack

Category             | Tools Used
Languages            | SQL, Python
Libraries            | pandas, nltk, TextBlob, VADER, fuzzywuzzy, matplotlib, seaborn
Database             | MySQL
Data Sources         | Kaggle (Google Play Store + Reviews Dataset)
Visualization        | Power BI
Environment          | Jupyter Notebook

## 📌 Key Features:-
1.🔄 ETL Pipeline: From CSV to MySQL to final BI dashboard
2.🤖 Sentiment Classification: Custom rule-based & NLP-enhanced tagging
3.🧠 Smart Matching: Used fuzzy logic to align reviews with proper app metadata
4.📈 Business Insight Driven Visuals: Created with decision-making in mind
5.🎯 Real-World Simulation: Large dataset, data mismatches, duplicate handling, and optimization

## 🔧 Key Sorting & Processing Techniques 
1.🧹 Data Cleaning (SQL): Removed outliers (invalid ratings, installs, prices) using regex, casting, and conditional filters.
2.🔗 App Matching via Fuzzy Logic: Matched inconsistent app names across datasets using fuzzywuzzy + Levenshtein.
3.📦 Sentiment Classification: Applied TextBlob & VADER to classify reviews into Positive, Negative, Neutral.
4.🔄 Joining Datasets: Used custom app_key (cleaned text) to match reviews and store data accurately.
5.📊 Top N Filtering: Visualized top 10/15 apps by installs, ratings, and sentiment mismatch in Power BI.

6. ## 🧮 DAX Measures (Power BI):
AvgUserRating
RatingDiff
PositiveSentimentPct

7.📈 Price Binning: Used DAX SWITCH to group prices into bins like “Free”, “$0–5”, “$5–10”, “$10+”.
8.📋 SQL Aggregations: Used GROUP BY, JOIN, and COUNT to group and analyze key metrics.

## ✅ Key Results (Insights from Analysis)
1.📊 App Rating vs Review Sentiment Mismatch: Identified apps with high store ratings but poor user sentiment — suggesting misleading store ratings.
2.💰 Price vs Experience: Found no strong correlation between app price and user satisfaction; some free apps performed better than paid ones.
3.🏆 Top Paid Apps: Highlighted top-rated paid apps based on average user sentiment scores.
4.📉 Negative Feedback Drivers: Identified most negatively reviewed apps to flag quality issues or user dissatisfaction.
5.🧠 Sentiment Distribution:
Positive: 62%
Neutral: 19%
Negative: 19%
6.🔍 Free vs Paid Review Patterns: Free apps received more consistent engagement, paid apps had more polarizing sentiments.
7.💡 User Behavior Trends: Analyzed install counts, app categories, and sentiment by content rating for deeper user experience understanding.









