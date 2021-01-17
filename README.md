# School District Analysis

## Project Overview
As the chief data scientist for the Austin Independent School District, I have been tasked to prepare all standardized test data for analysis, reporting, and presentation to provide insights about performance trends and patterns. These insights will be used to inform discussions and strategic decisions at the school and district level. Here is the list of deliverables for the school district analysis: 

- A high-level snapshot of the district's key metrics, presented in a table format
- An overview of the key metrics for each school, presented in a table format
- Tables presenting each of the following metrics:
  - Top 5 and bottom 5 performing schools, based on the overall passing rate
  - The average math score received by students in each grade level at each school
  - The average reading score received by students in each grade level at each school
  - School performance based on the budget per student
  - School performance based on the school size 
  - School performance based on the type of school

## Resources
- **Data Sources**: schools_complete.csv, students_complete.csv
- **Software**: Python 3.7.6, Anaconda 4.9.2, Git Bash 2.29.2
- **Tools**: Jupyter Notebook, Pandas 

## Summary


## Challenge Overview
The school board notified me that the `students_complete.csv` file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to me for help. Therefore, I have replaced the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. After I replaced the math and reading scores, I repeated the school district analysis.

## Challenge Deliverables
### Deliverable 1: Replace ninth-grade reading and math scores

I used the Pandas `loc` method with conditional statements and comparison and logical operators to select the 9th grade reading and math scores for Thomas High School. Then, I used the Pandas `NumPy` module to change the reading and math scores to NaN.

<img src="images/Deliverable 1 code.PNG">

I confirmed that the DataFrame looks like the image below, where the ninth-grade reading and math scores from Thomas High School have been replaced with NaNs. 

<img src="images/Deliverable 1 confirmation.PNG">

### Deliverable 2: Repeat the school district analysis

After replacing the test scores for 9th graders at Thomas High School with NaNs, I repeated the school district analysis I previously did to exclude Thomas High School 9th grade test scores. I recreated the following metrics:

- **The district summary**

  I recalculated the total student count by subtracting the number of ninth-grade students in Thomas High School from the total student count, then recalculated the passing math and passing reading percentages, and the overall passing percentage with the recalculated total student count.

  <img src="images/Deliverable 2_district summary.PNG">

  Then, I recreated the District Summary DataFrame and confirmed it displayed correctly.

  <img src="images/Deliverable 2_district summary confirmation.PNG">

- **The school summary**

  I used the initial code from this assignment to create and format the School Summary DataFrame, then updated the school summary using the 10th-12th graders from Thomas High School as follows:

  - First, I calculated the number of 10th-12th graders in Thomas High School.

    <img src="images/Deliverable 2_school summary_THS count.PNG">

  - Then, I created three new DataFrames for the 10th-12th graders from Thomas High School: students who passed math, students who passed reading, and students who passed both math and reading.

    <img src="images/Deliverable 2_school summary_THS passing DataFrames.PNG">

  - Using these DataFrames, I recalculated the percentage of students who passed math, passed reading, and passed both math and reading for Thomas High School only.

    <img src="images/Deliverable 2_school summary_THS passing percentages.PNG">

  - Next, I replaced the % Passing Math, % Passing Reading, and % Overall Passing scores in the current School Summary DataFrame with the new passing percentages for Thomas High School.

    <img src="images/Deliverable 2_school summary_THS replaced passing percentages.PNG">
  
  - Finally, I confirmed the new School Summary DataFrame displayed correctly.

    <img src="images/Deliverable 2_school summary confirmation.PNG">

- **The top 5 and bottom 5 performing schools, based on the overall passing rate**

  I reused my initial code to recalculate these metrics:

  <img src="images/Deliverable 2_top 5 and bottom 5.PNG">

- **The average math score for each grade level from each school**

  I reused my initial code to recalculate and format these metrics:

  <img src="images/Deliverable 2_avg math scores.PNG">

- **The average reading score for each grade level from each school**

  I reused my initial code to recalculate and format these metrics:

  <img src="images/Deliverable 2_avg reading scores.PNG">

- **The scores by school spending per student, by school size, and by school type**

  I reused my initial code to recalculate and format the following metrics:

  - Scores by School Spending
  
    <img src="images/Deliverable 2_scores by school spending.PNG">
  
  - Scores by School Size
  
    <img src="images/Deliverable 2_scores by school size.PNG">
  
  - Scores by School Type
  
    <img src="images/Deliverable 2_scores by school type.PNG">


## Challenge Results

- The district summary was slightly affected after replacing the test scores for 9th graders at Thomas High School with NaNs. The average math score decreased from 79.0 to 78.9 while the average reading score remained unchanged. The percentage of students passing math decreased from 75.0% to 74.8%, the percentage of students passing reading decreased from 85.8% to 85.7%, and the overall percentage of students passing decreased from 65.2% to 64.9%.

- After replacing the test scores for 9th graders at Thomas High School with NaNs, the school summary saw slight changes solely for Thomas High School metrics:
  - average math score decreased from 83.42 to 83.35<sup>1</sup>
  - average reading score increased from 83.85 to 83.9<sup>1</sup>
  - percentage passing math decreased from 93.27% to 93.19%<sup>1</sup>
  - percentage passing reading decreased from 97.31% to 97.02%<sup>1</sup>
  - percentage overall passing decreased from 90.95% to 90.63%<sup>1</sup> 
  
  <sup>1</sup> all amounts above are rounded to the nearest hundredths

- Replacing the 9th graders' math and reading scores did not affect Thomas High School's performance relative to other schools. They retained their #2 rank of top performing schools.

- Replacing the ninth-grade scores affected the following:

  - Math and reading scores by grade
  
    Thomas High School now displays an 'nan' in the 9th grade column, which makes sense since we replaced all 9th graders' scores with NaNs.
  
  - There were no changes to the Scores by school spending, Scores by school size, or Scores by school type
  
## Challenge Summary
In Summary, four major changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs were:
1. The district summary showed changes, with the most dramatic impact to the overall percentage of students passing, which decreased 0.3%.
2. The school summary showed changes for Thomas High School metrics, with the most dramatic impact to the overall percentage of students passing, which decreased by 0.32%.
3. Even though Thomas High School's metrics changed, their metrics did not change dramatically enough to see their performance ranking change compared to other schools. They continue to be the #2 top performing school in the district.
4. The math and reading scores by grade tables now show 'nan's for 9th graders at Thomas High School.


