# tableau-challenge
Modul1 18 - Tableau Challenge

	Following are the different files that I used and created for Module 18 Challenge:
	
	1. Combined_data.csv -> The data includes from Aug 2022 - Jan 2023 as I wanted some summer, fall and winter months.

        Please note, I have deleted many rows from each of the monthly data files to keep the file size under 1 GB. Also,  I was having performance issue with my computer when attempting to load/clean up csv files.

	2. Cleanup-data.ipynb -> is the Jupyter notebook file that contains code to read data from different csv files and combine it into one csv file.  (Code comments are included within the notebook file).

data folder -> contains raw citibike-tripdata csv files from Aug 2022 to Jan 2023.

I have included the following visualizations:

	a. Total Trips Over Time - Since, I have cleaned up most of the data due to size and performance issue, there are less data points for August. But, looking at the visualization, we can say that the Trips start increasing from August and take a dip towards the December holidays and reduce over winter.
	b. Percentage Growth in Ridership: This is plain text visualization. I first created three calculated Fields (i) Initial Trips (ii) Final Trips (iii) Percentage Growth in Ridership using below formula:
	
	Initial Trips = { FIXED [started_at]: COUNTD(IF DATEPART('month', [started_at]) = 8 AND DATEPART('year', [started_at]) = 2022 THEN [ride_id] END) }
	
	Final Trips = { FIXED [started_at]: COUNTD(IF DATEPART('month', [started_at]) = 1 AND DATEPART('year', [started_at]) = 2023 THEN [ride_id] END) }
	
	Percentage Growth = 
	(([Final Trips] - [Initial Trips]) / [Initial Trips]) * 100
	
	c. Changes in User Proportions per Hour (Member vs Casual): is a stacked chart which shows the changes in User proportions each hour through the day.
	I defined a calculated field "Count of Records" using below formula:
	SUM([Count of Records])
	
	d. Top 10 Starting Stations - Created a Bar chart that shows Count RideID for each station Name. Details are shown for Start Station ID. The view is sorted and filtered on Start Station Name, which keeps 10 of remaining dataset.
	
	e. Top 10 Starting Stations - Created a Bar chart that shows Count RideID for each End station Name. Details are shown for End Station ID. The view is sorted and filtered on End Station Name, which keeps 10 of remaining dataset.
	f. Fall Peak Hours
	g. Winter Peak Hours
	h. New York Citibike Usage Visualization dashboard - I just added 5 of the total 8 Visualization on Dashboard.
	i. Map showing Popular Bike Station locations.
	j. I have also added a Story and a Dashboard

	3. Screenshot of all the above Visualizations is copied under folder "Visualization Images" subfolder.
	4. Module18-Homework.twbx  - Tableau Workbook file.
	5. Link to my Public Tableau site which contains solution for Module 18 Homework: 
	6. https://public.tableau.com/app/profile/vineetha.ramachandra/viz/Module18-Homework/NewYorkCitibikeUsageVisualizationstory?publish=yes


	
	
	

          
	
	
	
	
	





