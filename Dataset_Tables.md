### Box Office Mojo Dataset 


This dataset contains box-office revenue (both domestic and foreign) and the year the movie was released by title and studio. The movies were released between the years 2010 and 2018 and the set contains thousands of entries. Because we are only trying to determine current trends, this collection of movies released in the 2010s (2019 excluded) is a good fit for our goal.  



The dataset contains the following fields:

**title:** Full title of the film. <br>
**studio:** Abbreviation of the film studio that produced the film. <br>
**domestic-gross:** The gross box-office revenue from North America (U.S., Canada, and Puerto Rico). <br>
**foreign_gross:** "The gross box-office revenue for the rest of the World. <br>
**year:** Year of film release.


### The Numbers Dataset  

The Numbers Dataset contains very useful information for the cost and revenue of a large number of films from 1915 to 2020. I have added a few more columns to look at each month and year seperately, as well as engineered another column to represent the total return on investment (ROI) of each film. See code below for more details.

**id:** unique identifier for dataset (primay key) <br> 
**release_date:** full date of movie release    
**movie:** title of film                    
**production_budget:**  total budget of film           
**domestic_gross:**  domestic gross revenue                
**worldwide_gross:** total global revenue            
**release_year:**  year of release pulled from release_date          
**release_month:** month of release pulled from release_date     
**ROI:** the return on investment for the film normalized (total percent return based on budget and global revenue)

### IMBd Dataset 


*imdb.name.basics.csv.gz*     

**nconst:** Unique identifier for names(of people, not movie titles)  <br>
**primary_name:** Full Name of person in movie industry <br> 
**birth_year:** year film industry person was born <br>
**death_year:** year of death <br>
**primary_profession:** Primary profession in the film industry <br>
**known_for_titles:** string of comma seperated *tconst* (unique title id of films for IMBd)<br>

 
*imdb.title.basics.csv.gz* 

**tconst:** Unique identifier for IMBd movie titles  <br>
**primary_title:** working title of movie <br> 
**original_title:** original title for movie release (untranslated) <br>
**start_year:** year of movie release <br>
**runtime_minutes:** float value of film length <br>
**genres:** string of comma seperated genre values<br>



*imdb.title.akas.csv.gz*   

**tconst:** Unique identifier for IMBd movie titles  <br>
**ordering:** indexes to go with each set of tconst <br> 
**title:** alt title specific to region <br>
**region:** region of particular title <br>
**language:** language of film (alot of missing data) <br>
**attributes:** descrpition of particular title (3D version, fake, etc)<br>
**is_original_title:** boolean check for original title (0.0 false, 1.0 true)<br>


imdb.title.crew.csv.gz    

**tconst:** Unique identifier for IMBd movie titles  <br>
**directors:** comma seperated string of *nconst* for directors <br> 
**writers:** comma seperated string of *nconst* for writers<br>



*imdb.title.principals.csv.gz*   

**tconst:** Unique identifier for IMBd movie titles  <br>
**ordering:** indexes to go with each set of tconst <br> 
**nconst:** Unique identifier for names(of people, not movie titles) <br>
**category** job category (actor, director, writer, etc) <br>
**job:** role of particular nconst (person) <br>
**characters:** list of characters played by nconst for tconst <br>


*imdb.title.ratings.csv.gz*

**tconst:** Unique identifier for IMBd movie titles  <br>
**averagerating:** 1-10 IMBd movie score weighted average (see link below for detailed explanation of IMBd ratings) <br> 
**numvotes:** number of votes by registered users to calculate the IMBd score <br>

[IMDb weighted average for ratings](https://help.imdb.com/article/imdb/track-movies-tv/weighted-average-ratings/GWT2DSBYVT2F25SK?ref_=helpart_nav_8#)


It seems that another column *ordering* must be used when there are duplicate tconst or nconst values to aid with indexing 


### The Movie Database

The Movie Database is an open alternative to IMDb with an easily accesible API. It is not as old as IMBd and therefore is less complete/established. 


**genre_ids:** list of Unique identifiers for TMDb genres <br>
**id:** unique id of movie title <br> 
**original_language:** abbrevated original language <br>
**original_title** string of original title <br>
**popularity:** score using various parameters to measure current popularity of title (see below for more info) <br>
**release_date:** date of movie release <br>
**title** working title of movie displayed on TMDb <br>
**vote_average:** average score 1-10 based on user votes <br>
**vote_count:** total number of votes for title rating <br>

[TMDb Popularity Explained](https://developers.themoviedb.org/3/getting-started/popularity)


### Rotten Tomatoes Dataset  

*rt.movie_info.tsv.gz*

**id:** unique identifiers for RT titles <br> 
**synopsis:** summary of movie plot <br> 
**rating:** Motion Picture Association film rating system rating (R, PG, etc) <br>
**genre** list of genres <br>
**director:** string of directors <br>
**writer:** string of writers <br>
**theater_date** date movie hit theaters <br>
**dvd_release:** date movie available on DVD <br>
**currency:** currency of box_office revenue <br>
**box_office** gross domestic box office revenue  <br>
**runtime:** total runtime of film in minutes <br>

*rt.reviews.tsv.gz*

**id:** unqie title identifier, primary key <br>
**review:** crtic review (paragraph of text) <br> 
**fresh:** fresh or rotten (good or bad) score by critic <br>
**critic** name of critic  <br>
**top_critic:** booleon to check if critic is top critic for title <br>
**publisher:** publishing company critic works for <br>
**date:** date crtic published review <br>

