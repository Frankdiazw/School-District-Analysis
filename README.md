# School District Analysis :school:

## Overview of the school district analysis :100::mag:
In this analysis, the main goal is to standardize all test data for analysis, reporting, and presentation to provide insight into performance patterns and trends. All of this to guide the school board in adjusting school budgets. During the analysis it will be possible to observe data frames with the student's name, math and reading scores, along with the allocated budget; all this calculated with the pandas library and NumPy library to guarantee a better analysis towards the school board.
However, for this challenge, it is believed that there was academic dishonesty in the "students_complete.csv" file by Thomas High School in the ninth grade. To verify this, the results for Reading and Math will be changed to "NaN" and the analysis will be performed again to analyze the impact of the "corrupted" scores.

## Results :books:
For this analysis, the student had to carry out the previous work called "PyCity Schools" to begin to carry out the challenge of this module.

### Deliverable 1: Replacing 9th Grade Math and Reading Scores: :notebook:
- For this deliverable, the Pandas loc method with conditional statements and logical and comparison operators was used, 9th grade reading and math scores were selected for Thomas High School. The Pandas NumPy module was then used to change the reading and math scores to NaN. The outcomes are as follows:

![](https://github.com/Frankdiazw/School-District-Analysis/blob/main/Resources/Deliverable%201.png)

- Figure 1. DataFrame with reading and math scores of ninth graders in Thomas High school replaced with NaNs. 

### Deliverable 2: Repeat the School District Analysis :clipboard:
- Now for this deliverable, the district summary was updated first. For this, the total student count was recalculated by subtracting the number of ninth grade students at Thomas High School from the total student count, then the math and reading passing rates were recalculated, and the overall passing rate. with the total student count recalculated. The updated DataFrame resulted as follows:

![](https://github.com/Frankdiazw/School-District-Analysis/blob/main/Resources/Deliverable%202.1.png)

- Figure 2. Updated DataFrame with the recalculated data.

  - By altering the total student count, it was observed that the math and reading pass rates increased by a few tenths and the overall pass rate increased by almost 1%.

- Next, the code for this module was run that creates and formats the School Summary Data Frame, and then the School Summary was updated with Thomas High School students in grades 10-12 as follows: 
  - First, the number of 10-12 grade students was calculated in Thomas High School with this code: 
    - TSH_grade_count = student_data_df.loc [(student_data_df ["grade"] == "9th") & (student_data_df ["school_name"] == "Thomas High School")] ["student_name"]. Count ()

- After that, the school summary was updated using Thomas High School's 10-12 grade students as follows: First, the number of 10-12 grade students was calculated in Thomas High School with this code: TSH_grade_count = student_data_df.loc [(student_data_df ["grade"] == "9th") & (student_data_df ["school_name"] == "Thomas High School")] ["student_name"]. Count ()

- Then, three new DataFrames were created for Thomas High School students in grades 10-12: students who passed math, students who passed reading, and students who passed both math and reading. Using these DataFrames, the percentage of students who passed math, reading, and math only at Thomas High School was recalculated. In the code, three logical operator conditional statements were used so that only students in grades 10-12 would pass math, pass reading, and pass math and reading at Thomas High School. Then, the percentage of students who passed math, reading, and reading and passed both math and reading for Thomas High School was calculated. And finally, the % Passing Math, % Passing Reading, and % Overall Passing scores were replaced in the School Summary DataFrame for Thomas High School. The code and the DataFrame are shown below:
  - Code for creating the updated DataFrame for Thomas High School
    - district_summary_df = pd.DataFrame(
          [{"Total Schools": school_count, 
          "Total Students": student_count, 
          "Total Budget": total_budget,
          "Average Math Score": average_math_score, 
          "Average Reading Score": average_reading_score,
          "% Passing Math": passing_math_percentage,
         "% Passing Reading": passing_reading_percentage,
        "% Overall Passing": overall_passing_percentage}])
        
![](https://github.com/Frankdiazw/School-District-Analysis/blob/main/Resources/Deliverable%202.2.png)

- Figure 3. Updated DataFrame for Thomas High School.

- The summary of the affected school. Changes can be observed when comparing the data frame metric from the previous school summary to the data frame metric from the subsequent school summary. After Thomas High School ninth graders were excluded and only calculating 10-12 grade students who passed math, reading at Thomas High School. Passing% math, reading, and passing grades overall increased.

- By replacing the math and reading scores of ninth grade students, Thomas Middle School's performance relative to the other schools was affected. This is because at the time of replacing the grades with "NaN", the number has become smaller, increasing the percentage of passing mathematics and the percentage of passing reading and overall.

- Replacing ninth grade scores affects the following: 
- **Math and reading scores by grade**, when math and reading scores by grade were calculated, all grades got results, but after replacing ninth grade with NaN, they got (math and reading scores) for the ninth grade equal NaN, but all other grades had the same result.
- **School Spending Scores**: Replacing ninth grade scores did not affect school spending scores.
- **School size**. Due to the change in Thomas High School's 9th grade scores for "NaN". The overall percentage of grades for middle schools decreased. Small and large school scores remained the same.
- **Scores by type school type**, Replacing the ninth grade scores affected the scores as in the type of school, the ninth grade scores from Thomas High School were replaced, since Thomas High School is autonomous, the percentage overall decreased. However, the district-type school had no effect.

## Summary :dart:
Changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs are presented below:

- Changes to the updated school district analysis after the ninth grade reading and math scores at Thomas Middle School have been superseded by NaN.

- By replacing the grades of Thomas High School ninth graders with "NaN," the number of passing math students changed.

- Due to the change in the number of students passing math, the percentage of students passing math at Thomas High School also changed.

- Likewise, by replacing the grades of Thomas High School's ninth graders with "NaN," the number of approved reading students changed. Due to the change in the number of passing students in reading, the percentage of passing students in math at Thomas High School also changed.

- When math and reading scores were calculated by grade. All grades had results, but after replacing the 9th grade with NaN for Thomas High School, the math and reading scores for the 9th grade were determined to be equal to "NaN", but all other grades had the same result as the previous analysis.

- When the passing percentage in math and reading was calculated, the percentage was affected due to the change in grades of the ninth graders by "NaN."

