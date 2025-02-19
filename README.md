🎬 Movie Recommender System
- This project is a Chinese movie recommendation system that suggests movies based on genres, famous actors, endings, voting, and ratings. 
The dataset consists of 90 Chinese movies from IMDb, and multiple machine learning techniques are used to analyze and predict movie popularity.

📂 Dataset and Sources
- Dataset & Distance Matrices: [Link](https://drive.google.com/drive/folders/1N36PT7d21R0kRzbwhGVBNLkApC9oHSf2?usp=sharing)
- Movie List Source: [IMDb](https://www.imdb.com/list/ls549262458/?ref_=ext_shr_lnk)
- Logistic Regression Reference: [Machine Learning Plus](https://www.machinelearningplus.com/machine-learning/logistic-regression-tutorial-examples-r/)
- Confusion Matrix Guide: MachineLearningMastery.com

📖 Project Overview
- The goal of this project is to recommend movies based on similarity metrics and analyze the relationship between movie features and popularity.

Feature	Description
- 🎥 Movies	90 Chinese movie series (1998 - 2024)
- 🎭 Genres	Comedy, Drama, Crime, Romance, Action, Adventure, Mystery, Fantasy
- ⏳ Runtime:	40 - 90 mins
- ⭐ IMDB Ratings:	6.4 - 8.6
- 🏆 Famous Actors:	Shi Shi Liu, Dilraba Dilmurat, Yang Yang, etc.
- 🎬 Ending Types:	Happy, Sad, Open
- 🗳️ Voting Data:	14 - 5,669 votes

🛠️ Methods Used:
1. Movie Recommendation via Distance Metrics
- Euclidean & Manhattan distance
- Finds the top 5 recommended movies based on a list of 5 watched movies.
2. K-Means Clustering for Classification
- Groups movies based on:
  - Genres & Ratings
  - Famous actors & Ratings
  - Movie endings & Ratings
  - Voting & Ratings
- Determines patterns in movie ratings.
3. Machine Learning Models for Popularity Prediction
- KNN (K-Nearest Neighbors)
  - Classifies high-rated vs. not-high-rated movies.
  - Accuracy: 70% | Misclassification: 30%
- Decision Tree
  - Predicts high-rating movies.
  - Accuracy: 80% | Misclassification: 20%
- Logistic Regression
  - Models the probability of high ratings based on selected features.
  - Accuracy: 76.7% | Misclassification: 23.3%
  
📊 Results & Key Findings
1. Movie Recommendation:
- Based on the Euclidean & Manhattan distance, the system suggests 5 similar movies.
- Example Recommendations:
  - Kill Me Love Me
  - Love Me, Love My Voice
  - Here We Meet Again
  - The Imperial Coroner
  - Bohe zhi xia
2. Best Predictive Model:
- Decision Tree had the highest accuracy (80%).
- High voting count was the most important factor in predicting high-rated movies.
3. Clustering Insights:
- High voting movies tend to have higher ratings.
- Happy-ending movies generally receive lower ratings than sad or open-ended movies.

📊 Data Visualization
- Treemap Chart: Highlights top-rated movies, such as Follow Your Heart (8.6) and Hidden Love (8.6).
- Pie Chart: Shows the percentage of genres, with Drama being the most dominant (48.89%).

🛡️ Ethics & Privacy Considerations
- The dataset is limited to 90 movies, which may introduce biases.
- Cultural bias exists as only Chinese movies are considered.
- The "Famous Actor" category is subjective and may change over time.
- Ratings are sourced from IMDb, but additional sources could strengthen the analysis.
  
🚀 Future Improvements
- Expanding the dataset for better clustering results.
- Analyzing additional factors like critic reviews, audience comments, and streaming data.
- Exploring budget, revenue, and profit analysis to predict a movie's success.
- Investigating seasonal movie trends and how audience preferences shift over time.
