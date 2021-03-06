---
title: Scalable Sitecore marketing website
titleSuffix: Azure Solution Ideas
author: adamboeglin
ms.date: 12/16/2019
description: With the Sitecore Experience Platform (xP), you have at your fingertips the complete data, integrated tools, and automation capabilities to engage your customers throughout an iterative life cycle—the technology foundation necessary to win customers for life.
ms.custom: acom-architecture, web-apps, 'https://azure.microsoft.com/solutions/architecture/digital-marketing-sitecore/'
ms.service: architecture-center
ms.subservice: solution-idea
---

# Scalable Sitecore marketing website

[!INCLUDE [header_file](../header.md)]

With the Sitecore Experience Platform (xP), you have at your fingertips the complete data, integrated tools, and automation capabilities to engage your customers throughout an iterative life cycle—the technology foundation necessary to win customers for life.

This solution is built on the Azure managed services: [Azure SQL Database](https://azure.microsoft.com/services/sql-database), [Azure Cache for Redis](https://azure.microsoft.com/services/cache), [Azure Cognitive Search](https://azure.microsoft.com/services/search) and [Azure Monitor](https://azure.microsoft.com/services/monitor). These services run in a high-availability environment, patched and supported, allowing you to focus on your solution instead of the environment they run in.

## Architecture

![Architecture diagram](../media/digital-marketing-sitecore.svg)

## Components

* App Service [Web Apps](https://azure.microsoft.com/services/app-service/web) runs in multiple regions, accessible to web and mobile browsers, and is scaled out across multiple server instances. Used by Sitecore to host its content delivery, content management, reporting, and processing roles.
* [Azure SQL Database](https://azure.microsoft.com/services/sql-database): A SQL Database stores and serves data about the site.
* [Azure Cache for Redis](https://azure.microsoft.com/services/cache) enables very fast queries, and improves scalability by reducing the load on the main database. Sitecore's Session State session state is managed by [Azure Cache for Redis](https://azure.microsoft.com/services/cache).
* An [Azure Cognitive Search](https://azure.microsoft.com/services/search) service used for quick look up of data. All Sitecore search indexes are stored in [Azure Cognitive Search](https://azure.microsoft.com/services/search) for quick look up and scalability.
* [Azure Monitor](https://azure.microsoft.com/services/monitor) provides service health and performance monitoring, and diagnostics. [Azure Monitor](https://azure.microsoft.com/services/monitor) provides Sitecore with a solution for its health and performance monitoring needs.

## Next steps

* [Deploy an ASP.NET web app to Azure App Service, using Visual Studio](https://docs.microsoft.com/azure/app-service/app-service-web-get-started-dotnet)
* [SQL Database tutorial: Create a SQL database in minutes by using the Azure portal](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-get-started)
* [How to create a Web App with Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-web-app-howto)
* [Use Azure Cognitive Search](https://azure.microsoft.com/services/search)
* [Application Performance Management with Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview)
