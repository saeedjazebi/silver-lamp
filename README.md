# silver-lamp
The link for the Jupyter notebook for this project is: https://github.com/saeedjazebi/silver-lamp/blob/main/silver_lamp.ipynb

Amazon is assessing a new service that can increase local business traffic by offering coupon to drivers in the area. Will it be a successful service or business? 

The goal of this project is to use visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

The data comes from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\$20 - $50).
First, the proper libraries are imprted: matplotlib, seaborn, pandas, numpy, and plotly
Next, the data is improted with read_csv function
Next by reviewing the data fields, there seems to be some missing data, specifically in column "car". Also, columns, Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, and Restaurant20To50 also missing data. I decided to remove the column "car" entirely since virtually no data is available for this column. For the other columns, the rows with missing data are removed with dropna method.
What proportion of the total observations chose to accept the coupon? %56.9
Bar plot is used to visualize the coupon column. The coffee house coupons are more than other offers and expensive restaurants are the lowest.
A histogram is used to visualize the temprature column. The cuopons are offered more when the temprature is higher. 
Used a scatter plot to see if there is correlation between temprature and number of coupon types. There was none. 
A dataframe is created with only "Bar" coupon data
What proportion of bar coupons were accepted? %41.2
The acceptance rate between those who went to a bar 3 or fewer times a month to those who went more are compared with a bar plot. People that go to bars between 4-8 times are more likely to accept the cuopons. 
Then, the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others are compared. The data is queried for this population of the data and compared to overal acceptance rate by a pie chart. The acceptance rate is almost %67 higher than the entire population.
The population that had occupations of "farming, fishing, or forestry" were removed from the data set. The same process above was implemented to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid vs. they were a kid. When there was no kid, the accepptance rate was much higher (%70 vs. %38)
To have a better understanding about the relationships between passanger and bar columns and the acceptance rate, a barh plot is used to plot different combinations, which shows for group where kids are present and the person goes to bar more than 8 times, the acceptance rate is higher.
Three cases were compared with a pie chart, and it seems that people that go to bars more than one time a month and are under age of 30 are more likely to accept the coupons. 
My independent investigation revealed couple of general observations listed bellow:
The higher the temprerature the higher the chances of accepting the ticket
If the person is not going to an urgent place, it is more likely to accept the coupon
If they are with friends, they are more likely to accept the ticket
Noon time is the best time to offer the coupon
They accept the cuopon if they have more time to use it
Males are more likely to accept the offer
Younger people are more interested in cuopons
Single people are more interested in cuopons
If they do not have childeren they are more interested
Less graduated are more interested
Less income are more interested
