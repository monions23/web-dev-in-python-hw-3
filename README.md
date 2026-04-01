# Web Development in Python - Assignment 3: MongoDB Setup and Queries

## MongoDB Atlas Setup

Begin by **signing up for a MongoDB account** with the [link here](https://www.mongodb.com/cloud/atlas/register).

Second, **create a free cluster** (help available [here](https://www.mongodb.com/docs/guides/atlas/cluster/)) and **create a database user** (see link [here](https://www.mongodb.com/docs/guides/atlas/db-user/)).

Third, **configure a network connection** with the link [here](https://www.mongodb.com/docs/atlas/security/ip-access-list/). Atlas may give you a pop-up asking you to include your current IP address in your IP Access List; if so, make sure you click to include that IP address.

Fourth, **load some sample data** in your cluster (instructions in the link [here](https://www.mongodb.com/docs/atlas/sample-data/)]. For this assignment, I used **sample_mflix (sample movie data)**.

Lastly, **get a connection string** by going to your project homepage and clicking "connect" on your free cluster. Click that you have Compass installed; the connection string that appears will be what you will use.

## Installing MongoDB Community Edition

Note - ensure you have MongoDB Compass downloaded as well. You can use [this link](https://www.mongodb.com/try/download/compass) to do so.

Use [this tutorial](https://www.mongodb.com/docs/manual/administration/install-community/) to install MongoDB Community Edition for your computer.

Then, use the **connection string** from your setup to make a connection in MongoDB Compass.

## Writing Two Example Queries

Note - to query the sample_mflix dataset specifically, I ran the following command in the MongoDB Shell (which is available in the Compass GUI):

```use sample_mflix```

1) Find all movies with runtime greater than 200 minutes in year 1983. The result should include a list of objects sorted by runtime increasing, and each object only has three fields: runtime, title, year.

I entered the following query into the MongoDB Shell: 

```db.movies.find({"runtime": {$gt: 200}, "year": 1983}, {"runtime": 1, "title": 1, "year": 1}).sort({"runtime": 1})```

This effectively found movies with a runtime greater than 200 and a release year of 1983. The attributes selected to be printed in the output were runtime, title, and year; I accomplished this by placing these three fields in the projection clause of the query. Then, the '.sort({"runtime", 1})' sorted a list of objects by runtime increasing.

<img width="710" height="1156" alt="image" src="https://github.com/user-attachments/assets/a8351732-5153-4b82-8050-ac74c55b2d94" />

2) Find all movies after year 2014 with imdb rating greater than 9.

I entered the following query into the MongoDB Shell:

```db.movies.find({"year": {$gt: 2014}, "imdb.rating": {$gt: 9}}, {"title": 1, "year": 1, "imdb.rating": 1}).sort({"imdb.rating": -1})```

This found all movies released after 2014 with an IMDB rating greater than 9. The attributes projected into the output were title, year, and imdb rating, and the results were sorted by IMDB rating in descending order.

The output was the following:

<img width="842" height="780" alt="image" src="https://github.com/user-attachments/assets/64229398-e5a6-44b8-a416-457bd3612641" />

