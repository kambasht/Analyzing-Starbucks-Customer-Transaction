# Analyzing-Starbucks-Customer-Transaction

Analyzing customer transaction at Starbucks to recommend and predict offers to existing and potential customers

# Table of Contents
1. Project Motivation
2. Project Tasks
3. File Descriptions
4. Running the code
5. Results
6. Licensing, Authors, and Acknowledgements

## Project Motivation

Starbucks offers rewards programs for customers on its mobile app. Concerted efforts in providing marketing and promotional offers to subscribers allows them to engage existing subscribers and provide a platform to attract potential customers.

Based on transactions with customers in the past, we can help analyze this data and serve potential customers with offer recommendations. Predictive modeling can help us predict which section of customers can be more likely to complete offers.

Our task will be to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type

## Project Tasks

I. Exploratory Data Analysis

Exploring the data to find patterns and dive into the details of the provided dataset

II. Data Cleaning and Merge

The raw data needs to be cleaned up and transformed to prepare it for analysis. We use data cleaning and transformation method to help derive a merged database for analysis

III. Observations and Recommendations

We look at specific parameters such as age, income and gender to help recommend similar offers for customers

IV. Data Modeling and Prediction

We use a xgboost model to help predict which customers are most likely to complete an offer based on previous transactions

V. Conclusion

## File Descriptions

The data is contained in three files:

portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)

profile.json - demographic data for each customer

transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

### portfolio.json

id (string) - offer id
offer_type (string) - type of offer ie BOGO, discount, informational
difficulty (int) - minimum required spend to complete an offer
reward (int) - reward given for completing an offer
duration (int) - time for offer to be open, in days
channels (list of strings)

### profile.json

age (int) - age of the customer
became_member_on (int) - date when customer created an app account
gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
id (str) - customer id
income (float) - customer's income

### transcript.json

event (str) - record description (ie transaction, offer received, offer viewed, etc.)
person (str) - customer id
time (int) - time in hours since start of test. The data begins at time t=0
value - (dict of strings) - either an offer id or transaction amount depending on the record

## Running the code

Installations required before running the code:
- no external libraries are required for installation

Folder structure:
- Place the method file 'method.py', data files and the jupyter notebook from the repo into a single folder and then run the notebook

## Results

Based on our analysis of the model factors like the minimum required spend needed to complete an offer, reward value , if the offer has been viewed or not are the most important factors which affect the process of offer completion

Other factors like income and gender are further down in the list of important measures that add to this result set.

The main findings of the code can be found at a post available [here](https://medium.com/@karan.ambasht89/5-things-you-should-know-for-your-next-trip-to-seattle-d6f93a43eea3).

## Licensing, Authors, Acknowledgements
Credits to [Starbucks](https://www.starbucks.com/) for the dataset
