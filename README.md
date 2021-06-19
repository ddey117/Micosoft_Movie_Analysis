# 21st Century Movie Trend Analysis

**Author**: [Dylan Dey](mailto:ddey2985@gmail.com)

## Repository Structure 
```
├── data (raw zipped data and cleaned/processed data saved in seperate files)
├── images (png files for all images related to this project)
├── README.md (This ReadMe focuses heavily on the contents of the project)
├── Dataset_Tables.md  (table created to explore the contents of the data)
└── Data_Exploration_and_Processing.ipynb (first notebook for important and processing unkown data)
├── Analysis_and_Visualizations.ipynb (second notebook for visualizing the data and results)
└── moviePresentation.pd (final presentation of findings)
```

## Overview

The notebook Data Analysis Notebook imports the processed data from the Data Exploration notebook in order to analyze current movie trends on behalf of Microsoft's new movie studio. By putting an emphasis on the median ROI% value of movie data from a number of movie database websites, as well as by creating a list of the most popular movies, evaluation of financial performance and the risk involved was evaluted and recommendations based on these findings were made. A focus on large budget movies with particular genre elements released at the appropriate time of the year will ensure the best chance of success at the box office for Microsoft.

## Business Problem
This project covers the following hypothetical:
Microsoft wants to create a new movie studio and decided to hire me to conduct data analysis to determine what films are currently performing the best at the box office. Using multiple datasets from a number of movie databases, expected returns and risk as well as expected cost and how to best utilize recourses can be determined through anaylsis. As the newcomer to a crowded realm, further analysis was conducted to ensure a well recieved debut movie and to set the standard for the quality of it's future films.

## Data

[The Numbers](https://www.the-numbers.com/) <br>
[Box Office Mojo](https://www.boxofficemojo.com/) <br>
[IMDb](https://www.imdb.com/) <br>
[Rotten Tomatoes](https://www.rottentomatoes.com/) <br>
[The Movie Database](https://www.themoviedb.org/)

The Numbers and Box Office Mojo websites provided all of the financial information (budgets and revenue) needed for analysis. IMDb provids a large amount of data for writers, directors, genres, and general information for a large sum of movies. Rotten Tomatoes provides a unqiue value in terms of critical review from trained professionals. The Movie Database provides an alternative to the information available from IMDb. 

Please reference the [Dataset Table](https://github.com/ddey117/Microsoft_Movie_Analysis/blob/master/Dataset_Tables.md) for a detailed description of every dataset involved in this project.


*The data is described and explored in much more detail in the accompanying jupyter notebooks.*


<img src="images/Schema.png">

## Methods

This project focuses on creating appropriate visualizations in order to quickly identify important trends for financial success of movies as well as approval from the public. An ROI% feature was engineered to gain financial insight, whereas a collection of popular movies was queried to make analyses focusing on IMDb ratings. 

## Results


Currently the trend for movie profitabilty is bit more varied than it was a decade ago, there still appears to be year over year growth and now is a good time for Microsoft to enter the field.
![film_Profitability](./images/film_Profitability.png)
High budget films are preffered over low budget films in terms of financial success.
![low_vs_high](./images/low_vs_high.png)
Early summer and winter holidays are the best times to release a new film.
![high_seasons](./images/high_seasons.png)
Drama, Action, and Adventure are the most popular genre elements. 
![top_genres](./images/top_genres.png)


## Conclusions
Overall, it is riskier to get into the movie studio buisness than it was at the beginning of the 2010s. That being said, there is still a good financial incentive for Microsoft to enter the field right now, keeping in mind the following recommendations: 

* Focus on large budget films and be prepared to spend more than $20,000,000 per film. Although lower budget movies can have impressive ROI returns, they are more likely to fail than larger budget movies. 
* Plan to release movies towards the beginning of summer, or during the winter holidays. Avoid releasing movies at the beginning of the year or during the fall. 
* Focus on creating a film with elements of Drama, Action, and Adventure as they tend to be recieved well by the public as compared to other genres. 



### Next steps


Include more consumer side analysis. Who is the major target audience? 

Gain more insight into lower budget movies and make further recommendations if high budget films are unnatainable. 

Including analysis of the rotten tomato dataset could reveal some insights about how critical acclaim affects the financial success of movies.

Including analysis of the TMDb Dataset with focus on the unique feature of 'popularity' can be used to support some of my findings and to explore the data even further.

By using the OMDb API, it would be possible to gain insight on how the success of a movie relates to their associated posters, but it was beyond the scope of this project.


## For More Information

See the full analysis in the [Exploratory Notebook](./Data_Exploration_and_Processing.ipynb) and [Analysis Notebook](./Analysis_and_Visualizations.ipynb) or review this [presentation](........).

For additional info, contact Dylan Dey at [ddey2985@gmail.com](mailto:ddey295@gmail.com)


## Repository Structure (reminder)

```
├── data
├── images
├── README.md
├── Dataset_Tables.md
└── Data_Exploration_and_Processing.ipynb
├── Analysis_and_Visualizations.ipynb
└── moviePresentation.pdf
```
