MICROSOFT MOVIES

BUSINESS PROBLEM
Microsoft sees all the big companies creating original video content and they want to get in on the fun. 

They have decided to create a new movie studio, but they don’t know anything about creating movies.

Objectives
Exploring what types of films are currently doing the best at the box office. 
Translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

Data loading
3 data sets were loaded separately:
- imdb.title.basics
- imdb.title.ratings
- bom.movie_gross

They were imported as csv and analyzed using pandas library

DATA INSPECTION AND MERGING
- Each data set was inspected separately
- The 3 data sets were then merged using common column keys i.e. title, and tconst

DATA CLEANING
- The column foreign gross was converted to the correct data type: object to float
- There was significant number of missing values in the foreign gross column (38.1%).
- Imputation using the median was done because of the skewed distribution

  ![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/e391590e-c6ec-4d6f-b417-e1bf6e85095b)

  - Outliers were then assessed using box plots
    
![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/91a31e6b-ed19-4907-8579-a60aae47b928)


- Considering the context within which this data is collected is not all outliers were removed. Movies that are doing better than average in terms of income and ratings are worth noting. This is valuable information that should be kept as part of the analysis. There are outliers in run time that is isolated and likely to alter the analysis. These were subsequently dropped

![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/a0bdae87-0752-42d9-84b7-e2a8f1c43374)

- There were no duplicated rows

EXPLORATORY DATA ANALYSIS
- The movies were then grouped by their genre and analyzed in various categories
  the top 10 genres by average rating, domestic gross, runtime, foreign gross and number of votes were as follows:
![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/1f1107c1-2d97-4092-ae5c-23864fd46229)
![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/b15e0bf2-d8d3-4632-8fe4-dd224d3c6397)
![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/9872915e-e23c-4d00-b291-071c7ecc7249)
![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/51b5190a-f346-48e1-92ac-32ee96b6cbcb)
![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/972c2849-77b6-4178-81ab-945e043cec4e)

Equal weights were then assigned to each category and then used to calculate the overall best movie genres as a performance metric.
The top 5 performing genres were as follows

![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/4c9fff99-60dd-488e-9460-1e8abb58c5d3)

The correlation matrix of the movie attributes was as below:
![image](https://github.com/FelixMburu/Project-1-Felix-Mburu/assets/151352303/1ff1006d-1d2e-4d84-9128-0030f405a7e3)

SUMMARY AND INSIGHTS

The top genre of movies by average rating are (Adventure, Drama, Scifi) and (Biography, Documentaries, Family) which both have an average rating of 8.3
The top genre by domestic gross income is Sci-Fi
The top genre by foreign gross is Adventure, drama, sport
The top genre by number of votes is Adventure, drama, sci-fi
The top genre by run time is Action, Drama, Sport
Overall the top performing genre is adventure, drama, sport
There is a positive correlation between number of votes and gross income
Insight
Microsoft should consider making movies in the Adventure, drama, sport genre.

