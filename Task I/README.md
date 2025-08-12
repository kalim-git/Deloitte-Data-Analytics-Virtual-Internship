# Task 1: Telemetry Data Analysis in Tableau

This repository contains my solution for Task 1. The goal of this task was to analyze telemetry data from Daikibo's factories and answer two business-critical questions using Tableau.

## Background Information
Daikibo, an industrial manufacturing company, collected telemetry data from four factories worldwide:
- Factory Meiyo (Tokyo, Japan)
- Factory Seiko (Osaka, Japan)
- Daikibo Berlin (Berlin, Germany)
- Daikibo Shenzhen (Shenzhen, China)

Each factory had 9 types of machines, generating telemetry messages every 10 minutes over a one-month period (May 2021)

## Objective
Analyze telemetry data collected from four Daikibo factory locations for the month of May 2021, and answer:
- In which location did machines break the most?
- What are the machines that broke most often in that location?

## Approach

1. **Data Import**
- Imported the **JSON telemetry data** into **Tableau**

2. **Calculated Field**
- Created a calculated field called **`Unhealthy`**
- Formula: `IF [Status] = "Unhealthy" THEN 10 ELSE 0 END`
- This is representing 10 minutes of potential downtime per message

3. **Data Visualization**
- **Sheet1 Bar chart**: "Down Time per Factory" to compare machine downtime across factories.
- **Sheet2 Bar chart**: "Down Time per Device Type" to show breakdowns by machine type.

4. **Designed an interactive dashboard**
- Linked both charts to allow filtering by factory.
- Enabled dynamic insights by selecting a factory to view its machine downtime details.

## Tableau Dashboard
**Task 1**
<img width="1920" height="1080" alt="Dashboard" src="https://github.com/user-attachments/assets/656d30a5-9433-433f-ad29-ca116d19507e" />

## Insights

1.**Factory-Level Downtime**
- **`Daikibo-Factory-Seiko`** experienced the highest downtime with 480 unhealthy units, indicating significant production issues.
- **`Daikibo-Shenzhen`** followed with 420 units, showing potential maintenance gaps.
- **`Daikibo-Factory-Meiyo`** showed moderate downtime at 110 units.
- **`Daikibo-Berlin`** had the least downtime (20 units), suggesting strong equipment health and operational efficiency.

2.**Device-Level Downtime**
- Laser Welder had the highest downtime among all devices (480 units), followed closely by the Laser Cutter (430 units).
- Other devices such as Heavy Duty Drill (70 units) and Furnace (20 units) contributed moderately.
- Devices like Metal Press and Air Wrench reported zero downtime, highlighting their reliability.

## Conclusion
- The major contributors to downtime are specific devices like Laser Welder and Laser Cutter, and factories such as Seiko and Shenzhen.
- These insights can guide preventive maintenance planning, equipment upgrades, and process optimization in the most affected areas.
- Learning from Berlin's efficiency could help improve performance across other locations.






