# Leap_Assesment
Leap _ Assessment For the Purpose of my interview - this analysis is completely about the A/B testing and  binomial Distribution and baye's theorem
# Data Science Application Test

In this test, we would like you to write up an analysis about a mock experiment. We aim to measure your current knowledge in Data Cleaning, Exploratory Data Analysis and Drawing Conclusions from observations.

## Experimentation Details
We recently ran an A/B test on the cancellation page of our subscription service. Before running the test, members where able to cancel using a simple web form. The experiment aims measure the impact of forcing members to phone-in to our customer service line in order to cancel.

Information about the test:
- control group can cancel using a web form
- test group can only cancel by calling in
- Users were randomly assigned to a group when they go to the websites cancel page for the first-time
- The distribution probabilty between both groups is uneven (you can see this like an unfair coinflip)
- We've recored additional transactions generated after users were randomized
- REBILLs are Transactions recurring payments that were processed
- CHARGEBACKs or REFUNDs transactions represent payments that were cancelled

## Information About the Data
You will find the required data-sets for this analysis in the zip file. This is split in the following 2 csv files:
- [testSamples.csv](testSamples.csv)
- [transData.csv](transData.csv)

In testSamples.csv, you will find a list of unique users that were randomized in the A/B test.
* sample_id : is the unique identifier for the sample
* test_group : is the group in which the sample was placed, 0= control group, 1=test group

In transData.csv, you will find a list of transactions generated by randomized users after their randomization:
* transaction_id : is the unique identifier for the transaction
* sample_id : is a foreign key that links transactions to test samples
* transaction_type : is the transaction type for a transaction, can be REBILL, CHARGEBACK or REFUND
* transaction_amount : is the amount generated for a transaction, this can be a negative value

## Analysis Requirements

In this analysis we would like you to answer the following questions:

1. What is the aproximate probability distribution between the test group and the control group
2. Is a user that must call-in to cancel more likely to generate at least 1 addition REBILL?
3. Is a user that must call-in to cancel more likely to generate more revenues?
4. Is a user that must call-in more likely to produce a higher chargeback rate(CHARGEBACKs/REBILLs)?

Technical Requirements:

1. Analysis must be coded in R or Python
2. Analysis must be submitted to a github repository
3. Analysis must be written in markdown format
4. Please include at least 1 visualization with your analysis
5. Please use statistical significance tools to answer the questions we've asked
6. Include the code you used to perform the analysis in the github repository
7. Send us the link to your repository once you've completed the analysis

-----

We do not expect you to complete everything, but please work on what you can to the best of your ability.
