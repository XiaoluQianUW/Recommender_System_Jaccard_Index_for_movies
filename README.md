# Ratings and Recommendations
I looked at some measures for similarity and popularity that recommendation systems might use
to recommend things, like movies. I decided to work with the movielens 100k dataset, which consists of 100,000
ratings of movies from 943 users on 1682 movies. The ratings vary between 1 and 5. It was collected by the University
of Minnesota and is available for easiy download at [here](http://grouplens.org/datasets/movielens/100k/). You will need to
download this dataset.

Recommender systems often try to pick movies you will like based upon a given movie that you like. To do this
requires a similarity metric between movies. In this problem we consider a simple one that only considers the users
that have rated two movies, but not the ratings themselves. It is called the Jaccard index. Given two movies M1 and
M2, 0 <= J(M1, M2) <= 1, where J is the Jaccard index. J(M,M) = 1. The Jaccard index is defined as the number
of users in the database who rated both M1 and M2 divided by the total number of users who rated at least one of M1
or M2.

For example, if you test this dataset:
* J( Chasing Amy, Good Will Hunting ) = 0.175
* J( Heat, The Godfather ) = 0.311
* J( The Godfather, The Godfather: Part II ) = 0.433

In this jupyter notebook, I first simply look at the user ratings for movies in this database. Then I found the two movies that have perfect ratings from all the users who saw them, and which also tie for the most users who rated them. I also found the five most highly rated movies (by mean rating over all users who rated them) for movies that were rated by more that 100 people.

In the end, I demonstrated how to find the five closest movies by Jaccard index to Toy Story and Casablanca.
