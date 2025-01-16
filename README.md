# Scrapy_rotten_tomatoes_reviews
Here are two folders that use Scrapy Python framework to collect some critics' reviews from Rotten Tomatoes website.

Scrapy framework is a web scraper and web crawler that collects a few critics' reviews from Rotten Tomatoes website. Each folder has specific files for the main script to run, the most_popular_movies folder has the main Python script named "most_popular_movies.py" in path "most_popular_movies\most_popular_movies\spiders" and also for the least_rated_movies in the path "least_rated_movies\least_rated_movies\spiders" is the main script called "least_rated_movies.py". To run these crawlers, each one individually or each folder, these commands must be run in the terminal:


For the most popular movies: `scrapy crawl popular_movies`

For the least rated movies: `scrapy crawl bad_movies`

This works because, Scrapy runs the class of the spider / main script and since the classes are called 'popular_movies' and 'bad_movies' respectfully, you need to be in the same folder as the spider and then run the command in terminal.
