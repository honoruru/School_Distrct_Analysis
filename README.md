# School District Analysis
## Project Overview

After evidence of academic dishonesty in reading and math grades for Thomas High School (Thomas) ninth graders, a request was made to disregard the math and reading scores for Thomas while keeping the rest of the data intact.  This was accomplished by replacing the Thomas scores with NaNs.  The school district analysis was then repeated using the cleansed data.

## Results

To summarize the impact of the replacement of Thomas scores with Nans:

*The district summary was minimally affected*  
The District’s Overall Passing Percentage decreased by 0.317 percentile points to 64.856%.

*The school summary was minimally affected*  
Only the scores of Thomas were revised. The impact would be to Thomas’ ranking among other district schools as detailed below. 

*Thomas’ performance relative to the other schools*  
Thomas’ ranking among all 15 schools was affected as follows:  
  - Average math:		  4th to 6th  
  - Average reading:	Remains 5th  
  - Passing math:		  Remains 7th  
  - Passing reading:  1st to 3rd  
  - Overall:  		    Remains 2nd  

•	
•	Replacing the ninth-grade scores had the following impact:
o	Math and reading scores by grade
	Thomas was ranked 3rd but moves to last as there is no math score
	All schools previously ranked below Thomas move up one rank as Thomas moves from 3rd to 15th.

	Thomas was ranked 5th but moves to last as there is no reading score
	All schools previously ranked below Thomas move up one rank as Thomas moves from 5th to 15th.

	There is no impact on the scores of 10th, 11th, and 12th graders.

o	Scores by school spending
o	For the four schools in the same spending range of $630-$644 (per student) as Thomas, there was no change. When ranked by % Overall Passing, Thomas was and remains in 1st place for all test score categories. 

o	Scores by school size
o	For the five schools in the same **Medium Size** category as Thomas, the relative changes follow when ranked by % Overall Passing:
Medium schools
Average math:  	    2nd to 4th
Average reading:  	Remains 3rd
Passing math:  	    Remains 5th
Passing reading:  	1st to 3rd
Overall:  Remains 	2nd 
•	
o	Scores by school type
o	For the eight charter schools of with Thomas is one, the relative changes follow when ranked by % Overall Passing:
•	Average math:  	    4th to 6th 
•	Average reading:  	Remains 5th 
•	Passing math:  	    Remains 7th 
•	Passing reading:  	1st to 3rd 
•	Overall:  		      Remains 2nd 

## Summary


In summary, four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

1.	The math and reading scores of Thomas 9th graders in student_data_df was replaced with NaN.  This effectively removed their data from the numerator used in calculating math, reading and overall test percentages in the school district analysis.

2.	The count of Thomas 9th graders was subtracted from the total student count in school_data_complete_df. This reduced the denominator used in calculating math, reading and overall test percentages in the school district analysis.  It should be noted that the total student count in school_data_complete_df was not changed.

The combined effect of 1. and 2. is that the Thomas 9th graders’ scores are not considered in the calculation of math, reading, and passing percentages.  In effect, the Thomas 9th graders were not students in the district for grading purposes.

3.	Thomas’ % Passing scores were recalculated based on those of 10th, 11th, and 12th graders.  This was done by reducing the number of Thomas students by the number of 9th graders.  Ninth grader scores were already effectively removed from the data by their replacement with NaN.  The % Passing scores were then inserted into the per_school_summary_df, replacing the values which included the suspect 9th grader calculations. 

The presentation of this statistic is deserving of at least a footnote that the determination and inclusion of actual 9th grade scores is pending the outcome of the district’s investigation.  

4.	The cumulative effect of the above changed Thomas’ rankings among the other schools in the district:

-	Thomas is no longer ranked in the 9th grade math and reading scores as there are no 9th grader scores.

-	Thomas’ overall ranking (based on 10th, 11th, and 12th grader scores were impacted in some, but not all, cases.  Most notably, Thomas’ rank as 2nd in the district based on % Overall Passing was unchanged.  Where there was little or no effect on Thomas’ rankings, one would conclude that the suspect 9th grader scores were followed a distribution similar to the remaining student body.  
