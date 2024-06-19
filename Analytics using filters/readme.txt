Download the Dataset from the link : https://www.kaggle.com/datasets/ravindrasinghrana/job-description-dataset


Open the code file and run it
It will create a new cleaned csv file with an additional column i.e timestamp

Follow the below steps for working with tableau: 
Steps to Create the Chart
Load the Data into Tableau

Open Tableau and connect to your dataset.
Create Calculated Fields

Create a calculated field to filter the Job Posting Date:

[Job Posting Date] >= #2021-11-30# AND [Job Posting Date] <= #2022-03-30#

Create a calculated field to determine the Work Type based on Preference:

IF [Preference] = 'Male' THEN 'Contract'
ELSEIF [Preference] = 'Female' THEN 'Full-time'
END

Create a calculated field to filter Company Names:

LEFT([Company Name], 1) IN ('M', 'A', 'E')

Create a calculated field to filter the Country:

LEFT([Country], 1) = 'B'

Create a calculated field to filter the Job Portal:

[Job Portal] = 'Indeed'

Create a calculated field to filter the Posting Time:

HOUR([Job Posting date timestamp]) >= 10 AND HOUR([Job Posting date timestamp]) <= 12

Apply Filters

Drag the calculated fields to the Filters shelf:

For Job Posting Date, use the calculated field to filter by the date range.

For Work Type, use the calculated field to filter based on the Work Type determined by Preference.

For Company Name, use the calculated field to filter by the company name initials.

For Country, use the calculated field to filter by countries starting with 'B'.

For Job Portal, use the calculated field to filter by 'Indeed'.

For Job Posting Time, use the calculated field to filter by the time range (10 AM to 12 PM).

Build the Chart

Drag Role to the Rows shelf.
Drag Job Title to the Columns shelf.
Drag Job Id to the Text mark to display the number of job postings.
Configure the Chart

Adjust the chart type and formatting as needed to display the data clearly.


