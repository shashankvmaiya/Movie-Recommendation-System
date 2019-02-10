# Movie-Recommendation-System

In this project, we build a movie recommendation engine using multiple Content based and Collaborative based filtering techniques and similarity functions like Pearson correlation, euclidean and cosine distances. 

Three data sets are collected for this purpose - 
* users.dat: Contains the information about users or critics who rate the movies - gender, age, employment and zip code
* movies.dat: Contains the information about the movies - movie name, list of genres that they belong to
* ratings.dat: Contains set of ratings (1 to 5) provided by the users to a subset of the movies

Given a sparse user to movie matrix which contains the rating, recommendation system essentially fills in (or predicts) the rating for all the empty cells. Once we can estimate ratings for these unrated items, we can recommend to the user the movie(s) with the highest estimated rating(s). In this project, we split the provided ratings data into test and train set and predict the ratings on the test set. We use Root Mean Square Error (RMSE) as the metric to evaluate the performance of the model.  

Few interesting results
* Overall mean rating ~3.5. This indicates that critic more often rate a movie above average
* The zero-bias recommendation system which essentially returns the overall mean rating is a great first choice system (with a low RMSE)
* Among several simple collaborative based filtering techniques, the collaboration based on users zip yielded lowest RMSE. This indicates that users from similar geographical locations rate movies similarly!
* Cosine function works best among the tried similarity functions. 
