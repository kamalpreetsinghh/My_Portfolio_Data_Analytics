r# Projects

# 1. Most Popular Anime in Japan

I want to find out the most popular anime in Japan and their genres, and want to know if anime rating has an impact on the number of viewers

### Data Collection

I have downloaded the dataset from data.world

The dataset contains names, genres, number of episodes, ratings and number of viewers for an anime

### Data Cleansing

I have cleansed the data for creating visualization in Power BI

I have selected anime with number of episodes greater than 1 and ratings greater than 8.5

### Dashboard

![Image of Anime Dashboard](https://user-images.githubusercontent.com/88215400/127746305-0743fb4d-0a0a-4d1d-bd60-8a0aa6ff35ae.png)

### Insights

1. In the first graph, I have used a line graph to compare the number of viewers with the anime ratings. There is no correlation between the number of viewers and the ratings.

2. In the second graph, I have used a clustered column chart to find the top five anime with most number of viewers. I have found that Death Note has the highest number of viewers while it has not the highest ratings.

3. In the third graph, I have used a pie chart to find the top five highest rated anime. I have found that the Full Metal Alchemist is the highest rated anime in Japan.
 
4. In the fourth graph, I have used a Area Chart to find the most viewed genres of anime. Action and Copmedy anime are most viewed and horror anime are least viewed by the people.

# 2. Analysis of US Hotels 

I want to find out the most popular destinations of hotels in US.

### Data Collection

I have downloaded the dataset from [data.world](https://data.world/datafiniti/hotel-reviews)

The dataset contains names, cities, states, ratings, date of stay and number of viewers for a hotel

### Data Cleansing

I have cleansed the data for creating visualization in Power BI

I have selected top 6 cities with most number of hotels in US

### Dashboard

![Image of Hotel Dashboard](https://user-images.githubusercontent.com/88215400/127747552-cb938089-142f-4ec4-95da-fa1d85aa53e4.png)

### Insights

1. In the first graph, I have used a vertical bar chart to compare the number of hotels in major US cities. It is clearly visible from the chart that Las Vegas has the greatest number of hotels and Los Angeles has the minimum number of hotels. Vertical Bar Charts are great for comparing data

2. In the second graph, I have used a line chart to compare the average hotel ratings from 2015 to 2018. I have found that the hotel ratings increase from 2015 to 2017 and then decreases to 2018. Customers are most satisfied with their hotels in 2017. Line chart is great for data with timelines.

3. In the third graph, I have used a pie chart to visualize the composition of average hotel ratings in US. All the US states have almost similar average hotel ratings which means the customers are equally satisfied with their hotels in the US.

4. In the fourth graph, I have used a Waterfall graph to see the number of ratings in the major US cities and the total number of ratings. It will help me in understanding the variation in population of different cities which is giving hotel reviews.

# 3. Cancer Analysis Using Neural Networks

I have used a cancer dataset to find if a patient has cancer or no cancer based on the variables like clump thickness, mitosis, etc. using Neural Networks 

### Data Collection 

I have downloaded the dataset from data.world The dataset contains clumpthickness, mitosis, bland chromatin, normal nucleoli, marginal adhesion, bare nucleoli values of a patient. 

### Data Cleansing 

I have cleansed the data for creating visualization in Power BI

### Key Statistical Data

![Key Statistical Data](https://user-images.githubusercontent.com/88215400/127748005-6ed89cba-ddb0-417e-b788-4cefda42c8a7.png)

### Neural Network Code for Classifying patient into Cancer and No Cancer

```markdown
#Create x and y variables
X = df2.drop('Class', axis = 1).to_numpy()
y = df2['Class'].to_numpy()

#Create Train and Test datasets
from sklearn.model_selection import train_test_split  
X_train, X_test, y_train, y_test = train_test_split(X, y, stratify = y, test_size = 0.20, random_state = 100)

#Scale the data
from sklearn.preprocessing import StandardScaler  
sc = StandardScaler()  
x_train2 = sc.fit_transform(X_train)
x_test2 = sc.transform(X_test)

#Script for Neural Network
from sklearn.neural_network import MLPClassifier  
mlp = MLPClassifier(hidden_layer_sizes = (9, 4, 2),
                    activation = 'relu', solver = 'adam',
                    max_iter = 10000, random_state = 100)  
mlp.fit(x_train2, y_train) 
predictions = mlp.predict(x_test2) 

#Evaluation Report and Matrix
from sklearn.metrics import classification_report, confusion_matrix
print(confusion_matrix(y_test, predictions))  
print(classification_report(y_test, predictions, target_names = ['No Cancer', 'Cancer'])) 
```

### Classification Report

![Classification_Report](https://user-images.githubusercontent.com/88215400/127748212-35172c4b-d51b-4ffa-9322-f962eafb026f.png)

### Evaluate the algorithm.
The weighted average precision and recall score of the algorithm is 0.97 for both which is a very good score, and the dataset size is 137 which is a decent size of a dataset. The precision and recall score for no cancer are 0.97 and 0.99 respectively, and for cancer are 0.98 and 0.94 respectively which are very good metrics for an algorithm.
Hence our algorithm is a very good algorithm. We can also increase the sample size to get more accuracy of the algorithm.



## About Me
- 👋 Hi, I’m @kamalpreetsinghh
- 👀 I’m interested in programming, traveling and photography
- 🌱 I’m currently learning Python for Data Science
- 💞️ I’m looking to collaborate on Machine Learning and Deep Learning Projects
- 📫 How to reach me kamalpreetsingghh@gmail.com

I like to solve machine learning problems which requires out of the box thinking. 

I am good at creating interactive dashboards and SQL for database operations.

