# Analysis of Kickstarter Data

## Overview of Project 
This Kickstarter_Challenge document offers an analysis on different media fundraising goals based on the outcome for a hypothetical client.  The Kickstarter_Challenege excel sheet has two additional sheets named “Theater Outcomes by Launch Date” and “Outcomes Based on Goals,” that the data-1-1-3-StarterBook sheet does not have.  The goal of this analysis was to see how different campaigns fared in relation to their launch dates and their funding goals.

##Analysis and Challenges   

###Theater Outcomes by Launch Date
“Theater Outcomes by Launch Date” is a pivot table that filters by major category and years to output a table that gives the number of successful, failed, and canceled media per month for all years.  See “Theater_Outcomes_vs_Goals.PNG” for a photo of the graph associated with this pivot table.  

###Outcomes Based on Goals 
“Outcomes Based on Goals” is a table that counts the number of successful, failed, and canceled projects and their percentages out of the total of each of the goal categories (less than 1000, 1000-4999, 5000-9999, etc).  Each category corresponds to the money that the project made.  See “Outcome_vs_Goals.PNG” for a photo of the graph associated with this table.

###Challenges 
One of the biggest challenges of this analysis was the use of VLOOKUP in the VLOOKUP sheet.  Originally, the VLOOKUP function was failing to call the correct ID, even when the function appeared to be inputted correctly.  To fix this error, I manually found the first ID (“Be Prepared”) by filtering the names of the Kickstarter sheet by “Be Prepared.” I copied and pasted this into the A2 cell of the VLOOKUP sheet, and found that this fixed the bug.  I then compared the differences between the now working VLOOKUP function with the other ID’s I wanted to call.  I found that there was an additional space following the name of the IDs that was messing up the VLOOKUP function.  For example, when VLOOKUP was originally calling (what I thought was) “Be Prepared”, it was actually calling “Be Preapred “ with a space afterwards.  “Be Preapred “ with a space is not a valid name in the Kickstarter dataset, therefore VLOOKUP was unable to find the name.  After fixing this space, the VLOOKUP function worked perfectly for all other sections.    

## Results 
Based on the “Theater_Outcomes_vs_Launch” graph, the most successful time to launch appears to be in May, where the highest successful outcomes occur.  Theater outcomes between failed and successful appear to cancel each other out in December, where there were only three more successful projects than failed.  Based on the “Outcomes Based on Goals” graph, the number successful and failed appear to follow similar trends.  There are two points in which they deviate greatly - from “1000 to 4999” and “Greater Than 50000” where the number of successful outcomes outweighs the failed outcomes.  Looking at both of these graphs, we can conclude that the “Greater than 50000” section most likely occurred during May, due to the high successful theater outcomes in May.
