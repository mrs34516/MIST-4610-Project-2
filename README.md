# MIST 4610 Fall 2024 Project 2

## Group 2 Team Members
- Aryan Patel [@AryanUGA](https://github.com/AryanUGA)
- Caleb Maine [@trynagetdone](https://github.com/trynagetdone)
- Campbell Durbin [@campbelldurbin](https://github.com/campbelldurbin)
- Chandler Boyd [@ChandlerBoyd7](https://github.com/ChandlerBoyd7)
- Maddie Sells [@mrs34516](https://github.com/mrs34516)

## Description of Dataset

The dataset we selected contains information on founded crime reported after July 1st, 2016 in Montgomery County of Maryland. The data is derived from the Montgomery County Police Department's database of founded crime and was obtained from the United States Government's open data site, https://catalog.data.gov/dataset. 

The dataset contains 421,538 rows and 30 columns of data, including temporal, spatial, and categorical data related to each reported crime incident. Included below is a comprehensive list of the dataset's 30 columns, including a description and data type for each column. The key columns we focused on are highlighed below and are as follows: Incident ID, Dispatch Date / Time, Start_Date_Time, Crime Name2, Police District Name, Agency, and Beat.

![image](https://github.com/user-attachments/assets/bfda1e55-b00a-49f5-beb9-214dfe28cbd0)

## Question 1
Which police districts experience the highest levels of crime, and what are the most prevalent crime types within those districts? Furthermore, at what times are these crimes most frequently committed, categorized by crime type? 

Exploring the question(s) above has social, economic, policy, and strategic importance. Identifying the police districts that experience the most crime and understanding details about these crimes, specifically those related to type and timing, aids in efforts to improve public safety by empowering local government officials and law enforcement to prioritize resource allocation, like personnel placement, and the development of safety measures, like lighting and security cameras, in high-crime areas. This understanding and the afforemetioned efforts also support economic development as efficient policing helps mitigate the cost of crime, including property loss and medical expenses, and reduce expenditures for local government, police agencies, and the criminal justice system as a whole. Further, high-crime areas often correlate with systematic inequalities, so by revealing those police districts with the most crime, other related issues like poverty, education, and infrastructure may be exposed and can begin to be further explored and addressed.

## Question 1 Analysis & Results

Visualization #1: Crime Count by District
![Screenshot (322)](https://github.com/user-attachments/assets/f7643170-0684-4e6b-96a5-24d2f6b269d2)
We began answering Question 1 by first identifying which police districts experience the most crime. To do this, we displayed the count of Incident ID by Police District Name and sorted the resulting bars in descending order from left to right. This revealed Silver Spring, Wheaton, and Montgomery Village to be the three districts with the most crime.

Visualization #2: Crime Type Count by District
![Screenshot (323)](https://github.com/user-attachments/assets/7ae15b66-ecf1-481b-b713-a9686d5f6753)
Next, we further analyzed crime in these three districts by categorizing incidents by crime type. As shown above, although not in the same order for each district, Simple Assualt, Theft From Motor Vehicle, and Drug/Narcotinc Violations were within the top four crime types for each district. It is important to note, however, that we did filter to exclude the "All Other Offenses" crime type for each district as this category had the highest incident count for each category but did not provide relevant insight.

Visualization #3: Start Time vs. Dispatch Time
![Screenshot (327)](https://github.com/user-attachments/assets/eb58acbf-bafc-46a2-9a49-dca4baccc88b)
The dataset includes both start date/time as well as dispatch date/time. The start date/time refers to the date and time the actual crime began while dispatch date/time refers to the date and time police were sent to the scene. We explored the relationship between start date/time and crime type as well as dispatch date/time and crime type. Again, we explored this relationship only for the top three crime districts. The start date/time graph reveals that the occurence of all three crime types of focus (Simple Assault, Theft From Motor Vehicle, and Drug/Narcotic Violations) rises throughout the day with incidents occuring most frequently in the late hours of the day. 

While start date/time and dispatch date/time are closely correlated for Simple Assault and Drug/Narcotic Violations, there is significant variation between start time/date and dispatch date/time for Theft From Motor Vehicle. This is likely the result of a combination of two conditions. First, as shown in the start date/time visualization, Theft From Motor Vehicle incidents generally occur during the late hours when it's dark and cars are unoccupied and unattended to throughout the night. Owners generally return to their vehicles between 7:00 - 9:00 in the morning to depart for work, school, or other responsibilities, which would also be the time they notice their vehicle has been broken into and would thus explain the peak in dispatch time for Theft From Motor Vehicle incidents during these hours. The variation in start time and dispatch time for Theft From Motor Vehicles can likely also be explained by the fact that car theft is a relatively low priority crime. While car theft may be reported at or near the late hours, police units must prioritize responsing to higher priortiy crimes, including Simple Assault and Drug/Narcotic Violations, that also peak during the same hours. Thus, police units are then instead dispatched to car theft crime scenes during periods with less crime, explaining the rise in dispatch time for the Theft From Motor Vehicle crime type from 7:00 - 9:00 AM. 

## Question 2
Within each police agency, which beats are the most efficient responders? In other words, which beats have the quickest average response time? Additionally, which agencies have the highest percentage of high-performing beats?

For clarification purposes, a beat refers to a specific geographic area assigned to a police officer or a group of officers. Beats are housed under police agencies.

This question holds significant social, economic, cultural and operational importance. This question is socially significant because efficient response time is crucial in ensuring public safety. Responding to crime incidents quickly can prevent the escalation of emergencies, save lives, reduce harm, and build trust between law enforcement and citizens. While examining response time in general is beneficial, knowing the specific beats with the fastest responses times allows for higher-level analysis and decision-making. By identifying the beats with the shortest average response times, police agencies are better able to evaluate and make personnel assignments, as deploying the most efficient officers in high-crime areas would maximize resource utililzation and policing effectiveness. Similar to Question 1, this question is also economically important because strategic beat assignments helps improve cost-effectiveness and reduce losses from crime. 

By closely analyzing high-performing beats, police agencies and the local government can also determine which factors outside of merely personnel promote fast response times. For example, beats with slower average response times may be hindered by factors such as traffic congestion, poor lighting, or construction zones. By examining the beats with the shortest average response times, agencies and policymakers can attempt to identify and mimick conditions that empower police units to respond as quick as possible. 

This analysis can also identify which agencies have the most high performing beats by calculating the percentage of total beats within an agency that can be classified as "high-performing." This knowledge can support the local government's policy agency funding initiatives and decisions and, similarily to the previous paragraph, agencies and government representatives can evaluate high-performing agencies to institute similar practicies within low-performing agencies to work to work to achieve the discussed social, economical, cultural, and operational benefits discussed. 

## Question 2 Analysis & Results

Calculated Field
![Screenshot (328)](https://github.com/user-attachments/assets/293ea239-f1e4-4acd-a529-00c6b310cd9b)
Before creating our visualization, we first needed to create a calculated field for Response Time. As discussed during Question 1, the dataset include both Start Date/Time and Dispatch Date/Time. Thus, Response Time was calculated by using the DATEDIFF function, which found the difference between the Start Date/Time and Dispatch Date/Time in minutes as shown above.

Visualization: Average Response Time by Beat
![Screenshot (326)](https://github.com/user-attachments/assets/bd0a8e63-f75b-461c-a264-6e7f3cbed97f)
![Screenshot (331)](https://github.com/user-attachments/assets/0bfa8b6a-f937-4ef5-a999-25ee9e21a2ba)
![Screenshot (332)](https://github.com/user-attachments/assets/6ddf1fb1-6968-4ab0-a988-627da65ae241)

To answer Question 2, we examined the average response time for the highest-performing beats within each agency. To focus the analysis on beats with the fastest average response times, we filtered the average response time to only include those beats who had an average response time between 0 and 1,440 minutes (24 hours). Visually, it is evident that MCFM's beats have the lowest average response times, but we also calculated the percentage of beats that could be classified as high-performing by dividing the number of beats with an average response time between 0 - 1,440 by the total number of beats per agency and found the top performing agencies to be as follow:
- MCFM: 68.2% (30/44)
- TPPD: 52.6% (10/19)
- MCSO: 47.1% (8/17)
- GPD: 45.2% (19/42)
- RCPD: 24.2% (8/33)
- MCPD: 15.5% (9/58)

## Manipulations
We did not make any manipulations to the raw data source, but we did remove null values and outliers throughout our analyses. When using the Police District Name, Crime Name2, Start Date/Time, Disptach Date/Time, Agency, and Beat columns, we always removed null values. As discussed throughout our anaylses, we also regularly applied filters and created a calculated field (Response Time).

## Tableau Packaged Workbook
The Tableau Packaged Workbook containing the visualizations throughout this file is included in this repository. Our Powerpoint Presentation is also included in this repository.


