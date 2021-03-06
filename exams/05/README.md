
## Social Birthdays (40 points)

You are obsessed with wishing people happy birthday on Facebook. If you
have a day where none of your friends on Facebook have a birthday, you
weep. Because you are quickly mastering simulation studies, you want to
figure out the probability that at least one of your Facebook friends
will have a birthday on every single day of the year (excluding leap
years).

1.  Write a function with a single argument `n`, which represents the
    number of Facebook friends you have. This function should return
    either `TRUE` or `FALSE` to indicate whether or not someone you know
    has a birthday on every day of the year. (For example, if n \< 365,
    your function should always return `FALSE`). (20 points)

2.  Using the function defined in step 1, run a simulation with 1,000
    repetitions when you have 2,000 Facebook friends and store the
    results. (10 points)

3.  Using the results from step 2, estimate the probability that, given
    2,000 Facebook friends, at least one of your friends has a birthday
    every day of the year. (5 points)

4.  Build a 95% confidence interval on your estimate from step 3. (5
    points)

BONUS (20 points) Let’s say you want to probability of being able to
wish at least one person happy birthday every day to be at least 75%.
Using the tools we’ve learned in this course, how many Facebook friends
do you need in order to achieve this probability level?

Create a plot with the number of friends on the X axis (starting at
2,000 and going to the number you discovered in the previous step) and
the probability of someone having a birthday every day of the year on
the Y axis. Include your upper and lower confidence interval bounds.

## E-commerce (65 points)

You work as a data scientist for a large e-commerce company. You are
responsible for understanding customer interactions with the company
website. You have determined that there are two distinct types of
customers who visit the website: Casual Browsers and Targeted Shoppers.
These visitors are defined by the following characteristics:

#### Casual Browsers

Time Spent on the Website (`t`): An exponential distribution with lambda
= 0.3 Purchase Coefficient (`s`): A beta distribution with alpha = 1 and
beta = 25

#### Targeted Shoppers

Time Spent on the Website (`t`): An exponential distribution with lambda
= 1.75 Purchase Coefficient (`s`): A beta distribution with alpha = 5
and beta = 4

The amount of money a shopper is likely to spend is defined as their
time spent on the website multiplied by their purchase coefficient (`t`
\* `s`).

Under current conditions, the number of daily visitors to the website is
defined by a poisson distribution with a lambda value of 10,000. Of
those visitors, 30% are Targeted Shoppers while the others are Casual
Browsers.

You have been asked to evaluate a proposed targeted ad campaign. It is
estimated that daily website visitors under this new campaign would be
defined by a poisson distribution with a lambda value of 8,000. Of those
visitors, 50% are expected to be Targeted Shoppers. You’re job is to
determine if the 30-day site revenue would be higher with this proposed
campaign in place.

Note: The following functions will be helpful with this question:
`rbeta()` `rexp()` `rpois()`

1.  Create a function that takes two arguments: `f`: A function defining
    the number of daily visitors to the site `p`: The proportion of
    daily visitors who are Targeted Shoppers This function should return
    a revenue value for 30 days. (30 points) *Note: this function should
    generate a unique number of customers (defined by `f`) for each of
    the 30 days, calculate how many customers are Targeted Shoppers and
    how many are Casual Browsers (defined by `p`), and then calculate a
    unique time spent (`t`) and purchase coefficient (`s`) for each
    customer. This information is finally all combined into a single
    estimate for revenue generated in 30 days.*

2.  Using the function defined in step 1, run a simulation with 1,000
    repetitions with the current conditions and store the results. (10
    points)

3.  Using the function defined in step 1, run a simulation with 1,000
    repetitions with the conditions expected under the new ad campaign.
    (10 points)

4.  Using the results from steps 2 and 3, estimate the 30-day revenue of
    the site under current conditions and the proposed ad campaign.
    Construct a 95% confidence interval for both estimates. (10 points)

5.  Based on your results, will the proposed ad campaign effectively
    increase site revenue? (5 points)
