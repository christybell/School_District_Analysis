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

- How is the district summary affected?
- How is the school summary affected?
- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
- How does replacing the ninth-grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type
  
## Challenge Summary
Summarize four major changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
