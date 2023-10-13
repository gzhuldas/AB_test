# A/B test. Prioritizing and testing hypotheses for online retail store.

### Assigned tasks description: 
1. Worked closely with Marketing Department of online retail store to complile a list of 9 hypotheses to boost revenue.
Each hypothesis was specified according to Reach, Impact, Confidence and Effort. Prioritized the hypotheses according to ICE and RICE frameworks.
Identified the difference between the frameworks.(More about that in Python Notebook, ipynb file)
2. Conducted A/B tests.
3. Analyzed A/B tests by creating visualizations.
   
### Description of the data


#### Data used for RICE and ICE frameworks


/datasets/hypotheses_us.csv <br> Hypotheses — brief descriptions of the hypotheses<br>Reach — user reach, on a scale of one to ten<br>Impact — impact on users, on a scale of one to ten<br>Confidence — confidence in the hypothesis, on a scale of one to ten<br>Effort — the resources required to test a hypothesis, on a scale of one to ten. The higher the Effort value, the more resource-intensive the test.


#### Data used for A/B tests


 /datasets/orders_us.csv<br>transactionId — order identifier<br>visitorId — identifier of the user who placed the order<br>date — of the order<br>revenue — from the order
#### group — the A/B test group that the user belongs to


/datasets/visits_us.csv<br>date — date<br>group — A/B test group<br>visits — the number of visits on the date specified in the A/B test group specified


There were mistakes in the original datasets; some of the visitors might have gotten into both group A and group B. So the data were divided into filtered and unfiltered versions. A/B tests were conducted for both versions.


### A/B tests results for filtered and unfiltered data versions.
The tests showed that there is difference in conversion rates between groups with both raw and filtered data. The test of average order size showed that there is no difference between the groups with both raw and filtered data. The test for raw data has shown that there is a relative revenue gain of 28% in group B compared to group A, the results for the filtered data are opposite. They showed that there is, on the contrary, a relative revenue loss of 3%. Large relative revenue gain in group B with raw data was probably due to abnormal order sizes. The test should be stopped since there is no difference between the groups. 


### Data Visualizations
#### Cumulative revenue by group.
![image](https://github.com/gzhuldas/AB_test/assets/72769986/405c619d-4595-4188-9763-38b468a6e2f0)


Analysis:<br>Up until mid-August the cumulative revenue gained from both groups were relatively stable and tended to increase. But after that group B had a sudden spike reaching about 60000, while group A stayed at around 30000. This is definitely related to an increase of average order size in group B from the previuos graph. If the number of orders for both groups on 20/08/19 did not change compared to previous dates that would mean that clients of group B either spent more money in general or somebody made a very expensive purchase which led to the distortion of results.

#### Cumulative average order size by group.
![image](https://github.com/gzhuldas/AB_test/assets/72769986/e826b41e-9e52-4b74-82b9-bb30e2b97a3e)


Analysis<br>Average order size made by group B increased significantly in the second half of August. Then it gradually decreased while being higher than that of the group A anyway. Around 150 and 110 for groups B and A, respectively. Interestingly, during the first half of the month the increase of average order size for one group were followed by a decrease for another group. It is probably unreliable to make conclusions based on this metric since the graphs have not shown stable results.


#### The relative difference in cumulative average order size for group B compared with group A.
![image](https://github.com/gzhuldas/AB_test/assets/72769986/676b6b7a-b02e-4c68-924c-f2ba31de6d5a)

Analysis:<br>The results are not stable and great spikes are probably related to abnormal purchases made in group B.

#### The daily conversion rates of the two groups.
![image](https://github.com/gzhuldas/AB_test/assets/72769986/42d7f513-365e-46a1-b1ff-6f07339da6cc)

Analysis:<br>The conversion rate for group A was much higher at the beginning but it drastically decreased by the end of the first week. The conversion rates stabilized in the end and were practically same for both groups.

#### A scatter chart of the number of orders per user.
![image](https://github.com/gzhuldas/AB_test/assets/72769986/2b98a330-aca6-4509-ba70-4647dc325cd1)

Analysis:<br>The scatter plot which represents the number of orders per user shows that most clients made only one order. And nobody made more than 3 orders that month in general.

#### A scatter chart of order prices.
![image](https://github.com/gzhuldas/AB_test/assets/72769986/94d69ed8-7578-48f2-a633-6460b4ef7678)

Analysis:<br>The scatter plot with order prices shows that the majority of orders does not exceed 1000. There are two outliers of 20000 and 2500.

### Results:

Several graphs have been shown the average order prices between the groups and the relative difference for B compared to A. Cumulative revenue by group and the daily conversion rates for the whole month. The data used for the graphs were not filtered, which can be a probable reason why the results for group B are so different. All the graphs except for the daily conversion rates showed a huge increase in orders and revenue for group B in mid-August. Further research with data filtration has justified the assumptions about abnormalities in group B.<br>Hypotheses testing has shown that the test should be stopped since the groups have not shown any significant differences. 


