**Energy Consumption Dashboard**

**Project Overview**

An interactive Power BI tool called the Energy Consumption Dashboard was created to monitor, evaluate, and display energy (electricity, gas, and water) usage in various towns and buildings. To support improved decision-making and cost management, the dashboard offers vital insights into overall energy prices, usage patterns, and trends.Facility managers, sustainability teams, and decision-makers can find inefficiencies, optimize energy use, and save operating costs with the help of this project.

**Objectives**

Track and evaluate the energy usage of electricity, gas, and water.
Forecast consumption growth and provide historical trends.
Find chances for cost savings by identifying buildings that are expensive and consume a lot of energy.
Provide stakeholders with an intuitive and engaging dashboard.
Use effective data modeling and optimization strategies to boost output.
Project Workflow

**1.Data Collection & ETL (Extract, Transform, Load)**

Data Sources: Data on energy usage was taken from a variety of sources, including SQL databases, Excel, and API feeds.included monthly energy use information for several cities and buildings from 2016 to 2019.
Data Cleaning & Transformation: Used Power Query (M Language) to handle outliers, missing values, and inconsistent data.transformed information for analysis into a structured manner.Formatted and aggregated dates for trend analysis.
Data Modeling: Fact and dimension tables were made in order to facilitate effective connections in Power BI.For improved query efficiency, efficient relationships (Star Schema) were implemented.

**2. Dashboard Development & Design**

Three distinct sections make up the dashboard, each of which is devoted to a different energy type: electricity, gas, and water.

 **Main KPI Metrics Display:**

Total Cost (in millions): Shows the total cost of energy.
Total Units Consumed (in millions): This indicates how much energy was used during the chosen time frame.
City, Building, and Date Range Filters: These filters let users dynamically filter data.
Total Cost by Date and Consumption Type:

Uses a time-series line chart to monitor monthly cost patterns over time; aids in spotting cost swings and seasonal surges.
 Total Cost by City:

A pie chart representation of the distribution of energy costs in various cities.
Assists in identifying the cities with the highest energy use for strategic cost reduction.
 Total Cost by Building:

Visualization of a bar chart showing energy costs by building.
Assists facility managers in locating buildings with excessive usage.
Monthly Energy Consumption and Cost Breakdown (Table View):

Year, Quarter, Month, Units Consumed, and Total Cost are all included in this comprehensive table.
Enables users to examine trends of energy use in greater detail.

**3. DAX Measures & Calculations Used**

Total Energy Cost:

Total Cost = SUM(ConsumptionData[Total Cost])

Total Units Consumed:

Total Units = SUM(ConsumptionData[Unit Consumed])
Year-over-Year (YoY) Growth Analysis:
YoY Growth = 
VAR PrevYear = CALCULATE(SUM(ConsumptionData[Total Cost]), SAMEPERIODLASTYEAR(Date[Date]))
RETURN IF(ISBLANK(PrevYear), BLANK(), (SUM(ConsumptionData[Total Cost]) - PrevYear) / PrevYear)
Dynamic Filtering for Cities and Buildings:
Slicers and page-level filters were added to enable users to delve deeper into particular towns and structures.

**4. Challenges & Solutions**

Problem-Solving Put into practice
Dashboard performance is impacted by a large dataset.For quicker load times, indexing, DAX measure optimization, and aggregations were used.
Making sure data is updated in real timeConfigure Power BI Service to perform automatic updates by scheduling refreshes.
Managing a variety of data formats used Power Query transforms to make the dataset clean and consistent.
Dynamic filtering across several views is required.using cross-filtering methods and DAX measures.

**5. Impact & Business Value**

Improved Decision-Making: Stakeholders may now quickly monitor energy usage trends and expenses.
Cost Optimization: Determined which buildings were expensive and put energy-saving measures in place.
Operational Efficiency: By automating data integration and visualization, less manual reporting work was required.
Scalability: Additional energy kinds and timeframes can be added to the dashboard.

**6. Future Enhancements**
Predictive analytics: Use AI/ML models to predict how much energy will be used in the future.
Connect real-time sensor data for live monitoring through integration with IoT sensors.
Mobile Optimization: Create a mobile-friendly, responsive version of Power BI.

**Conclusion:**
A strong analytics tool, the Energy Consumption Dashboard offers comprehensive information on cost distribution, efficiency prospects, and patterns in energy use. This project helps businesses make data-driven choices and manage energy use by utilizing Power BI best practices, efficient DAX formulas, and an easy-to-use user interface.
