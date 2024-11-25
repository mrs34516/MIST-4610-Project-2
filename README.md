# MIST 4610 Fall 2024 Project 2

## Group 2 Team Members
- Aryan Patel [@AryanUGA](https://github.com/AryanUGA)
- Caleb Maine [@trynagetdone](https://github.com/trynagetdone)
- Campbell Durbin [@campbelldurbin](https://github.com/campbelldurbin)
- Chandler Boyd [@ChandlerBoyd7](https://github.com/ChandlerBoyd7)
- Maddie Sells [@mrs34516](https://github.com/mrs34516)

## Description of Dataset

The dataset we selected contains information on founded crime reported after July 1st, 2016 in Montgomery County of Maryland. The data is derived from the Montgomery County Police Department's database of founded crime and was obtained from the United States Government's open data site, https://catalog.data.gov/dataset. 

The dataset contains 421,538 rows and 30 columns of data, including temporal, spatial, and categorical data related to each reported crime incident. Included below is a compehensive list of the dataset's 30 columns, including a description and data type for each column. The key columns we focused on are highlighed below and are as follows: Incident ID, Dispatch Date / Time, Start_Date_Time, Crime Name2, Police District Name, Agency, and Beat.

Insert Table

## Question 1
Which police districts experience the highest levels of crime, and what are the most prevalent crime types within those districts? Furthermore, at what times are these crimes most frequently committed, categorized by crime type? 

Identifying the police districts that experience the most crime, the most prevalent types of crime in those districts, and the times at which these crimes occur and require police dispatch allows authorities to effectively evaluate and deploy resources, including personnel and preventative measures like lighting and security cameras.

Silver Spring, Wheaton, and Montgomery Village are the top three districts with the highest levels of crime within our data set and the most prevalent crimes within them are Simple Assault, Theft From Motor Vehicle, Drug/Narcotic Violation. These crimes are reported in the later parts of the day and peak from 6pm to 8pm. Crimes are less frequently reported in the mornings and begin to rise after 5am.This period in the early part of the day is also when dispatch sends out units to the scene as well.

## Question 1 Analysis & Results

Visualization #1: Crime Count by District
![Screenshot (322)](https://github.com/user-attachments/assets/f7643170-0684-4e6b-96a5-24d2f6b269d2)
Writing

Visualization #2: Crime Type Count by District
![Screenshot (323)](https://github.com/user-attachments/assets/7ae15b66-ecf1-481b-b713-a9686d5f6753)
Writing

Visualization #3: Start Time vs. Dispatch Time
![Screenshot (327)](https://github.com/user-attachments/assets/eb58acbf-bafc-46a2-9a49-dca4baccc88b)
Writing

## Question 2
Within each police agency, which beats are the most efficient responders? In other words, which beats have the quickest average response time?

This question holds significant social, economic, cultural and operational importance. This question is socially significant because police response time is crucial for public safety. We can use this question to analyze which areas have the fastest response time and which areas need improvement. Identifying the beats with the shortest average response times is valuable for evaluating beat assignments, as deploying the most efficient beats in high-crime areas would maximize effectiveness.This question is economically important because slower response times can lead to higher costs due to prolonged investigations. Using this analysis, we can determine which beats are the most efficient, why they are most efficient and how we can reduce response time in slower performing beats. Analyzing average response times can uncover operational efficiencies and shed light on external factors influencing response times, such as traffic congestion or staffing challenges.This is culturally important because communities rely on law enforcement's prompt arrival. With our formulated question, we can use the data on incident response times to optimize process efficiency to promote public safety.

## Question 2 Analysis & Results

Calculated Field
![Screenshot (328)](https://github.com/user-attachments/assets/293ea239-f1e4-4acd-a529-00c6b310cd9b)
Writing

Visualization: Average Response Time by Beat
![Screenshot (326)](https://github.com/user-attachments/assets/bd0a8e63-f75b-461c-a264-6e7f3cbed97f)
Writing



