---
title: "Lesson 9: Create Hierarchies | Microsoft Docs"
description: Learn how to create hierarchies for a tabular model project.
ms.date: 05/07/2019
ms.service: analysis-services
ms.custom: tabular-models
ms.topic: tutorial
ms.author: owend
ms.reviewer: owend
author: minewiskan

---
# Lesson 9: Create Hierarchies
[!INCLUDE[appliesto-sql2016-later-aas](../includes/appliesto-sql2016-later-aas.md)]

In this lesson, you will create hierarchies. Hierarchies are groups of columns arranged in levels; for example, a Geography hierarchy might have sub-levels for Country, State, County, and City. Hierarchies can appear separate from other columns in a reporting client application field list, making them easier for client users to navigate and include in a report. To learn more, see [Hierarchies](../tabular-models/hierarchies-ssas-tabular.md).  
  
To create hierarchies, you'll use the model designer in *Diagram View*. Creating and managing hierarchies is not supported in Data View.  
  
Estimated time to complete this lesson: **20 minutes**  
  
## Prerequisites  
This topic is part of a tabular modeling tutorial, which should be completed in order. Before performing the tasks in this lesson, you should have completed the previous lesson: [Lesson 8: Create Perspectives](lesson-8-create-perspectives.md).  
  
## Create hierarchies  
  
#### To create a Category hierarchy in the DimProduct table  
  
1.  In the model designer (diagram view), right-click the **DimProduct** table > **Create Hierarchy**. A new hierarchy appears at the bottom of the table window. Rename the hierarchy **Category**.  
  
2.  Click and drag the **ProductCategoryName** column to the new **Category** hierarchy.  
  
3.  In the **Category** hierarchy, right-click the **ProductCategoryName** > **Rename**, and then type **Category**.  
  
    > [!NOTE]  
    > Renaming a column in a hierarchy does not rename that column in the table. A column in a hierarchy is just a representation of the column in the table.  
  
4.  Click and drag the **ProductSubcategoryName** column to the **Category** hierarchy. Rename it **Subcategory**. 
  
5.  Right-click the **ModelName** column > **Add to hierarchy**, and then select **Category**. Do the same for **EnglishProductName**. Rename these columns in the hierarchy **Model** and **Product**.  

    ![Screenshot of DimProduct > Category showing the columns are named Model and Product.](media/as-tabular-lesson9-category.png)
  
#### To create hierarchies in the DimDate table  
  
1.  In the **DimDate** table, create a new hierarchy named **Calendar**.  
  
3.  Add the following columns in-order:

    *  CalendarYear
    *  CalendarSemester
    *  CalendarQuarter
    *  MonthCalendar
    *  DayNumberOfMonth
    
4.  In the **DimDate** table, create a **Fiscal** hierarchy. Include the following columns:  
  
    *  FiscalYear
    *  FiscalSemester
    *  FiscalQuarter
    *  MonthCalendar
    *  DayNumberOfMonth
  
5.  Finally, in the **DimDate** table, create a **ProductionCalendar** hierarchy. Include the following columns:  
    *  CalendarYear
    *  WeekNumberOfYear
    *  DayNumberOfWeek
  
 ## What's next?
Go to the next lesson: [Lesson 10: Create Partitions](lesson-10-create-partitions.md). 
  
  
