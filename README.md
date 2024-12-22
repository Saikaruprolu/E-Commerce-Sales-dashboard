# Ecommerce Sales Analysis

## Table of content

  - [Project Overview](#project-overview)
  - [Data Sources](#data-sources)
  - [Tools used/steps followed](#tools-used-and-steps-followed)
  - [DAX used](#dax-used)

## Project Overview

This data analysis project aims to provide insights into the sales performance of Ecommerce company over the past year. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's performance.

![Ecommerce advanced](https://github.com/user-attachments/assets/62baed75-7539-4a8f-bf30-b0aa9e110201)




### Data Sources


Sales Data: The primary dataset used for this analysis is the "Ecommerce_data.csv" file, containing detailed information about each sale made by the company.

### Tools used and steps followed

- Excel - Data Cleaning [Download here](https://microsoft.com)
- PowerBI - Creating reports

🪜𝗦𝘁𝗲𝗽 𝗳𝗼𝗹𝗹𝗼𝘄𝗲𝗱 𝘁𝗼 𝗰𝗿𝗲𝗮𝘁𝗲 𝗿𝗲𝗽𝗼𝗿𝘁:

Import Data : Gathered data from team leads and seamlessly imported it into Power BI for easy access.

📑Data Cleaning:
using power query and power query editor to clean the data like removing null values, remove unnecessary duplicates, change Data types.

📊Data Implementation: used 𝗗𝗔𝗫 function to calculate and adding new measures

🤗I used different types of customized visualization 💻(Area 𝗰𝗵𝗮𝗿𝘁, 𝗦𝘁𝗮𝗰𝗸𝗲𝗱 𝗯𝗮𝗿 𝗰𝗵𝗮𝗿𝘁, 𝗠𝗮𝗽 𝗩𝗶𝘀𝘂𝗮𝗹, Donut 𝗰𝗵𝗮𝗿𝘁 , 𝗠𝗮𝘁𝗿𝗶𝘅 & 𝗦𝗹𝗶𝗰𝗲𝗿 )⌨🖱

### DAX used

Below DAX formulas created ofr each KPI

```KPI
Sales YTD
1)YTD sales = TOTALYTD(SUM(ecommerce_data[sales_per_order]),Calender_table[Date])

2)PYTD SALES =CALCULATE(SUM(ecommerce_data[sales_per_order]),DATESYTD(SAMEPERIODLASTYEAR(Calender_table[Date])))

3)yoy sales = ([YTD sales]-[PYTD SALES])/[PYTD SALES]

4)Sales Icon symbol = var positive_sale=UNICHAR(9650)
 var negative_sale=UNICHAR(9660)
 var final_value= IF([yoy sales]>0,positive_sale,negative_sale)
 return final_value

5)sales Icon color = IF([yoy sales]>0,"Green","Red")

```
![Screenshot 2024-12-22 155728](https://github.com/user-attachments/assets/668dfbc6-0414-4716-b63b-b169be7ba006)


