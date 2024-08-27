# Movie Recommender System

This is a movie recommending site, that recommend movies based on the ratings given by users previously on different movies in different genre, Initially after first login, user is given set of Top movies in each genre using IMDB's weighted rating formula Weighted Rating (WR), After every 5 rating that the user rates, system runs the KNN algorithm to recommend the movies to the user based on the rating given by similar users, update the list of the movies that are shown to the user. The recommended movies are placed under mixed section which appears after the user has rated atleast 5 movies.

The data for the ratings and users are used from the kaggle movies dataset, complete data was not used due to hardware limitations , only small part of the data is being used in this project.  


## Getting Started

To run the web server on local machine follow these steps:

Create a virtual environment in the machine using command :``` virtualenv venv```
Before installing from the requirements folder some dependecies are needed to be installed
```  sudo apt-get install libmysqlclient-dev ```
```  pip3 install sudo numpy  ```
After creating the vitual environment install all the libraries and modules used using command : ``` pip3 install -r requirements.txt ```
Run the application using command :``` python3 app.py```

If error persist check which modules are missing from the logs and download them using ```pip3 install ```command

### Prerequisites

Virtual environment is required if not present in the system please install it using command : ``` pip3 install virtualenv ```
Mysql is used as a database to install mysql use command : ``` sudo apt-get insall mysql-server``` ``` sudo apt-get install mysql-client ```

Mysql settings :
A database is to be created with 2 tables in them

Table 1 : users table  
Table 2 : ratings table  

To create users table and ratings table use the following commands : 

``` CREATE TABLE users(id INT(11) AUTO_INCREMENT PRIMARY KEY,name VARCHAR(100),email VARCHAR(100),username VARCHAR(30),password VARCHAR(100),rated VARCHAR(10),movie1 VARCHAR(10),movie2 VARCHAR(10),movie3 VARCHAR(10),movie4 VARCHAR(10),movie5 VARCHAR(10),movie6 VARCHAR(10),movie7 VARCHAR(10),movie8 VARCHAR(10),movie9 VARCHAR(10),movie10 VARCHAR(10)); ```

``` CREATE TABLE ratings(id INT(11) AUTO_INCREMENT PRIMARY KEY, userId VARCHAR(100),movieId VARCHAR(100),imdbId VARCHAR(100),rating VARCHAR(5),rating_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP); ```

## Deployment

To Deploy the project on the cloud follow this small [youtube series](https://www.youtube.com/watch?v=-Gc8CMjQZfc&list=PL5KTLzN85O4KTCYzsWZPTP0BfRj6I_yUP) specially for flask app deployment on aws ec2 : 

## Built With

* [Flask](http://flask.pocoo.org/) - The web framework used
* [MySql](https://www.mysql.com/) - Database used
* [The Movies Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset) - The Movies Dataset used

#### Note  

Main focus of this project is to integrate machine learning algorithm in website.  
Edge cases for login and route checking middleware are not used in this project
