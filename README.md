# Pandas Challenge
![iStock-1316170198-1024x488](https://github.com/cbake105/Pandas_School_Budget/assets/133677209/438e7e09-dc6a-4637-93a6-6b62835c233d)

## Instructions
Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

## District Summary
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:
- Total number of unique schools
- Total students
- Total budget
- Average math score
- Average reading score
- % Passing math (the percentage of students who passed math)
- % Passing reading (the percentage of students who passed reading)
- % Overall passing (the percentage of students who passed math AND reading)

## School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:
- School name
- School type
- Total students
- Total school budget
- Per student budget
- Average math score
- Average reading score
- % Passing math (the percentage of students who passed math)
- % Passing reading (the percentage of students who passed reading)
- % Overall passing (the percentage of students who passed math AND reading)

## Highest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in descending order and display the top 5 rows.

Save the results in a DataFrame called "top_schools".

## Lowest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in ascending order and display the top 5 rows.

Save the results in a DataFrame called "bottom_schools".

## Math Scores by Grade
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

## Reading Scores by Grade
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

## Scores by School Spending
Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.

spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
Use pd.cut to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()

Use the scores above to create a DataFrame called spending_summary.
Include the following metrics in the table:
- Average math score
- Average reading score
- % Passing math (the percentage of students who passed math)
- % Passing reading (the percentage of students who passed reading)
- % Overall passing (the percentage of students who passed math AND reading)

## Scores by School Size
Use the following code to bin the per_school_summary.

size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

## Scores by School Type
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.

This new DataFrame should show school performance based on the "School Type".




# Written Report

Summary: 
The dataset has 15 total schools, 2 types of schools (charter/district), 39,170 total students, a total budget of $24,649,428 , an average math score of 78.99, an average reading score of 81.88, passing math at 74.98%, passing reading at 85.81%, and overall passing at 65.17%.  

Observable Trends:

Scores by school spending - the spending ranges (per student) at <$585 produced higher average scores and percentage passing than the spending ranges (per student) at $585-630, $630-645, $645-680. 

Scores by school size - the school size large (2000-5000) produced the lowest averages and passing percentages. School sizes small (<1000) and medium (1000-2000) produced similar averages and passing percentages.

Scores by school type - Charter schools produced higher averages and passing percentages than District schools.


# Cite
AskBCS Learning Assistant

Richie 
https://smuvirtdatapt-yzn4480.slack.com/archives/D05CPK7DC9H/p1690553492411389

Ryan Ellison 
https://smuvirtdatapt-yzn4480.slack.com/archives/D05CPK7DC9H/p1690485212307359

Class Office hours
