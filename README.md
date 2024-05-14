# UCB-ML-AI-Project-5.1


READ ME FILE

This is the first Practical Application Assignment (assignment 5.1) for the UC Berkeley Professional Certificate in Machine Learning and Artificial Intelligence, summer 2024.

COLLABORATION: I collaborated on interpreting the requirements of the problem assignment questions and on debugging code with a fellow student.

DATA CLEANING: For columns with null values, I replaced the null with zero/none/never. I did not extrapolate or interpolate to replace the null entries with any non-zero values.

PART 1

ANALYSIS – Guided Investigation: 

2. What proportion of bar coupons were accepted?
Across all observations, 58.9985% of bar coupons were accepted.

3. Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more.
Acceptance rate for people who have been to a bar 3 or fewer times in the last month is 56.1595%.
Acceptance rate for people who have been to a bar 4 or more times in the last month is 62.2456%.
I analyzed acceptance rate across all coupon types, not just bar coupons, because the question did not specify only bar coupons.

4. Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to all others. Is there a difference?
Acceptance rate for people who go to a bar more than once a month and are over 25 is 62.1534%.
Acceptance rate for people who are not in the group going to a bar more than once a month and over 25 is 55.3548%.
I analyzed acceptance rate across all coupon types, not just bar coupons, because the question did not specify only bar coupons.

5. Use the same process to compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry.
Acceptance rate for people who go to a bar more than once a month and have no kid passenger is 62.3%.
Acceptance rate for people who go to a bar more than once a month and have no kid passenger and not in Farming, Fishing & Forestry occupation is 62.3106%.
NOTE: This is exactly the same percentage as bar more than once per month and no kid passenger.
With only the Bar>1 and Passenger != kids, there are no observations that include the occupation
of Farming Fishing & Forestry. Therefore, adding the filter to remove Farming Fishing & Forestry
drivers from the calculation did not change the number of driver observations.
I analyzed acceptance rate across all coupon types, not just bar coupons, because the question
did not specify only bar coupons.

6. Compare the acceptance rates between those drivers who:
•	go to bars more than once a month, had passengers that were not a kid, and were not widowed OR
•	go to bars more than once a month and are under the age of 30 OR
•	go to cheap restaurants more than 4 times a month and income is less than 50K.
I analyzed acceptance rate across all coupon types, not just bar coupons, because the question did not specify only bar coupons.

Comparing the acceptance rates between these groups of drivers:

•	62.3106% if they go to bars more than once a month, had passengers that were not a kid, and were not widowed.
•	62.8081% if they go to bars more than once a month and are under the age of 30.
•	60.0702% if they go to cheap restaurants more than 4 times a month and income is less than 50K.
There is surprisingly little percentage difference between the different groups of drivers. All categories and sub-categories of drivers analyzed were in the 56-63% acceptance range.

7. Based on these observations, what do you hypothesize about drivers who accepted the bar coupons?
From this analysis, it appears that drivers who go to bars more than once a month and are under the age of 30, have the highest coupon acceptance rate (62.8081%) of all categories examined in this assignment. 

PART 2

ANALYSIS – Independent Investigation: 

I am interested in looking at how people with kids as passengers in the car varied their acceptance rate depending upon how far the business was from their current location.

VALUE COUNT ANALYSIS: For coupon acceptance rate, dependent upon distance from driver's current location: As would be expected, the closer the business, the high the coupon acceptance rate.

5.0 - 14.9 min     5,562 counts    61.4168% accepted the coupon.
15.0 - 24.9 min    5,611 counts    56.0684% accepted the coupon.
25.0 min & more    1,511 counts    42.8855% accepted the coupon.

Across all driver categories, for driving distances in the 5-14 minute range and 15-24 minute range, more coupons were accepted than ignored. But, for distances over 25 minutes, the opposite was true, and more coupons were ignored than accepted.

ANALYSIS: It is interesting that generally coupons were only offered when drivers were alone or with partners, not with friends or kids. This is not connected to acceptance rate necessarily, but it might say something about who is signing up to receive coupon offers.

RECOMMENDATION: It might be beneficial to evaluate how drivers are being selected to receive coupons, independent of which coupons they receive. Some valuable customer bases are possibly being missed.

ANALYSIS: With kids in the car, acceptance rate is 50.497%, but without kids in the car, acceptance rate is 57.39%. This result suggests that having kids in the car makes a driver a less valuable target for sending coupons while driving.

RECOMMENDATION: If parents are busy or distracted while driving with their kids it is not a great time to send them coupons. To not overburden drivers with coupons they do not want or cannot use, avoid sending coupons to people who have kids during the hours of 7-9am and 2-4pm while they may likely be driving their kids to and from school.

