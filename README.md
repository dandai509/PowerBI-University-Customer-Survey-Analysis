# Recreation Centre Customer Survey Analysis
## Business Problem
The University of Auckland Recreation Center conducts customer surveys on an annual basis. The goal is to find out how customers rate our services and seek space for improvement. In the 2022 report, various questions were asked, and raw data were gathered from UoA website. As an operations coordinator, I’m responsible for generating a report by using Power BI to the manager to make operational decisions based on the data findings.

![00](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/93767468-b386-485a-8e55-276dc38bfd9d)


## Data Clean and Transformation

Initial data has 349 responses, and participants have been asked to rate our service from 0-7, 0 being extremely unsatisfied and 7 being extremely satisfied. 

Raw data was collected from Oracle service cloud and exported in Excel format. First a refrence table called Rating is created in the raw data excel sheet. This table will be used to convert rating to numbers for futher calculation. Second we import this Raw Data Table into Power BI. I select Survey raw data and Rating table to transform to Power BI, then I duplicate the Survery Raw data, seperated it as Facility Feedbacks, Group Fitness Feedbacks and General table, General table has surveyers names, IDs, Emails etc. Date transforamation tecniques such as replace null value, remove columns, promote headers and filters rows were applied.

![Picture1](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/b03cd758-755a-413a-a53e-9556a958ee83)
![Picture2](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/9e7a2a2a-af76-4cb2-b5e6-b264fe80a4d4)


I then Selected UoA ID, selected Unpivoted the other columns in Facility Feedbacks table, which gives feedbacks and rating score. I then Mergeed Facility Feedbacks table and Rating table by left joining two tables by rating score column. I then expaned the Rating Column by chosing Rating, I now have an extra column which I renamed as Rating and has ratings.

![Picture3](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/392f7033-c692-4d76-a4df-b378d4dfbeff)
![Picture4](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/8e6eb314-795c-4a87-ae32-e5c713f3b22d)


Lastly, I added an conditional column named it Overall Satisfaction. Any scores that is greater or equal to 5 will be considered Satisfied. Less then and equal to 3 is Unsatisfied. Else will be Neutral.
Data transformation is now completed and I move on to Data modeling.
![Picture5](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/9617138f-3e8b-4162-b9b4-5fcf5944411c)

## Data Modeling

In Model view, the relationships between tables were automatic created. Since I already merged Rating and Facility Feedbacks table, Rating and Group Fitness Feedback table in power query, I no longer need the relationship, therefore I deleted it. The One to many relationship between General Table and Facility Feedback table is linked by UOA ID column.

![Picture6](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/6a2a9aa2-9ba8-458a-bcdf-eb1c909e90ef)


## Data Analysis
In total 287 respondents from the online survey. 92% of them are currently UoA Recreation Centre members. If members rate 5 or above, we consider that they are satisfied. 3 and 4 being neutral, anything 2 or below is considered unsatisfied. 

Overall, 60% of the members are satisfied, 24% are neutral, and 16% are unsatisfied. Members are most satisfied with our facility's cleanness, with an average score of 5.85, and only 9 respondents said they were not satisfied. 

In Group Class feedback, members are most satisfied with the quality of the instructors, with an average score rating of 5.63.

![Dashboard](https://github.com/user-attachments/assets/42af060a-3b75-4335-a597-2550c0880cc0)

Members are very happy about our staff presentation and professionalism, fitness and reception staff are very helpful in terms of helping them on the gym floor. On the other hand, members are unhappy about how they make friends in the gym. Almost half of the respondents said the gym did not connect them with new friends or community. Further, members feedback showed that the rec centre need to send more communication both via social media and email.

![Feedbacks Rating Score](https://github.com/user-attachments/assets/e2044195-7c0e-4187-8d12-403551473753)

Further more in drill through, members feeling towards connection them with new friends are mostly diversed. rating score 1-7 are quite evenly distributed with close 50 members for each score. on the other hand, Facility Cleanness and Staff Presentation right skewed meaning thenumber of members who giving the highest rating score are the most.
![DrillThrough](https://github.com/user-attachments/assets/5af21d4a-c1a7-4f73-a09e-a2ef0ab5c268)

## Summary

To conclude, overall satisfaction rate is 60%, with 24% respndents unsatisfied. Overall Satisfaction Score is 4.8 out of 7. Connection with Friends for members has the lowest average satisfaction score of 3.94. Facility Cleanness has the highest average satisfaction score of 5.85.

## Recommendations 

Customer service team to engage more members in social media, e.g posting news, group class photo, weekly challenges to increase the engagement of the students.

Adding monthly newsletter for all members, including centre events, membership specials, members engagement photos etc																			
Create fun social events to let members get to know each other, to create a sense of community e.g members night, bring friends to work out etc.


