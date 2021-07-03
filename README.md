# School District Analysis

# Overview
The school board has noticed evidence of academic dishonesty in the reading and math scores for Thomas High School ninth graders. They believe the grades to have been altered. We are replacing the Thomas High School 9th grade math and reading scores with "NaN" values and repeating our analysis to report the changes of how this affects our school district analysis summaries.

## Process:

Deliverable 1: We found and replaced the Thomas High School ninth-grade reading and math scores with "NaN" values before running the school district analysis

Deliverable 2: We repeated the school district analysis using our new DataFrame and updated the following summaries: 

1. The district summary 
2. The school summary 
3. The top 5 performing schools, based on the overall passing rate
4. The bottom and 5 performing schools, based on the overall passing rate
5. The average math score for each grade level from each school
6. The average reading score for each grade level from each school
7. The scores by school spending per student, by school size, and by school type

## Resources
Data Sources: [schools_complete.csv](https://github.com/corispade/School_District_Analysis/blob/main/Resources/schools_complete.csv), [students_complete.csv](https://github.com/corispade/School_District_Analysis/blob/main/Resources/students_complete.csv)

Software: Python 3.7.6, Conda 4.10.1

Environment: Jupyter Notebook

# Results: 
Find the completed School District Analysis [here](https://github.com/corispade/School_District_Analysis/blob/main/PyCitySchools_Challenge.ipynb) for reference.

After replacing Thomas High School 9th grade math and reading scores with "NaN" values, we found the following results: 

### District Summary: 
* The District Summary was marginally affected: 
  * The average math score reduced by 0.2. 
  * The average reading score did not change
  * The % Passing Math reduced by 0.2%
  * The % Passing Reading reduced by 0.1%
  * The % Overall Passing Reduced by 0.3%

Original District Summary:

![original](https://github.com/corispade/School_District_Analysis/blob/main/Resources/original/district_summary.png)

New District Summary with Changes:

![new](https://github.com/corispade/School_District_Analysis/blob/main/Resources/Thomas/thomas_district_summary.png)

### School Summary: 
* The school district summary for Thomas High School when replacing the 9th grade math and reading scores with NaN was greatly affected. This reduction was caused because we are still calculating the grades based on total student count. Since the 9th grade count has been reduced, the passing percentages were reduced accordingly. This created inaccurate results:
  * The average math score reduced by 0.06. 
  * The average reading score increased by 0.05.
  * The % Passing Math reduced by 26.36%
  * The % Passing Reading reduced by 27.64%
  * The % Overall Passing Reduced by 25.87%

![wrong](https://github.com/corispade/School_District_Analysis/blob/main/Resources/Thomas/thomas_school_summary_wrong.png)

* After correcting the DataFrame by updating the Thomas High School count to account for 10th, 11th and 12th graders only, the school summary for Thomas High School was only marginally affected:
  * The average math score reduced by 0.06. 
  * The average reading score increased by 0.05.
  * The % Passing Math reduced by 0.09%
  * The % Passing Reading reduced by 0.29%
  * The % Overall Passing reduced by 0.31%

Corrected School Summary DataFrame for reference:

![right](https://github.com/corispade/School_District_Analysis/blob/main/Resources/Thomas/thomas_school_summary.png)

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
* When replacing the 9th grade math and reading scores with NaN (while still accounting for the original total student count), Thomas High School drops out of the top 5 school ranking. Surprisingly, they still rank higher than the bottom 5 schools.

* When replacing the 9th grade math and reading scores with Nan (updating the count for 10th, 11th and 12th graders only), Thomas High School remained in the top 5 performing schools based on the overall passing percentage. Their #2 ranking did not change. 

Original Top 5 Performing Schools:

![original](https://github.com/corispade/School_District_Analysis/blob/main/Resources/original/top_5.png)

New Top 5 Performing Schools:

![new](https://github.com/corispade/School_District_Analysis/blob/main/Resources/Thomas/thomas_top_5.png)

### How does replacing the ninth-grade scores affect the following:

* Math and reading scores by grade:
  * 

* Scores by school spending:
  * 

* Scores by school size:
  * 

* Scores by school type:
  * 

# Summary: 
Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

It is difficult to come to a conclusion about academic dishonesty for Thomas High School 9th grade math and reading scores based on this analysis. When omitting the 9th grade scores, Thomas High School % passing math, % passing reading and % overall passing were reduced by <1%. This is not a large enough margin to 