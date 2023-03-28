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

:::image type="content" source="./media/monitor-logs-workbooks/log-workbook-gallery.png" alt-text="Screenshot of the gallery for workbooks" border="true":::

To access Log Analytics Workspace Insights:

1. In the Azure portal, select your Cosmos DB NoSQL account.
2. Under Monitoring, select "Workbooks" on the workspace menu, which will direct you to the workbooks gallery.
3. Select the "Log Analytics Troubleshooting Workbook".

The data is organized in tabs for troubleshooting issues with throughput, latency, throttling, operation management, and storage. The time range on top defaults to the last 7 days and applies to all tabs. It is important to select the database, collection, and workspace you'd like to investigate. 

:::image type="content" source="./media/monitor-logs-workbooks/select-database-collection-workspace.png" alt-text="Screenshot of selection of database, collection, or workspace" border="true":::

## View and edit queries
Log Analytics workbooks are versatile such that you can view the exact query being displayed behind the scenes and can further modify it based on your needs. Within each query panel, you can select the "Log Analytics" query editor icon:

:::image type="content" source="./media/monitor-logs-workbooks/viewing-query-in-la.png" alt-text="Screenshot of editing queries" border="true":::

This will take you the the Log Analytics query pane where you can directly modify the query and change parameters such as aggregation type and amount. 

:::image type="content" source="./media/monitor-logs-workbooks/modify-query-in-la.png" alt-text="Screenshot of how to edit the Log Query for workbooks" border="true":::

## Modifying Templates
To modify the existing workbook with new queries or settings, first select Edit, and then add text, queries, and parameters as necessary. 

:::image type="content" source="./media/monitor-logs-workbooks/edit-workbook.png" alt-text="Screenshot of modifying existing templates" border="true":::

Use the edit buttons on bottom-right of markdown control to update the content for each query panel or text.
:::image type="content" source="./media/monitor-logs-workbooks/editing-workbook.png" alt-text="Screenshot of editing existing workbooks" border="true":::

## Saving Template

This experience is built on top of Azure Monitor workbook templates. You can use  Edit > Save As to modify and save a copy of your modified version into a custom workbook and resource group. This modified workbook will then live in your specified workbook gallery.

## Next Steps 
- For more information on how to create diagnostic settings for Azure Cosmos DB, see [Creating Diagnostics settings](monitor-resource-logs.md).
- For detailed information about how to create a diagnostic setting by using the Azure portal, CLI, or PowerShell, see [create diagnostic setting to collect platform logs and metrics in Azure](../azure-monitor/essentials/diagnostic-settings.md).
- * [Diagnose and troubleshoot Azure Cosmos DB request rate too large (429) exceptions](nosql/troubleshoot-request-rate-too-large.md)
