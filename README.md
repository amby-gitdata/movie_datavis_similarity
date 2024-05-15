# # movie_datavis_similarity

This project/code involves the analysis of movie watch data and a rudimentary movie similarity detection tool. 

## Movie_data_cleanup 

Code removes unwanted profiles and columns that won't be used in further analysis. It converts time to an integer format (minutes). It identifies movies versus tv shows by using the logic that movie titles are shorter and don't contain the words 'episode' and 'season'. The limitation of this method is that some movies might contain those words, and I attempt to identify those in the code. A better way would be to use the IMBbPY library, which I use in the next set of code.

## Movie_data_vis_similarity

Code plots some graphs of interest such as amount of time spent per title, top genres, etc. Genres and other info about the movie were obtained by utilizing the IMBbPY library.

I then used two algorithms to check similarity of movies to a query movie namely k nearest neighbors and cosine similarity. The two were sort of in agreement. The limitations of these methods are : Could use more investigation in the effectiveness of the algorithms when considering extremely high dimensional matrices, the query movie title is fixed and is not a function accepting any query movie title. There is a lot of the redundancy in the way the genres are converted to binary features, because most movies follow a few top genres. The data is intrinsically biased because it is already preferred/ watched data. Also one of the metrics of movie rating /sorting is 'engagement' which is the duration of minutes spent watching a particular title normalized to the runtime of the title. This is only an indirect metric of interest in the movie. 
