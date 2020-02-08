# Kickstarter Analysis using Excel
<b>Background:</b><br>
Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.  Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. The Excel sheet's main information is a database of 4,000 past projects.<br>
<br>
<b>Objective 1: Modify the Main Information sheet to make patterns clearer</b><br>
A. To do this, I used conditional formatting to fill in each cell in the "state" column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.<br>
B. I, then, created a new column O called "Percent Funded" that uses a simple formula to uncover how much money a campaign made to reach its initial goal.<br>
C. Next, I used conditional formatting to fill each cell in the "Percent Funded" column using a three-color scale. The scale starts at 0 and is a dark shade of red, transitioning to green at 100, and blue at 200.<br>
![Kickstarter Table](https://github.com/swati-dontamsetti/Kickstarter-Analysis/blob/master/Images/FullTable.png)
D. Next, I created a new column P called "Average Donation" that uses a formula to uncover how much each backer for the project paid on average.<br>
E. Lastly, I created two new columns, one called "Category" at Q and another called "Sub-Category" at R, which use formulas to split the "Category and Sub-Category" column into two parts.<br>
<br>
<b>Objective 2: Create Pivot Tables to show different trends</b><br>
A. First, I created a new sheet with a pivot table that analyzes the information on the Main Information sheet to count how many campaigns were successful, failed, canceled, or are currently live per category.<br>
B. On that sheet I added a stacked colum pivot chart that can be filtered by country.<br>
C. Next, I created another new sheet with a pivot table that analyzes the information on the Main Information sheet to count how many campaigns were successful, failed, or canceled, or are currently live per sub-category.<br>
D. On that sheet I added a stacked column pivot chart that can be filtered by country and its parent category.<br>
<br>
<b>Objective 3: Convert the timestamps to a normal date</b><br>
A. I created two new columns on the Main Information sheet called "Date Created Conversion" and "Date Ended Conversion".<br>
B. The dates stored within the "Deadline" and "Launched_at" columns use Unix timestamps. Using an existing conversion formula, the "Date Created Conversion" now holds the conversion of the "launched_at" timestamps. And the "Date Ended Conversion" now holds the conversion of the "Deadline" timestamps.<br>
C. Next, I created a new sheet with a pivot table with a column of "State", rows of "Date Created Conversion". The values are based on the count of state, and it filters based on the parent "Category" and "Years".<br>
D. Lastly, I created a pivot chart line graph that visualizes this new table.<br>
<br>
<b>Objective 4: Create a Bonus Sheet that Counts the State of a Kickstarted by its Goal Range</b><br>
A. Create 8 columns called:
<br>&emsp;- "Goal"
<br>&emsp;- "Number Successful"
<br>&emsp;- "Number Failed"
<br>&emsp;- "Number Canceled"
<br>&emsp;- "Total Projects"
<br>&emsp;- "Percentage Successful"
<br>&emsp;- "Percentage Failed"
<br>&emsp;- "Percentage Canceled".<br>
B. In the "Goal" column, create 12 rows with the following headers:
<br>&emsp;- "Less than 1000"
<br>&emsp;- "1000 to 4999"
<br>&emsp;- "5000 to 9999"
<br>&emsp;- "10000 to 14999"
<br>&emsp;- "15000 to 19999"
<br>&emsp;- "20000 to 24999"
<br>&emsp;- "25000 to 29999"
<br>&emsp;- "30000 to 34999"
<br>&emsp;- "35000 to 39999"
<br>&emsp;- "40000 to 44999"
<br>&emsp;- "45000 to 49999"
<br>&emsp;- "Greater than or equal to 50000".<br>
C. Using the COUNTIFS() formula, I counted how many successful, failed, and canceled projects were created with goals within the ranges listed above. I populated the "Number Successful", "Number Failed", and "Number Canceled" columns with this data.<br>
D. Next, I added up each of the values in the "Number Successful", "Number Failed", and "Number Canceled" columns to populate the "Total Projects" column. Then, using a mathematical formula, I found the percentage of projects that were successful, failed, or canceled per goal range.<br>
E. Lastly, I created a line chart that graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.<br>
<br>
<b>Objective 5: Bonus Statistical Analysis</b><br>
A. I filtered the Main Information sheet by the "state" column. First I looked at the successful state and copied the "state" column and the "backers_count" column.<br>
B. I created a new sheet and pasted the above information.<br>
C. Next, I went back to the Main Information sheet and filtered for the failure state. I copied the "state" and "backers_count" columns to the same sheet.<br>
D. Next, I used Excel to evaluate the following for successful campaigns, and then for unsuccessful campaigns:
<br>&emsp;- The mean number of backers.
<br>&emsp;- The median number of backers.
<br>&emsp;- The minimum number of backers.
<br>&emsp;- The maximum number of backers.
<br>&emsp;- The variance of the number of backers.
<br>&emsp;- The standard deviation of the number of backers.
