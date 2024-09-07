How to start a data engineer project:


In this project, we apply Data Modeling with Postgres and build an ETL pipeline using Python. A startup wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. Currently, they are collecting data in json format and the analytics team is particularly interested in understanding what songs users are listening to.



What types of data engineer projects do we have:

Types of projects:

Extract data from JSON files

Transform the data in Python to fit the star schema structure

Load the transformed data directly into the final PostgreSQL star schema tables


How to setup such a problem?
We need to setup business questions.
We need to define the measured, meaning what do we want to see that will be queried often?
What are the data sources





From the previous project we get the following questions:

Why dont we do any staging, and when can we decide to use staging or not?

Answer: We do stagining, if the volume of the data to fetch is too big, we do it if we want to have a central hub. we do it if we want to diminsh the querying time / the hardness on the source.
We do it if we want to give control to only certain parts of the source.we do it if the transformtion we want to make are too complex.

So we use the staging depedning on the volume of the data really, we use it also depedning on the type of transformations we desire to make.

Can act a central hub of data from multiple sources, basically as a buffer.

Users will be querying from the data wharehouse, so they wont be affected.

I am only seeing stagining as a way to act as a buffer/ stopping hitting the retry button when we want to make new calls / transformation, sicne the data will be there, and we wont be botthering the main source.

We dont do it if the data source is simple.



