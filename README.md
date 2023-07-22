# Netflix-Movies-and-TV-Shows-Clustering
### Verified Project :[Credentials](https://certificates.almabetter.com/en/verify/33591944820269)
# **Project Summary -**

# The steps involved in making this project are:


**1. Know Your Data:**

  The first step in this machine learning project is to get to know the data. This involves importing necessary libraries and loading the dataset. Once the dataset is loaded, it is important to take a first look at the data and understand its rows and columns. The dataset information should be checked for duplicate values and missing or null values.

**2. Understanding Your Variables:**

  The next step is to understand the variables in the dataset. This involves describing the variables and checking their unique values. Data wrangling may be necessary to manipulate the data and gain insights.

**3. Data Visualization:**

Data visualization is an important part of this project. The goal is to understand the relationships between variables by experimenting with different charts. For each chart, it is important to explain why it was chosen and what insights were gained from it. These insights should be evaluated for their potential to create a positive business impact.

**4. Feature Engineering & Data Pre-processing:**

Feature engineering and data preprocessing are also important steps in this project. Missing values must be handled using appropriate imputation techniques. Data preprocessing may involve expansion and lower casing, removing punctuation, stopwords, and whitespace, text normalization and vectorization, data scaling, and dimensionality reduction. Outlier treatment techniques should also be used as necessary.

**5. ML Model Implementation:**

The final step in this project is to implement machine learning models. Several models are suggested including K-means clustering, hierarchical clustering, and the elbow method. Text data can be vectorized using TF-IDF. The performance of each model should be evaluated using appropriate evaluation metrics and cross-validation and hyperparameter tuning may be necessary.

**6. Conclusion:**

In conclusion, this machine learning project involves several steps including data exploration, data visualization, feature engineering, and model implementation. By following these steps carefully, it is possible to create a successful machine learning model that can be deployed on a live server for real user interaction.

# **Problem Statement**

This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Flixable which is a third-party Netflix search engine.
In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.

Integrating this dataset with other external datasets such as IMDB ratings, rotten tomatoes can also provide many interesting findings.

 ### The observations I found are:

- The dataset consists of 7787 rows and 12 columns.
- There are no duplicate values in the dataset.
- The column with the highest percentage of null values is 'director', with almost 30% null values. This is followed by the 'cast' and 'country' columns, which have 9.2% and 6.7% null values respectively.
- All columns contain data of the object type, except for the 'release_year' column which is of integer type. This means that there is only one numerical column in the dataset.

### Variables Description 
Here are the descriptions of each variable:

1. `show_id`: A unique identifier for each show.
2. `type`: The type of the show, either 'Movie' or 'TV Show'.
3. `title`: The title of the show.
4. `director`: The director(s) of the show.
5. `cast`: The main cast members of the show.
6. `country`: The country or countries where the show was produced.
7. `date_added`: The date when the show was added to Netflix.
8. `release_year`: The year when the show was released.
9. `rating`: The content rating of the show (e.g., TV-MA, PG-13).
10. `duration`: The duration of the show in minutes (for movies) or seasons (for TV shows).
11. `listed_in`: The genre(s) that the show belongs to.
12. `description`: A brief description of the show's plot.

### What all manipulations have you done and insights you found?

1. The 'date_added' column was converted into a datetime format and new columns were created to extract information such as 'day_name', 'day_added', 'year_added', and 'month_added'.

2. Created a new variable for tv-series and movies using 'type'.
3. Using above variables we created two dataframes for movies and tv-series named 'df_mov and 'df_tv'.
4. The ‘rating’ column contained several categories, so for better understanding, it was categorized into 4 basic categories: kids, older kids, teens, and adults. 
5. Changed types of necessary columns to strings.

# **Conclusion**


### EDA Findings:

* Netflix tends to add new content towards the end of the current year and the beginning of the next year.
* In 2019, Netflix's content consisted of approximately 70% movies and 30% TV shows.
* There was a noticeable decrease in new content after 2020 due to the COVID-19 pandemic.
* The most popular genre on Netflix is comedy.
* Around 30% of movies and 50% of TV shows on Netflix are original productions.
* India has the second highest amount of content available on Netflix, with the United States having the most.
* Content categories by country:
  1. India has the most teen content.
  2. Spain has the most adult content.
  3. Canada has the most kids content.
  4. Japan has the most older kids content.

* These insights are valuable for business development and SWOT analysis.

### Clustering Conclusions:
* We tested 3 machine learning models:
 1. K-means clustering
 2. Elbow curve
 3. Hierarchical clustering

* K-means clustering is the best model for this dataset.
* K-means clustering indicated that 4 is the optimal number of clusters with a silhouette score of 0.44. 
* However, after cross-validation with the Elbow curve, we selected 6 as the 
  optimal number of clusters.

* The cosine-based recommender system performed very well.
