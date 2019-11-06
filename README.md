# Starbucks Capstone Project
Project in Data Scientist Nanodegree of Udacity

* Table of Contents
* Installation
* Project Motivation
* File Descriptions
* Results
* Licensing, Authors, and Acknowledgements

## Installation

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python. The code should run with no issues using Python versions 3.*.

## Project Motivation

It is the Starbuck's Capstone Challenge of the Data Scientist Nanodegree from Udacity. We get the dataset from the program that creates the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers. We want to make a recommendation engine that recommends Starbucks which offer should be sent to a particular customer.

I'm interested to answer the following two questions:

* How many offers have been viewed and completed within required time?
* Which demograhic groups are more likely to compelete a offer?

## File Descriptions

The notebook available here showcases work related to the above questions.

This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

The data is contained in three files:

* portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* profile.json - demographic data for each customer
* transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

portfolio.json

* id (string) - offer id
* offer_type (string) - the type of offer ie BOGO, discount, informational
* difficulty (int) - the minimum required to spend to complete an offer
* reward (int) - the reward is given for completing an offer
* duration (int) - time for the offer to be open, in days
* channels (list of strings)

profile.json

* age (int) - age of the customer
* became_member_on (int) - the date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

transcript.json

* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours since the start of the test. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record

## Results

The main findings of the code can be found at the blog available here https://medium.com/@iris_yao/starbucks-capstone-project-28b4b0954596.

Based on the transcript records, I built three machine learning models (Logistic Regression, Random Forest and AdaboostClassifier) to predict if the offer would be viewed and completed. Eventually I picked Random Forest after comparison between accuracy, F1-Score and processing time.


## Licensing, Authors, Acknowledgements

Credit to Starbucks
