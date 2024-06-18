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
 Average wait list = AVERAGE(All_Data[Total])
  
 Avg/Med wait list = SWITCH(VALUES('Calculation Method'[Calc Method]), "Average", 'Measure table'[Average wait list], "Median", 'Measure table'[Median wait list])
  
 Dynamic title = SWITCH(VALUES('Calculation Method'[Calc Method]), "Average", "Patient wait list(Average)", "Median", "Patient wait list(Median)")
  
 Lastest month wait list = CALCULATE( SUM(All_Data[Total]), All_Data[Archive_Date] = MAX(All_Data[Archive_Date]))
  
 Median wait list = MEDIAN(All_Data[Total])
  
 No data left = if (ISBLANK(CALCULATE(sum(All_Data[Total]), All_Data[Case_Type] <> "Outpatient")), "No data for selected criteria", "")
  
 No data right = if (ISBLANK(CALCULATE(sum(All_Data[Total]), All_Data[Case_Type] = "Outpatient")), "No data for selected criteria", "")
  
 PY Lastest month wait list = CALCULATE( SUM(All_Data[Total]), All_Data[Archive_Date] = EDATE(MAX(All_Data[Archive_Date]), -12)) + 0

 </code>
</pre>
### Views Included
- Summary view
- Detailed page for granular analysis

### Report Preview

![Preview 1](https://github.com/PrinceMario/Health-care/assets/172631198/bc4082aa-9448-44a3-9cc3-9dee5240a40c)


![Preview 2](https://github.com/PrinceMario/Health-care/assets/172631198/2b4ed11a-583f-4c6d-be47-b09643d42bfb)

## Tech Stack
Project makes use of the following key technologies:

- `Power BI Desktop` Design, visualization, and interactive reporting.
- `DAX (Data Analysis Expressions)` Creation of calculations and measures supporting data visualizations.
- `Power Query` Clean and transform raw data into a structured format.

## Files Information
