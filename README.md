# Pewlett-Hackard-Analysis
## Purpose
The purpose of this analysis was to aid Pewlett Hackard in determing how many of their employees (from which department and level) are retiring in the near future.

## Results
In deliverable one an analysis was preformed to find who is likely to retire soon and their title, and then count the amount of future retirees by title. From this analysis we know:
* that very few managers (2) are expected to retire soon
* many Senior Enginners (25916) 
* many members of Senior Staff (24926) are expected to retire soon
* The results of the query that shows the results above is here [retiring_tiles](www.github.com/tori-taylor/Pewlett-Hackard-Analysis/edit/main/data/retiring_titles.csv)

In the second deliverable an analysis was preformed to determine how many employees are eligible for mentorship
* There are 1549 records in the mentorship_eligibility file, which has only unique employee ids and therefore there are 1549 employees who are eligibile

## Summary
Assuming all roles of retiring employees need to be filled, there would be 72,458 roles that would need to be filled. The additional query used to calcuate this is as follows:
  
  SELECT COUNT(emp_no)
  
  FROM retirement_titles
  
  WHERE to_date = '9999-01-01'
  
There are only 1549 mentorhip eligible employees to mentor for 72,458 roles this seems unrealstic, as that is a ratio of about 47 mentees to one mentor (47:1). In summary there are too many roles to fill and not enough mentees to support them. The query to find the number of mentorship eligible employees is 

SELECT COUNT (emp_no)

FROM mentorship_eligibility
  
