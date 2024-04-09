## **Movie Recommendation System using TMDB Dataset**
This project implements a movie recommendation system using the TMDB (The Movie Database - https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) dataset. Recommendation systems are algorithms designed to suggest items to users based on their preferences and behaviors. In the context of movies, recommendation systems help users discover films they might enjoy based on their past viewing history, ratings, or other relevant attributes.

**Types of Recommendation Systems**
There are several types of recommendation systems, each with its own approach to providing personalized recommendations:

- **Content-Based Filtering:** This approach recommends items similar to those a user has previously liked or interacted with. In the context of movies, content-based filtering analyzes attributes such as genres, keywords, and descriptions to suggest films that share similar characteristics with ones the user has enjoyed in the past.
- **Collaborative Filtering:** Collaborative filtering suggests items based on the preferences of similar users. It identifies users with similar tastes and recommends items liked by these users but not yet seen by the current user. This approach does not rely on item attributes but rather on user interactions and preferences.
- **Hybrid Recommendation Systems:** Hybrid systems combine multiple recommendation techniques to provide more accurate and diverse recommendations. By leveraging both content-based and collaborative filtering approaches, hybrid systems aim to overcome the limitations of individual methods and deliver more tailored recommendations.

**Approach Used in This Project**
The movie recommendation system implemented in this project primarily utilizes content-based filtering. By analyzing textual features such as genres, keywords, and overviews of movies, the system calculates similarity scores between movies and suggests films that are most similar to those the user has expressed interest in. Since there is no user data available for collaborative filtering, the focus remains on content-based techniques for providing personalized recommendations.

**Data**
The dataset comprises two main dataframes:

- **df1:** Contains detailed information about movies, including title, genres, keywords, production companies, cast, crew, overview, release date, etc.
- **df2:** Provides credits information such as cast and crew for each movie.
  
**Algorithm**
- Data Preprocessing: The script preprocesses the data by handling missing values, dropping irrelevant columns, and converting data types as required.
- Text Processing: Utilizes NLTK for text processing tasks such as tokenization, stopword removal, lemmatization, and cleaning of textual features like overview, genres, keywords, etc.
- Feature Extraction: Employs CountVectorizer to convert textual features into numerical vectors, enabling similarity calculations.
- Similarity Calculation: Computes cosine similarity between the feature vectors of movies, resulting in a similarity matrix.
- Recommendation Generation: Generates movie recommendations based on a given movie title by sorting movies according to their similarity scores and selecting the top N similar movies.
