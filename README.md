# Bike-Share_Case_Study
This is a documentation of my capstone project in the [Google Data Analytics Professional Certificate](https://www.coursera.org/google-certificates/data-analytics-certificate) course. The study is on subscriber data of a fictional bike sharing company that invesitgates the ways its members and casual riders use bikes differently. 

# Scenario
Lindsay Silk-Kremenak, Director of Marketing for the Chicago area’s Divvy bike-share program, understood the company’s future success depended on a focused approach to marketing that maximized the number of annual memberships. She was sure that data analysis could unlock the insights needed to design marketing strategies that would help her achieve that objective. But what Lindsay knew most certainly was that Divvy’s executive team would only support her team’s recommendations if members communicated their insights through expertly crafted data visualizations.

We will investigate existing dataset from Divvy case study ["'Sophisticated, Clear, and Polished’: Divvy and Data Visualization"](https://artscience.blog/home/divvy-dataviz-case-study) written by Kevin Hartman, to determine if there are any trends that we can identify. These insights will then be used to give high level recommendations to guide the marketing strategy for the company.

# 1.0 Ask 

### 1.1 Business Task:
Maximize the annual membership of Divvy Bike-share program by analyzing subscriber data to identify trends and insights, to give recommendation to the marketing for strategy marketing campaigns toward achieving the business task.

### 1.2 Key Stakeholders:
+ **Lily Moreno:** The director of marketing and your manager. Moreno is responsible for the development of campaigns
and initiatives to promote the bike-share program. These may include email, social media, and other channels.

+ **Cyclistic marketing analytics team:** A team of data analysts who are responsible for collecting, analyzing, and
reporting data that helps guide Cyclistic marketing strategy. You joined this team six months ago and have been busy
learning about Cyclistic’s mission and business goals — as well as how you, as a junior data analyst, can help Cyclistic
achieve them.

+ **Cyclistic executive team:** The notoriously detail-oriented executive team will decide whether to approve the
recommended marketing program.

### 1.3 Product:
**Cyclistic:** A bike-share program that features more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself
apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with
disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about
8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to
commute to work each day


# 2.0 Prepare

### 2.1 Information on data source and structure:  
+ Data is a public dataset which is made available online by [Motivate International Inc](https://artscience.blog/home/divvy-dataviz-case-study)

+ Data is divided into 4 quarters. The structure of the data is wide format 


### 2.2 Information about bias, credibility, licensing, privacy, security, and accessibility of data  
+ Motivate International Inc made the data available under this [License](https://ride.divvybikes.com/data-license-agreement), which adequately addresses the concerns about privacy, security and the right of access  

+ Dataset is a good sample size of about 3.8 million data points
 
### 2.3 Ensuring data integrity
+ Columns were compared, renamed, and reomoved where relevant for consistency across the entire dataset

+ The data type of the column date was converted to the numeric date data type

+ Because the 12 months data was divided into 4 quarters, the 4 datasets were combined during the data cleaning process 

+ The new data frame from the combined data was inspected by checking for list of column names, number of rows in data frame, the dimensions of the data frame, list of columns and data types (numeric, character, etc)
and a statistical summary of data. Mainly for numerics

### 2.4 Validity of dataset to answer business question
After cleaning data and combining the 4 datasets into one, a the user type was streamlined to two, members and casual instead of the initial 4. A new column that calculates the trip duration was also created to make it easy to compare patronage by the two user types


### 2.5 Problems with the data


# 3.0 Process 

### 3.1 Tools used for the project and why  

I used the R extension in visual studio code, because Excel, Sheets, R studio and BigQuery could not support the volume of data I uploaded: 
+ [Divvy_Trips_2019_Q2](https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2019_Q2.zip)
+ [Divvy_Trips_2019_Q3](https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2019_Q3.zip)
+ [Divvy_Trips_2019_Q4](https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2019_Q4.zip)
+ [Divvy_Trips_2020_Q1](https://divvy-tripdata.s3.amazonaws.com/Divvy_Trips_2020_Q1.zip)

In addtion, I used the R extention in visual studio code because I am currently using the free tier version R Studio and BigQuery, and these do have some limitations 

### 3.2 Have data integrity been ensured
Yes! Very much so. See section 2.3 Ensuring data integrity


# 4.0 Analyze 
### 4.1 Information about data format
Please refer to section 2.1 Information on data source and structure

### 4.2 What insights, trends and/or relationships were discovered
+ Average of all rides = 1479.139 Secs

+ Median of all rides = 712 Secs

+ Longest ride = 9387024 Secs

+ Shortest ride = 1 Sec


+ Average ride by member type

  Member type     |Ride_length	  |Unit   
  ----------------|---------------|------- 
  casual          |3552.7502	    |Secs   
  member          | 850.0662	    |Secs   


 + Median ride by member type

   Member type     |Ride_length	  |Unit   
   ----------------|--------------|-------
   casual          |1546		      |Secs   
   member          |589	      	  |Secs   

 + Maximum ride by member type

   Member type     |Ride_length	   |Unit  
   ----------------|---------------|------
   casual          |9387024	       |Secs  
   member          |9056634	       |Secs  

 + Minimum ride by member type

   Member type     |Ride_length	   |Unit  
   ----------------|---------------|------
   casual          |2		           |Secs  
   member          |1		           |Secs  


 + Average ride time by each day by member type

   Member type     |Day of week         |Ride length
   ----------------|--------------------|--------------
   casual          |Sunday              |3581.4054
   member          |Sunday              |919.9746
   casual          |Monday              |3372.2869
   member          |Monday              |842.5726
   casual          |Tuesday             |3596.3599
   member          |Tuesday             |826.1427
   casual          |Wednesday           |3718.6619
   member          |Wednesday           |823.9996
   casual          |Thursday            |3682.9847
   member          |Thursday            |823.9278
   casual          |Friday              |3773.8351
   member          |Friday              |824.5305
   casual          |Saturday            |3331.9138
   member          |Saturday            |968.9337

   

### 4.3 How will these insights help answer your business questions? 
The final analysis of the dataset compares the trip duration of the two subscribers, i.e. members and casual by day of the week. This data is useful for:
+ Finding which of the users traveled the longest trip

+ Which day of the week had the most trips

+ Which day of the week recorded the longest trip


# 5.0 Share
### 5.1 Were you able to answer the question of how annual members and casual riders use Cyclistic bikes differently?
Casual subscribers tend to be more active durinf the week compared to member subscribers

### 5.2 What story does your data tell?
Some key insights the data reveals include:
+ Casual subscribers account for **80.6%** of the all Divvy's bike-share program subscribers

+ Most active days for casual subscribers are **Fridays, Wednesdays, and Sundays** respectively

+ Most active days for member subscribers are weekends; **Sundays and Saturdays**

+ Maximum trip duration by casual subscribers is **3,774 minutes**

+ Minimum trip duration for casual subscribers is **3,372 minutes**

+ Maximum trip duration for member subscribers **969 minutes**

+ Minimum trip duration for member subscribers **824 minutes**

+ **Wednesday and Thursday** had the same trip duration 



### 5.3 How do your findings relate to your original question?
The study sought to identify how casual and member subscribers use Divvy's bike-share program differently. The findings showed that casual subscribers were more ative on week days whereas member subscribers were more active on weekends.

### 5.4 Who is your audience? What is the best way to communicate with them?
The Direcor of Marketing and the executive team. A powerpoint presentation and a dashboard would be an effective way to communicate with them.

### 5.5 Can data visualization help you share your findings?
Absolutely. The findings have been visualize using a bar chart and pie chart.
![Dashboard 2](https://github.com/Ed-Kwesi/bike_share/assets/140979188/98a9a869-02c2-41d3-aac6-e4bf9c1957c6)
This column chart was visualized in Tableau as part of the capstone project


![Dashboard 1](https://github.com/Ed-Kwesi/bike_share/assets/140979188/509e1295-4fbf-4707-acd1-71eb51c5e1e9)
This bar chart was visualized in Tableau as part of the capstone project

![Dashboard 3](https://github.com/Ed-Kwesi/bike_share/assets/140979188/441f9309-5985-4e95-a46f-e02aee1368df)
This pie chart was visualized in Tableau as part of the capstone project

### 5.6 Is your presentation accessible to your audience?
A dashboard has been visualized in Tableau as part of the capstone project. The dashboard is made accessible via this [Link](https://public.tableau.com/views/Bike-shareCasestudy/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link)

![Dashboard 4](https://github.com/Ed-Kwesi/bike_share/assets/140979188/8b4debb2-e961-49a2-ae38-29f848ce554c)
This is a screenshot of the link to the dashboard visualized in Tableau as part of the capstone project


# Reference
1) I drew inspiration from the outline of a colleague in the Google Data Analytics Certificate Program [https://github.com/jwilsh/Bellabeat_Case_Study/blob/main/README.md#10-ask](https://github.com/jwilsh/Bellabeat_Case_Study/blob/main/README.md#10-ask)

2) Data Licence Agreement [https://ride.divvybikes.com/data-license-agreement](https://ride.divvybikes.com/data-license-agreement)

3) Bolden text [https://www.markdownguide.org/basic-syntax/#:~:text=To%20bold%20text%2C%20add%20two,without%20spaces%20around%20the%20letters.&text=I%20just%20love%20**bold,bold%20text.](https://www.markdownguide.org/basic-syntax/#:~:text=To%20bold%20text%2C%20add%20two,without%20spaces%20around%20the%20letters.&text=I%20just%20love%20**bold,bold%20text.)

4) Lists [https://www.markdownguide.org/basic-syntax/#:~:text=To%20create%20an%20unordered%20list,to%20create%20a%20nested%20list.](https://www.markdownguide.org/basic-syntax/#:~:text=To%20create%20an%20unordered%20list,to%20create%20a%20nested%20list.)

5)  Dataset [https://divvy-tripdata.s3.amazonaws.com/index.html](https://divvy-tripdata.s3.amazonaws.com/index.html)

6) Tables [https://www.codecademy.com/resources/docs/markdown/tables](https://www.codecademy.com/resources/docs/markdown/tables)

7) Case study [https://artscience.blog/home/divvy-dataviz-case-study](https://artscience.blog/home/divvy-dataviz-case-study)

8) Images [https://stackoverflow.com/questions/41604263/how-do-i-display-local-image-in-markdown](https://stackoverflow.com/questions/41604263/how-do-i-display-local-image-in-markdown)

9) Pie chart [https://community.tableau.com/s/question/0D54T00000C62nfSAB/percentage-and-count-in-pie-charts](https://community.tableau.com/s/question/0D54T00000C62nfSAB/percentage-and-count-in-pie-charts)  
