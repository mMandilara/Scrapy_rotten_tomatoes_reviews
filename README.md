# Scrapy_rotten_tomatoes_reviews
Here are two folders that use Scrapy Python framework to collect some critics' reviews from Rotten Tomatoes website.

Scrapy framework is a web scraper and web crawler that collects a few critics' reviews from Rotten Tomatoes website. Each folder has specific files for the main script to run, the most_popular_movies folder has the main Python script named "most_popular_movies.py" in path "most_popular_movies\most_popular_movies\spiders" and also for the least_rated_movies in the path "least_rated_movies\least_rated_movies\spiders" is the main script called "least_rated_movies.py". To run these crawlers, each one individually or each folder, these commands must be run in the terminal:


For the most popular movies: `scrapy crawl popular_movies`

For the least rated movies: `scrapy crawl bad_movies`

This works because, Scrapy runs the class of the spider / main script and since the classes are called 'popular_movies' and 'bad_movies' respectfully, you need to be in the same folder as the spider and then run the command in terminal.

So scrpay goes to the main page with the filter most popular, for example
![image](https://github.com/user-attachments/assets/78c5b5b5-a12b-49d2-bd2b-3976da4c3b73)

And then it searches for 300 pages, up to 800 movie titles. When it collects all the titles it keeps their URL as to go to the movies page and collect the first six reviews from critics. Then it saves the the movie title, URL, review as a text and the sentment of the review in a JSON file. These JSON files are named ```popular_reviews.json``` and ```bad_reviews.json```, where for the bad reviews the pages search are from 1 to 3 and the movie titles collected are up to 100 instead of 800.

![image](https://github.com/user-attachments/assets/9d6f3c03-e3c8-4e3d-bfee-08f43f6361f9)

![image](https://github.com/user-attachments/assets/a5c3edfc-986b-4ee1-a922-69ba5532d9f4)

And the results of the JSON files look like this:
```
{
    "title": "Carry-On",
    "url": "https://www.rottentomatoes.com/m/carry_on",
    "review": "Carry-On is never amazing, but it\u2019s an easy watch that contains plenty of thrills and two very reliable performers at its center. And it teaches people to be nicer to TSA agents this holiday season.",
    "sentiment": "POSITIVE"
},
{
    "title": "65",
    "url": "https://www.rottentomatoes.com/m/65",
    "review": "The premise doesn't hold up to close scrutiny and the narrative can be jarringly slow-paced.",
    "sentiment": "NEGATIVE"
},
{
    "title": "65",
    "url": "https://www.rottentomatoes.com/m/65",
    "review": "65 is a gruesome thing to watch, even for dinosaur lovers\u2014and not much fun, either.",
    "sentiment": "NEGATIVE"
}```
