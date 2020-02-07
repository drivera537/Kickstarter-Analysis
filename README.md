# Kickstarter Analysis using Excel
Background: <br>
Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.  Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. The Excel sheet's main information is a database of 4,000 past projects.<br>
<br>
Objective 1: Modify the Main Information sheet to make patterns more clear<br>
A. To do this, I used conditional formatting to fill in each cell in the "state" column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.<br>
B. I, then, created a new column O called "Percent Funded" that uses a simple formula to uncover how much money a campaign made to reach its initial goal.<br>
C. Next, I used conditional formatting to fill each cell in the "Percent Funded" column using a three-color scale. The scale starts at 0 and is a dark shade of red, transitioning to green at 100, and blue at 200.<br>
D. Next, I created a new column P called "Average Donation" that uses a formula to uncover how much each backer for the project paid on average.<br>
E. Lastly, I created two new columns, one called "Category" at Q and another called "Sub-Category" at R, which use formulas to split the "Category and Sub-Category" column into two parts.<br>
<br>
Objective 2: Create Pivot Tables to show different trends<br>
A. First, I created a new sheet with a pivot table that analyzes the information on the Main Information sheet to count how many campaigns were successful, failed, canceled, or are currently live per category.<br>
B. On that sheet I added a stacked colum pivot chart that can be filtered by country.<br>
C. Next, I created a another new sheet with a pivot table that analyzes the information on the Main Information sheet to count how many campaigns were successful, failed, or canceled, or are currently live per sub-category.<br>
D. On that sheet I added a stacked column pivot chart that can be filtered by country and its parent category.<br>
<br>
Objective 3: Convert the timestamps to a normal date<br>
A. I created two new columns on the Main Information sheet called "Date Created Conversion" and "Date Ended Conversion".<br>
B. The dates stored within the "Deadline" and "Launched_at" columns use Unix timestamps. Using an existing conversion formula, the "Date Created Conversion" now holds the conversion of the "launched_at" timestamps. And the "Date Ended Conversion" now holds the conversion of the "Deadline" timestamps.<br>
C. Next, I created a new sheet with a pivot table with a column of "State", rows of "Date Created Conversion". The values are based on the count of state, and it filters based on the parent "Category" and "Years".<br>
D. Lastly, I created a pivot chart line graph that visualizes this new table.
