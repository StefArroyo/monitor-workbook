---
title: |
  Visualizing Log Analytics Data using Azure Monitor Workbooks
titleSuffix: Azure Cosmos DB
description: Use Azure Monitor Workbooks for dashboarding log analytics queries for your Azure Cosmos DB resources.
author: StefArroyo
ms.author: esarroyo
ms.reviewer: sidandrews
ms.service: cosmos-db
ms.topic: tutorial
ms.date: 03/27/2023
---

# Log Analytics Integration with Azure Monitor Workbooks

[!INCLUDE[NoSQL](includes/appliesto-nosql.md)]

Log Analytics Workbook provides comprehensive monitoring of your Azure Cosmos DB resources with Logs as a data source through a unified view of your usage, performance, operations, latency and throttling. This article helps you understand how to use and modify the workbook.

## Visualize your Log Analytics Data
You can use workbooks in the context of a specific Log Analytics workspace to display rich data and analytics of the resource performance, usage, etc.

<img width="1123" alt="log-workbook-gallery" src="https://user-images.githubusercontent.com/29219340/228302858-080a5378-33f8-4dac-90db-c523f81c4d3e.png">

To access Log Analytics Workspace Insights:

1. In the Azure portal, select your Cosmos DB NoSQL account.
2. Under Monitoring, select "Workbooks" on the workspace menu, which will direct you to the workbooks gallery.
3. Select the "Log Analytics Troubleshooting Workbook".

The data is organized in tabs for troubleshooting issues with throughput, latency, throttling, operation management, and storage. The time range on top defaults to the last 7 days and applies to all tabs. It is important to select the database, collection, and workspace you'd like to investigate. 

<img width="1045" alt="select-database-collection-workspace" src="https://user-images.githubusercontent.com/29219340/228302920-425f5329-05ab-4293-b7eb-e53d020df8c8.png">


## View and edit queries
Log Analytics workbooks are versatile such that you can view the exact query being displayed behind the scenes and can further modify it based on your needs. Within each query panel, you can select the "Log Analytics" query editor icon:

<img width="1055" alt="viewing-query-in-la" src="https://user-images.githubusercontent.com/29219340/228302952-f9176457-5b5e-414a-aea3-b50a3b12ebd7.png">


This will take you the the Log Analytics query pane where you can directly modify the query and change parameters such as aggregation type and amount. 

<img width="1201" alt="modify-query-in-la" src="https://user-images.githubusercontent.com/29219340/228302988-b514927e-2c42-4523-ad5d-938290521f92.png">


## Modifying Templates
To modify the existing workbook with new queries or settings, first select Edit, and then add text, queries, and parameters as necessary. 

<img width="536" alt="edit-workbook" src="https://user-images.githubusercontent.com/29219340/228303026-1ad06ddf-8042-4517-a63a-89b886cfb9db.png">


Use the edit buttons on bottom-right of markdown control to update the content for each query panel or text.
<img width="1041" alt="editing-workbook" src="https://user-images.githubusercontent.com/29219340/228303108-0b8da672-9b2f-4d75-b33d-49d7184b580b.png">


## Saving Template

This experience is built on top of Azure Monitor workbook templates. You can use  Edit > Save As to modify and save a copy of your modified version into a custom workbook and resource group. This modified workbook will then live in your specified workbook gallery.


