# HealthCare-Data-Analytics

![Data-Analytics](https://github.com/PrinceMario/Health-care/assets/172631198/49dbec3e-58c2-41e1-b7f2-311fee029bcf)




## Project Overview
 This project includes end to end in depth analysis of publicly available healthcare data  regarding patient wating list containig 2 categories inpatient and outpatient using power bi.

 ## Project Goals
 - Track current status of patient waiting list.
 - Analyze historical monthly trend of waiting list in inpatient and outpatient categories.
 - Detailed speciality level and age profile analysis.

## Steps Taken
### Data Preprocessing 
- Integrating both the tables inpatient and outpatient.
- Mapping speciality , creating connection between the two.
- Data transformation, dealing with null, blank and inappropriate values.

### Data Visualization And Insights
Build various interactive charts, donout chart, column chart, show average patient wait list, toggle mechanism which lets user switch between 2 metrics average and median and much more to extract meaningful insights.

####  Some of the measures created using Power Bi DAX  
<pre>
 <code>
 Latest Month Wait List = CALCULATE(SUM(All_Data[Total]),All_Data[Archive_Date] = MAX(All_Data[Archive_Date])) + 0

PY Latest Month Wait List = CALCULATE(SUM(All_Data[Total]),All_Data[Archive_Date]= EDATE(MAX(All_Data[Archive_Date]),-12)) + 0

Avg/Med Wait List = SWITCH(VALUES('Calculation Method'[Calc Method]),"Average",[Average Wait List],"Median",[Median Wait List]) 
  

 </code>
</pre>
### Views Included
- Summary view
- Detailed page for granular analysis

### Report Preview

![summary analysis](https://github.com/deepanshak/HealthCare-Data-Analytics/assets/139687677/197a8483-b2a2-43a0-a29a-e54d919a8b8b)


![detail analysis](https://github.com/deepanshak/HealthCare-Data-Analytics/assets/139687677/681cb257-22a6-4b8a-bf00-8007719cd906)

## Tech Stack
Project makes use of the following key technologies:

- `Power BI Desktop` Design, visualization, and interactive reporting.
- `DAX (Data Analysis Expressions)` Creation of calculations and measures supporting data visualizations.
- `Power Query` Clean and transform raw data into a structured format.

## Files Information
