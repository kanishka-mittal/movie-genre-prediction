Group:
Kanishka Mittal (200050058)
Khyati Patel (200050102)
Sanyam Saxena (200260047)
Vatsal Goyal (200020158)


To download the dataset used in the project use the following link:

https://drive.google.com/drive/folders/1cXPMqGUR9GrVAwS6pGZY1oiucAhrsndw?usp=sharing 


This link has 3 files:
MovieGenre.csv This is a file which links the dataset images to corresponding, genres, ratings. It has close 41k movie info 
archive.zip This is the file which contains a dataset of close to 1000 images which we use for our experiments
posters.zip This is the file which contains the entire dataset set without any cleaning  

Files Submitted:

1) Dataset_analysis.ipynb
      This is the file where we have analysed the complete dataset. 
      First we have plotted for the entire dataset num of movies per genre, average rating per genre (posters.zip)
      Then we have plotted for the smaller refined dataset num of movies per genre, average rating per genre, rgb average intesity per genre (archive.zip) 
       
2) Models.ipynb
      This is our main file which contains the following steps:
         a) Load data
         b) Clean data to remove empty values and images which were corrupt or didn't open
	 c) Split the data in train, val, and test
         d) A custom model which we designed and its results
	 e) KNN Model for different k values
         f) Pretrained Resnet for prediction where resnet model layers are not trained  
         g) Pretrained Resnet for prediction where resnet model layers are also trainable  
         h) Pretrained VGG model for prediction where resnet model layers are not trained  
3) Models_large_dataset.ipynb
      In this we have repeated all the above steps for the dataset of 5k images
4) Movie_success_predication.ipynb
      In this notebook, we try to predict the success of a movie(profitability) by its posters. 
5) Rating.ipynb
      sThis is the file in which we have tried to establish the relation between the imdb ratings
      and there poster using KNN regression and SVM regression.
      The results obtained proves no direct relation between poster and imdb rating 

How to reproduce results using our files "other than movie_success_prediction.ipynb":

1) It is recommended to run the code in Google collab
2) To use the dataset:
   a) Create a folder named Movies in your drive
   b) Put the 3 files present in the above link in that folder 
3) Open our .ipynb files in google collab and click Run All
4) The window will ask for your drive authentication. Authenticate it accordingly
5) All the cells will run for at max 10 minutes(in models.ipynb file, rest 2 minutes max) with GPU of collab enabled 


JUST FOR SUCCESS PREDICTION:
For success prediction, a different custom dataset was curated by merging IMDB and TMDB dataset. 
This link contains the images and the two datasets: https://drive.google.com/drive/folders/1P1MmDCOvo2juvwC47cbHldIgIJVpOqua?usp=sharing
Steps to reproduces:
	1) We recommend using Google Colab
	2) Save the Dataset.zip file and the 2 csv files in EarningPrediction folder in Movies folder in your drive
	3) Open our .ipynb files in google collab and click Run All
	4) The window will ask for your drive authentication. Authenticate it accordingly
	6) To reproduce the graph, set the early stopping to >=20 in the Trainer class
	

