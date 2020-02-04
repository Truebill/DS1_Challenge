# Truebill Data Science Challenge
This repository contains synthetic data for the Truebill Recruiting process.

If you've come across this repository on your own, feel free to take a look at the data. If you think you'd be interested in helping us in our mission to help the financial health of millions of people, we're hiring! We encourage you to check out our opportunities at https://angel.co/company/truebill/jobs.

## Instructions for Candidates:
A/B tests play a huge role in website optimization. Analyzing A/B tests data is a very important data scientist responsibility. Especially, data scientists have to make sure that results are reliable, trustworthy, and conclusions can be drawn. In this challenge, you will have to analyze results from an A/B test. 

## Challenge Description
Company XYZ is a worldwide e-commerce site with localized versions of the site.

A data scientist at XYZ noticed that Spain-based users have a much higher conversion rate than any other Spanish-speaking country. She therefore went and talked to the international team in charge of Spain And LatAm to see if they had any ideas about why that was happening. Spain and LatAm country manager suggested that one reason could be translation. All Spanish- speaking countries had the same translation of the site which was written by a Spaniard.

They agreed to try a test where each country would have its one translation written by a local. That is, Argentinian users would see a translation written by an Argentinian, Mexican users by a Mexican and so on. Obviously, nothing would change for users from Spain.

## You are asked to:
- Check to see if users from Spain actually tends to convert more than the users from other countries
- Are the localized translations really worse? Is it possible that there is selection bias? 

Present to us your findings on the above - statistical reasoning will be valued. Presentation of your results can be in whatever format you see best - Jupyter notebook, PPT/PDF/DOC. Language of choice is up to you - Python is preferred. Please share your code.

## Evaluation

The following artifacts are valued:

- Explanations of your intent, methods, conclusions and any assumptions
- Clear, documented, and well-structured code
- Methods you attempted that didn't work
- Ideas you didn't have time to complete but would have done with more time
- A thorough write up with any pertinent visualizations

## Data
We have two tables downloadable in the repository. The two tables are:

### “test_table”
This contains general information about the test results.

Columns: 
- user_id
- date
- source : This is the marketing channel and consist of either Ads, SEO, Direct. Direct means everything except for ads and SEO
- browser_language
- ads_channel : if marketing channel is ads, this is the site where the ad was displayed
- browser : browser used
- conversion : 1 for a user successfully converting, 0 for not converting.
- test : users are randomly split into test (1) and control (0). Test users see the new translation and control the old one. For Spain-based users, this is obviously always 0 since there is no change there.

### “user_table”
This contains some information about the user

Columns:
- user_id : the id of the user. It can be joined to user id in the other table
- sex : user sex: Male or Female
- age : user age (self-reported)
- country : user country based on ip address
