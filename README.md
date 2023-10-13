# AB_test

### Assigned tasks description: 
1. Worked closely with Marketing Department of online retail store to complile a list of 9 hypotheses to boost revenue.
Each hypothesis were specified according to Reach, Impact, Confidence and Effort. Prioritized the hypotheses according to ICE and RICE frameworks.
Identified the difference between the frameworks.
2. Conducted A/B tests.
3. Analyzed A/B tests by creating visualizations.

### Description of the data


#### Data used for RICE and ICE frameworks



/datasets/hypotheses_us.csv 


Hypotheses — brief descriptions of the hypotheses



Reach — user reach, on a scale of one to ten


Impact — impact on users, on a scale of one to ten


Confidence — confidence in the hypothesis, on a scale of one to ten


Effort — the resources required to test a hypothesis, on a scale of one to ten. The higher the Effort value, the more resource-intensive the test.


#### Data used for A/B tests


 /datasets/orders_us.csv

 
transactionId — order identifier


visitorId — identifier of the user who placed the order


date — of the order


revenue — from the order


#### group — the A/B test group that the user belongs to


/datasets/visits_us.csv


date — date


group — A/B test group


visits — the number of visits on the date specified in the A/B test group specified


#### Cumulative revenue by group.
![image](https://github.com/gzhuldas/AB_test/assets/72769986/405c619d-4595-4188-9763-38b468a6e2f0)


Analysis:
Up until mid-August the cumulative revenue gained from both groups were relatively stable and tended to increase. But after that group B had a sudden spike reaching about 60000, while group A stayed at around 30000. This is definitely related to an increase of average order size in group B from the previuos graph. If the number of orders for both groups on 20/08/19 did not change compared to previous dates that would mean that clients of group B either spent more money in general or somebody made a very expensive purchase which led to the distortion of results.

#### Cumulative average order size by group.

