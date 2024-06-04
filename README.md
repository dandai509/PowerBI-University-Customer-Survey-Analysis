# Recreation Centre Customer Survey Analysis
## Business Problem
The recreation center conducts customer surveys on an annual basis. The goal is to find out how customers rate our services and seek space for improvement. In the 2022 report, various questions were asked, and raw data were gathered from UoA website. As an operations coordinator, I’m responsible for generating a report by using Power BI to the manager to make operational decisions based on the data findings.

![00](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/93767468-b386-485a-8e55-276dc38bfd9d)


## Data Clean and Transformation

Initial data has 349 responses, and participants have been asked to rate our service from 0-7, 0 being extremely unsatisfied and 7 being extremely satisfied. 

Raw data was collected from Oracle service cloud and exported in Excel format. First a refrence table called Rating is created in the raw data excel sheet. This table will be used to convert rating to numbers for futher calculation. Second we import this Raw Data Table into Power BI. I select Survey raw data and Rating table to transform to Power BI, then I duplicate the Survery Raw data, seperated it as Facility Feedbacks, Group Fitness Feedbacks and General table, General table has surveyers names, IDs, Emails etc. Date transforamation tecniques such as replace null value, remove columns, promote headers and filters rows were applied.

![Picture1](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/b03cd758-755a-413a-a53e-9556a958ee83)
![Picture2](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/9e7a2a2a-af76-4cb2-b5e6-b264fe80a4d4)


I then Selected UoA ID, selected Unpivoted the other columns in Facility Feedbacks table, which gives feedbacks and rating score. I then Mergeed Facility Feedbacks table and Rating table by left joining two tables by rating score column. I then expaned the Rating Column by chosing Rating, I now have an extra column which I renamed as Rating and has ratings.

![Picture3](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/392f7033-c692-4d76-a4df-b378d4dfbeff)

![Picture4](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/2116287d-efb5-4ec8-95c2-db49faf73e61)

Lastly, I added an conditional column named it Overall Satisfaction. Any scores that is greater or equal to 5 will be considered Satisfied. Less then and equal to 3 is Unsatisfied. Else will be Neutral.
Data transformation is now completed and I move on to Data modeling.
![Picture5](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/1e48215b-5b80-4021-abe3-d42f7ccdb283)

## Data Modeling

In Model view, the relationships between tables were automatic created. Since I already merged Rating and Facility Feedbacks table, Rating and Group Fitness Feedback table in power query, I no longer need the relationship, therefore I deleted it. The One to many relationship between General Table and Facility Feedback table is linked by UOA ID column.

![Picture6](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/6a2a9aa2-9ba8-458a-bcdf-eb1c909e90ef)

![1](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/de9154b2-10fd-481b-b935-63e661f7415f)

## Data Analysis

![11](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/77e65e1d-a4c6-400d-916b-6f1d887b8e9d)

85% of the survey respondents have completed the full survey. The rest of the 15% has only partially completed.

![22](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/3873b03d-8761-45c2-bf78-506b66f183d0)

Overall, 97% of respondents said they were satisfied with the service that the recreation provides. 5% are netural and 17% that is not satisfied with the service

![33](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/5c94ae69-9c7f-4d9c-b4ba-3e735b99bdab)

Members are very happy about our staff presentation and professionalism, fitness and reception staff are very helpful in terms of helping them on the gym floor. On the other hand, members are unhappy about how they make friends in the gym. Almost half of the respondents said the gym did not connect them with new friends or community. Further, members feedback we need more communication both via social media and email.

![44](https://github.com/dandai509/Customer-Survey-Analysis/assets/106848444/2b5559b3-9aa4-4fd4-8b07-96b3ff7f5502)

The Clean and Hygieness achieved one of the best satisfaction levels, only 9 respondents said they were not satisfied. 

## Summary

Overall satisfaction rate reached 77%, 85% of the students who paticipated in survey has completed it. Communication via emails or social media has the low satisfaction rate. Staff professionalism and presentation reach a very high level of satisfaction. In Total, out of 349 students, only 9 students are not satisfied with general cleaningness.

## Recommendations 

Customer service team to engage more members in social media, e.g posting news, group class photo, weekly challenges to increase the engagement of the students 											
Adding monthly newsletter for all members, including centre events, membership specials, members engagement photos etc																			
Create fun social events to let members get to know each other, to create a sense of community e.g members night, bring friends to work out 	


