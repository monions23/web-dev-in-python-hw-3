# Web Development in Python - Assignment 3: MongoDB Setup and Queries

## MongoDB Atlas Setup

Begin by **signing up for a MongoDB account** with the [link here](https://www.mongodb.com/cloud/atlas/register).

Second, **create a free cluster** (help available [here](https://www.mongodb.com/docs/guides/atlas/cluster/)) and **create a database user** (see link [here](https://www.mongodb.com/docs/guides/atlas/db-user/)).

Third, **configure a network connection** with the link [here](https://www.mongodb.com/docs/atlas/security/ip-access-list/). Atlas may give you a pop-up asking you to include your current IP address in your IP Access List; if so, make sure you click to include that IP address.

Fourth, **load some sample data** in your cluster (instructions in the link [here](https://www.mongodb.com/docs/atlas/sample-data/)]. I chose **sample_mflix (sample movie data)** and **sample_restaurants (sample_restaurant data)**.

Lastly, **get a connection string** by going to your project homepage and clicking "connect" on your free cluster. Click that you have Compass installed; the connection string that appears will be what you will use.

## Installing MongoDB Community Edition

Note - ensure you have MongoDB Compass downloaded as well. You can use [this link](https://www.mongodb.com/try/download/compass) to do so.

Use [this tutorial](https://www.mongodb.com/docs/manual/administration/install-community/) to install MongoDB Community Edition for your computer.

Then, use the **connection string** from your setup to make a connection in MongoDB Compass.
