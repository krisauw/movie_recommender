# **🎬 Movie Recommender System**

## **Project Overview**
This project is a Chinese movie recommendation system that suggests movies based on genres, famous actors, endings, voting, and ratings. 
The dataset consists of 90 Chinese movies from IMDb, and multiple machine learning techniques are used to analyze and predict movie popularity.

---

## **🛠️ Technologies and Methods Used**
### **Technologies**
* Python 🐍 (for data cleaning)
* Pandas 🏷️ (for data processing)
* Plotly 📊 (for interactive visualizations)
* R 📓 (for running the analysis)

### **Methods**
* Find similarity using distance metric which are Euclidean and Manhattan to recommend top 5 recommendation movies based on a list of watched 5 movies.
* Classify different movie groups using k-means with different features and k value
* Use KNN to predict a popular movie based on feature selections through train and test data.
* Apply a decision tree to guess high rating movies based on feature selections through train and test data.
* Analyze a logistic Regression to portrait probability of high rating based on selected features.

---

## **🔑 Key Findings**
For movie recommendations, both Euclidean and Manhattan distance metrics work effectively. Regarding unsupervised methods like K-Means clustering, the results are inconsistent and lack meaningful grouping. Although famous leads may influence ratings, the small dataset limits the validity of such conclusions. For supervised methods such as KNN, Decision Tree, and Logistic Regression, all demonstrated high and relatively similar accuracy rates with low misclassification rates, as summarized in the table below:

![Image](https://github.com/user-attachments/assets/af215af5-ee79-443d-9147-459a884ef141)

### **Movie Recommendation**
#### **Based on the Euclidean & Manhattan distance, the system suggests 5 similar movies**
(Example Recommendations)
 * Kill Me Love Me
 * Love Me, Love My Voice
 * Here We Meet Again
 * The Imperial Coroner
 * Bohe zhi xia
   
#### **Best Predictive Model**
* Decision Tree had the highest accuracy (80%).
* High voting count was the most important factor in predicting high-rated movies.
  
#### **Clustering Insights**
* High voting movies tend to have higher ratings.
* Happy-ending movies generally receive lower ratings than sad or open-ended movies.

---

## **📂 Dataset**
### **Key Features**
- 🎥 Movies:	90 Chinese movie series (1998 - 2024)
- 🎭 Genres:	Comedy, Drama, Crime, Romance, Action, Adventure, Mystery, Fantasy
- ⏳ Runtime:	40 - 90 mins
- ⭐ IMDB Ratings:	6.4 - 8.6
- 🏆 Famous Actors:	Shi Shi Liu, Dilraba Dilmurat, Yang Yang, etc.
- 🎬 Ending Types:	Happy, Sad, Open
- 🗳️ Voting Data:	14 - 5,669 votes

### **Dataset Variables**

This dataset contains information on **90 Chinese movie series (1998-2024)**. Below is a detailed breakdown of the variables included:

| #  | Variable Name      | Description |
|----|--------------------|-------------|
| 1  | `ID`               | The order numbers of variables. |
| 2  | `Title`            | The movie’s English titles. |
| 3  | `Original_Title`   | The movie’s Chinese titles. |
| 4  | `Runtime`          | The runtime of one episode (in minutes). |
| 5  | `Ending`           | The type of movie ending: `happy`, `sad`, or `open`. |
| 6  | `Ending_Happy`     | `1` if `Ending` is happy, otherwise `0`. |
| 7  | `Ending_Sad`       | `1` if `Ending` is sad, otherwise `0`. |
| 8  | `Ending_Open`      | `1` if `Ending` is open-ended, otherwise `0`. |
| 9  | `Genres`           | The movie genre (Comedy, Drama, Crime, Romance, Action, Adventure, Mystery, Fantasy). |
| 10 | `Genre_Comedy`     | `1` if Comedy, otherwise `0`. |
| 11 | `Genre_Drama`      | `1` if Drama, otherwise `0`. |
| 12 | `Genre_Crime`      | `1` if Crime, otherwise `0`. |
| 13 | `Genre_Romance`    | `1` if Romance, otherwise `0`. |
| 14 | `Genre_Action`     | `1` if Action, otherwise `0`. |
| 15 | `Genre_Adventure`  | `1` if Adventure, otherwise `0`. |
| 16 | `Genre_Mystery`    | `1` if Mystery, otherwise `0`. |
| 17 | `Genre_Fantasy`    | `1` if Fantasy, otherwise `0`. |
| 18 | `Male_Lead`        | The name of the male lead. |
| 19 | `Male_Famous`      | `1` if the male lead is in the list of famous actors, otherwise `0`. |
| 20 | `Female_Lead`      | The name of the female lead. |
| 21 | `Female_Famous`    | `1` if the female lead is in the list of famous actresses, otherwise `0`. |
| 22 | `Main_Famous`      | `1` if at least one main lead is famous, otherwise `0`. |
| 23 | `Release_Date`     | The release date of the movie. |
| 24 | `Is_Summer`        | `1` if released in July, August, or September, otherwise `0`. |
| 25 | `Year`             | The release year of the movie. |
| 26 | `Num_Votes`        | The number of votes the movie received. |
| 27 | `High_Voting`      | `1` if `Num_Votes` >= 1000, otherwise `0`. |
| 28 | `IMDB_Rating`      | The IMDb rating of the movie. |
| 29 | `High_Rating`      | `1` if `IMDB_Rating` >= 8, otherwise `0`. |
| 30 | `Viet_Title`       | The Vietnamese title (personal reference). |

### 🔹 Notes:
- `Ending_Happy`, `Ending_Sad`, and `Ending_Open` are derived from the `Ending` column.
- `Genre_*` variables are one-hot encoded representations of `Genres`.
- `Male_Famous` and `Female_Famous` are binary indicators based on a predefined list of famous actors.
- `High_Voting` and `High_Rating` categorize movies based on the number of votes and IMDb ratings.

---

## **🛠️ Result and Visualiations**
### **General Data Distribution**
#### **Treemap Chart**: Highlights top-rated movies, such as Follow Your Heart (8.6) and Hidden Love (8.6).

![Image](https://github.com/user-attachments/assets/7f046c03-0287-41c8-bc39-80f9f49fba4f)

#### **Pie Chart**: Shows the percentage of genres, with Drama being the most dominant (48.89%).

![Image](https://github.com/user-attachments/assets/379a0bb8-10a2-43b7-9b49-af55d6b23f45)

### **Movie Recommendation via Distance Metrics - Euclidean & Manhattan distance**
Firstly, 5 titles which are 'Yuan lai wo hen ai ni', 'Lost You Forever', 'Mischievous Kiss', 'Amidst a Snowstorm of Love', and 'My Fair Princess' are selected randomly in R from the list of 90 movie dataset as a list of watched movies. 

Secondly, distances of all movies are calculated including 5 watched movies using Euclidean and Manhattan. There are 15 features to find similarities between movies, which are 'Title', 'Ending_Happy', 'Ending_Sad', 'Ending_Open', 'Genre_Comedy', 'Genre_Drama', 'Genre_Crime', 'Genre_Romance', 'Genre_Action', 'Genre_Adventure', 'Genre_Mystery', 'Genre_Fantasy',  'Female_Famous', 'Male_Famous', 'Main_Famous', 'Is_Summer', 'High_Voting', and 'High_Rating'. Except for Title, others are binary variables.

Thirdly, there are 5 sub steps to get the list of 5 movie recommendations:
Step 1: Find distances for 5 watched movies - ‘'Yuan lai wo hen ai ni', 'Lost You Forever', 'Mischievous Kiss', 'Amidst a Snowstorm of Love', and 'My Fair Princess' to every other movies from the calculated distance matric results. 
Step 2: Average the distances of 5 watched movies to every other movies
Step 3: Order the distances to find the closest movies
Step 4: Get the top 5 recommendations excluding 5 watched movies

Finally, the list of 5 movie suggestions is:
* "Kill Me Love Me"        
* "Love Me, Love My Voice" 
* "Here We Meet Again"    
* "The Imperial Coroner"   
* "Bohe zhi xia"

### **K-Means Clustering for Classification**
#### **Group movies according to Genres and High_Rating**
The genre grouping uses features as Genre_Comedy, Genre_Drama, Genre_Crime, Genre_Romance, Genre_Action, Genre_Adventure, Genre_Mystery, Genre_Fantasy, and High_Rating, with k = 12. The cluster sometimes does not make sense, for example, Cluster 3 - Genre_Romance has both high and not high ratings. 

![Image](https://github.com/user-attachments/assets/5a7a1b7f-f15c-4303-af44-71a9c4b5b735)

#### **Group movies according to Main_Famous, High_Rating**
The genre grouping uses features such as Main_Famous and High_Rating, with k = 4. Movies with famous leads tend to influence ratings more than those without. However, in this small dataset, the percentage of high-rated and not-high-rated movies is almost equal. Therefore, it is unclear whether movies with famous actors or actresses are highly rated.

![Image](https://github.com/user-attachments/assets/5a7a1b7f-f15c-4303-af44-71a9c4b5b735)

#### **Group movies according to Ending, High_Rating**
The genre grouping uses features such as Ending_Happy, Ending_Sad, Ending_Open, and High_Rating, with k = 6. It is evident that movies with happy endings tend to have lower ratings. However, sad and open endings show no significant difference in their high-rating percentages. 

![Image](https://github.com/user-attachments/assets/e6278b7a-5238-4733-904d-26e3b0e049f5)

#### **Group movies according to High_Voting, High_Rating***
The genre grouping uses features such as High_Voting, High_Rating, with k = 4. There is consistent evidence that movies with high voting tend to have high ratings and vice versa. However, low voting seems to impact ratings more than high voting.

![Image](https://github.com/user-attachments/assets/e87b47ab-18e2-4654-97ce-bfa2ef9a5fd2)

### **Machine Learning Models for Popularity Prediction**
#### **KNN (K-Nearest Neighbors)**
The dataset is divided into train dataset and test dataset. 80 rows are selected randomly as the train data and the rest 10 rows are marked as the test data. With k = 4, 'Ending_Sad', 'Ending_Happy',  'Ending_Open',  'High_Voting',  'Main_Famous' as predictors and High_Rating as the response, the prediction result is as below:

![Image](https://github.com/user-attachments/assets/cb169f6b-823d-49a0-b990-f8dffe7e5f3b)

Accuracy: 70% | Misclassification: 30%

![Image](https://github.com/user-attachments/assets/c78cda7e-3482-4a10-852d-0e6604a80ac1)

#### **Decision Tree**
This algorithm has features as Ending_Happy, Ending_Sad,  Ending_Open, Main_Famous, and High_Voting to predict High_Rating. At first, the dataset is labeled as train and test dataset, which is done in KNN. Using R to run the tree model, we have the image as below:

![Image](https://github.com/user-attachments/assets/c78cda7e-3482-4a10-852d-0e6604a80ac1)

The prediction result

![Image](https://github.com/user-attachments/assets/aae7999c-7c71-4677-bc14-f1662859171e)

![Image](https://github.com/user-attachments/assets/fec7fb06-98b0-44c0-80ea-28af44275697)

Accuracy: 80% | Misclassification: 20%

#### **Logistic Regression**
This algorithm has features as Ending_Happy, Ending_Open, Ending_Sad, Male_Famous, Female_Famous, and High_Voting to predict High_Rating. The model is built in R and the result is as below:

![Image](https://github.com/user-attachments/assets/f46da81b-24b1-4a09-b8f4-e3837cedc8f2)

log( p̂ / (1 - p̂) ) = -1.1550 - 0.5719 × Ending_Happy + 0.5185 × Ending_Open + 0.5650 × Male_Famous - 0.1104 × Female_Famous + 2.2302 × High_Voting

### 🔹 Notes:
p̂ / (1 - p̂): the predicted probability of High_Rating = 1

Interpretation table

![Image](https://github.com/user-attachments/assets/920ad221-bc37-4148-b2f3-456dd8387379)

The confusion matrix

![Image](https://github.com/user-attachments/assets/df15bd72-e22d-40a4-ac21-92204870f1dd)

Based on the confusion matrix, the accuracy and misclassification rates are described as below:

![Image](https://github.com/user-attachments/assets/32792aa2-4b9a-4139-b9cc-bae7d803789d)

Out of 61 not High_Rating movies, there are 52 correct predictions (true negatives) and 9 misclassifications (false positives). Out of 29 High_Rating movies, there are 17 correct predictions (true positives) and 12 misclassifications (false negatives). The accuracy rate is 76.7%, and the misclassification rate is 23.3%.

Accuracy: 76.7% | Misclassification: 23.3%

---

## **🛡️ Ethics & Privacy Considerations**
* The dataset is limited to 90 movies, which may introduce biases.
* Cultural bias exists as only Chinese movies are considered.
* The "Famous Actor" category is subjective and may change over time.
* Ratings are sourced from IMDb, but additional sources could strengthen the analysis.

---

## **🚀 Future Improvements**
* Expanding the dataset for better clustering results.
* Analyzing additional factors like critic reviews, audience comments, and streaming data.
* Exploring budget, revenue, and profit analysis to predict a movie's success.
* Investigating seasonal movie trends and how audience preferences shift over time.

--- 

## **📩 Contact & Contributions**
Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

