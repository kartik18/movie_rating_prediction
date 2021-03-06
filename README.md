![Alt text](/TitlePoster.png?raw=true "Movie Rating Prediction")
# REEL RATINGS
### Contributors: Victoria Sneddon (Project Manager), Andrew Polk, Ivy Tran (LATE), Brandon Tran, Ari Gilmore, Danielle Rabinson, Jake Hickey

## Abstract
We want to be able to predict the rating of a movie before it is released. We want to be able to input a movie or upcoming movie title and output the predicted movie rating.

# Table of Contents
* [Week 3](#weekthree)
* [Week 4-6](#weekfour-six)
* [Week 7](#weekseven)
* [Week 8](#weekeight)
* [Week 9](#weeknine)
* [Week 10](#weekten)

## Basic flowchart outline of the project
![Alt Text](/MovieRatings.png?raw=true "flow chart")

## Aspects:
+ Rotten Tomatoes API (Kaggle, IMDB) -previous movies of that genre and their rating
+ Data Algorithms (weighting actors vs. directors vs. budget…)
#
+ Query data about movie title or movie id to get parameters 
  + (Danielle & Brandon)
+ Query previous ratings of rating parameters
+ Create a method of storing data and accessing it from different parts of the program 
  + (Victoria & Andrew)
+ Some sort of statistical analysis on ratings (Data algorithms) 
  + (Ari, Jake, and Ivy)
+ Create an interface or web app to take input and display results
#
+ Factors available to use: 
  + Average movie rating
  + Actors
  + Director
  + Producers
  + Budget
  + Studio
  + Writers
  + Genre
  + Cinematographer
  + Music
  + ect...

## Data Sources:
+ API rotten tomatoes
+ API imdb
+ API themoviedb
+ Kaggle

## Languages:
+ Python
+ HTML

## Blockers
+ Themoviedb has a 40 query per 10 second limit per api key.
+ Other api's probably have similar restrictions.

## Creating a virtual environment
+ ### First time run:
   	+ > sudo apt install virtualenv (if needed)
   	+ > virtualenv peerenv
+ ### Starting virtualenv
   	+ > source peerenv/bin/activate
	+ > pip install -r requirements.txt
+ ### Closing virtualenv
	+ > deactivate

## Basic Project Timeline
  ## <a name='weekthree'></a>Week 3:
  + Create an outline for the project
  + Split into smaller groups (Pair up)  to work on individual sections of the project
  + ### Week 3 Update:
  	+ #### Brandon/Danielle:
		+ Made an account for Amazon Web Services (AWS)
		+ Downloaded AWS SDK for Java
		+ Downloaded legacy Java 6 for Eclipse
		+ Downloaded JVM 1.8 for Eclipse
		+ Configured AWS Toolkit for Eclipse, and samples successfully
		+ https://569112368633.signin.aws.amazon.com/console log in
  	+ #### Ari/Ivy/Jake
		+ Will weight the ratings of directors previous films based on date.
		+ Take the sample mean of the ratings of the director’s movies and that will be the prediction
		+ Award data? (how many oscars won) (later)
		+ Age of the director (later)
		+ Regression chart for when other factors come in
  	+ #### Andrew/Victoria
		+ Created a simple script in python, using libraries: json, requests, datetime
		+ The script accesses themoviedb and get the works and ratings for a director parsed into json
		+ Working on ways to pass the information from the script to the stats team
		+ Still need to get director age, awards and any other data the stats team wants
		+ Get data from rottenTomatoes/IMDB ect...?

  ## <a name='weekfour-six'></a>Week 4-6:
  + Start putting together the different portions that the smaller groups have been working on
  + ### Week 3-6 Update:
  	+ #### Brandon/Danielle:
		+ Downloaded IMDb's datasets using AWS S3 services
		+ Gave Andrew the data to merge
  	+ #### Ari/Ivy/Jake
		+ Considering date of directors' previous movies as a factor in rating
		+ Using number of ratings per movie rating to calculate mean value of directors' previous films
  	+ #### Andrew/Victoria
		+ Created script to access IMBDb's title names, ratings, etc.
		+ Created script to merge ratings and title info tsv files
		+ Will utilize both Movie DB and IMDb as foundation of project's data
  ## <a name='weekseven'></a>Week 7:
  + Finish merging different sections of the project
  ## <a name='weekeight'></a>Week 8:
  + Bug fixes
  + Add functionality (ex. Custom movies as input, Rate TV shows, add more parameters)
  ## <a name='weeknine'></a>Week 9:
  + Bug fixes
  + Clean up project 
  ## <a name='weekten'></a>Week 10:
  + Bug fixes
  + Clean up project

## Structure

	├── LICENSE
	├── README.md          <- The top-level README for developers using this project.
	├── data
	│   ├── external       <- Data from third party sources.
	│   ├── interim        <- Intermediate data that has been transformed.
	│   ├── processed      <- The final, canonical data sets for modeling.
	│   └── raw            <- The original, immutable data dump.
	│
	├── references         <- Data dictionaries, manuals, and all other explanatory materials.
	│
	├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
	│   └── figures        <- Generated graphics and figures to be used in reporting
	│
	├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
	│                         generated with `pip freeze > requirements.txt`
	│
	└── src                <- Source code for use in this project.
	    ├── __init__.py    <- Makes src a Python module
	    ├── example1.py    <- have to be here or cant import modules
	    ├── example2.py
	    ├── api_keys.txt 	<- stores api keys to be used in query
	    │
	    ├── data           <- Scripts to download or generate data
	    │   └── parameter_query.py 	<- downloads rating data for parameters 
	    |
	    ├── models         <- Scripts to train models and then use trained models to make
	    │   │                 predictions
	    │   └── predict_model.py <- replace with stats model
	    │
	    └── visualization  <- Scripts to create exploratory and results oriented visualizations
	        └── visualize.py
