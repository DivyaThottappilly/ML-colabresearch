# Exploratory Analysis - Will a customer accept the coupon?

## Overview 
In this first practical application assignment of the program, mainly trying to answer the question, “Will a customer accept the coupon?” The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those who did not. 

## Data
This data is from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, and passenger, and then asks people whether they will accept the coupon if they are the driver. There are three possible answers people can choose from:

“Right away”
“Later, before the coupon expires”
“No, I do not want the coupon”
The first two responses are labeled as “Y = 1,” and the third is labeled as “Y = 0.” There are five different types of coupons: Less expensive restaurants (under $20), coffee houses, carryout and takeaway, bars, and more expensive restaurants ($20–$50).

## Context
Imagine driving through town and a coupon is delivered to your cell phone for a restaurant near where you are driving. Would you accept that coupon and take a short detour to the restaurant? Would you accept the coupon but use it on a subsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaurant? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

## Data Description
Keep in mind that these values mentioned below are average values.

The attributes of this data set include:

User attributes
Gender: male, female
Age: below 21, 21 to 25, 26 to 30, etc.
Marital Status: single, married partner, unmarried partner, or widowed
Number of children: 0, 1, or more than 1
Education: high school, bachelors degree, associates degree, or graduate degree
Occupation: architecture & engineering, business & financial, etc.
Annual income: less than \$12500, \$12500 - \$24999, \$25000 - \$37499, etc.
Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she eats at a restaurant with average expense less than \$20 per person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
Contextual attributes
Driving destination: home, work, or no urgent destination
Location of user, coupon and destination: we provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
Weather: sunny, rainy, or snowy
Temperature: 30F, 55F, or 80F
Time: 10AM, 2PM, or 6PM
Passenger: alone, partner, kid(s), or friend(s)
Coupon attributes
time before it expires: 2 hours or one day
## Pre - Processing of data
Read coupons.csv in data folder and nvestigate the dataset for missing or problematic data.
Find missing data and Decide what to do about your missing data -- drop, replace, other...
Visualize different coupon type acceptance 

## Investigating the Bar Coupons
What proportion of bar coupons were accepted?

Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others. Is there a difference?

Compare the acceptance rates between those drivers who ...
go to bars more than once a month, had passengers that were not a kid, and were not widowed OR
go to bars more than once a month and are under the age of 30 OR
go to cheap restaurants more than 4 times a month and income is less than 50K.

### Summary of Acceptance of Bar coupons based on two conditons .
* Acceptance Rate of Bar coupons and Acceptance rate dependence on frequency 
* Acceptance rate for drivers who go to bars more than once a month, had passengers that were not a kid, and had occupations other than farming, fishing, or forestry.

### Summary 
Combined observations of above two criterias
There is a noticeable difference. The target group defined by these combined criteria (frequent bar visitors, no kids as passengers, and specific occupations) shows a significantly higher acceptance rate for bar coupons compared to all other drivers.

### Investigation on "Carry out & Take away" Coupons
What portions of " Carry out & Take away" coupons are accepted ?

Calculate acceptance rate of Carry and Take out coupns based on Education , Income and number of passengers

### Summary
* Overall Acceptance Rate for Carry out & Take away coupons:
  Proportion of accepted carry out & take away coupons: 0.74 (74)

There is a noticeable trend where individuals with Some High School education have a very high acceptance rate (0.94), which gradually decreases with higher levels of education, with Graduate degree (Masters or Doctorate) having the lowest acceptance rate (0.65).

Passengers accompanied by Friend(s) have the highest acceptance rate (0.76), while those with Kid(s) as passengers have the lowest (0.70).
