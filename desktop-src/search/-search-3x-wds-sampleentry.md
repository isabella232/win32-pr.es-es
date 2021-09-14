---
description: En este tema se describen las tecnologías relacionadas con Windows Search.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Tecnologías de búsqueda relacionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262580"
---
# <a name="related-search-technologies"></a>Tecnologías de búsqueda relacionadas

En este tema se describen las tecnologías relacionadas [con Windows Search](-search-3x-wds-overview.md).

Este tema se organiza de la siguiente manera:

-   [Enterprise Búsqueda](#enterprise-search)
    -   [SharePoint Enterprise Search](#sharepoint-enterprise-search)
-   [Windows Búsqueda de escritorio 2.x](#windows-desktop-search-2x)
-   [SDK de plataforma: Servicio de indexación](#platform-sdk-indexing-service)
-   [Temas relacionados](#related-topics)

## <a name="enterprise-search"></a>Enterprise Búsqueda

Para obtener información general sobre los recursos [técnicos Enterprise Search de Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), consulte:

-   [Enterprise Centro de recursos de búsqueda](https://developer.microsoft.com/office/docs)
-   [Blog de Microsoft Enterprise Search](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>SharePoint Enterprise Search

SharePoint Foundation 2010 proporciona consultas desde [código](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) del lado servidor y consultas desde [código del lado cliente](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)). Para obtener más información sobre la consulta, la búsqueda de contenido nuevo y la mejora de la relevancia con la búsqueda de sharepoint Server 2010 Enterprise, vea [Enterprise aspectos](/previous-versions/office/ee554857(v=office.14))básicos de la búsqueda.

Windows 7 Search admite la federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch, que permiten a los usuarios acceder a sus datos remotos e interactuar con ellos desde Windows Explorer. SharePoint Search Server 2008 y MOSS 2007 SP2 también admiten la búsqueda federada de servidores remotos mediante OpenSearch. Para obtener información sobre la implementación de Search Server 2008 con Office SharePoint Server 2007, vea [Federated Search \[ Server 2008 \] ](/previous-versions/office/bb931109(v=office.14)). Para obtener información sobre la búsqueda por caras de MOSS, en la que los resultados de la búsqueda se refina por categoría, vea [Codeplex](https://www.codeplex.com/FacetedSearch).

Windows Los controladores de protocolo de búsqueda usan especificaciones de diseño similares a SharePoint Server, y a menudo se pueden usar indistintamente. Por lo tanto, cuando los usuarios necesitan buscar bases de datos heredadas, almacenes de correo electrónico u otras estructuras de datos que no son compatibles con Windows Search, primero debe determinar si ya existe un controlador de protocolo para ese almacén de datos, quizás para su uso con otra aplicación como SharePoint Server. Si es así, puede instalar ese controlador de protocolo en el sistema.

## <a name="windows-desktop-search-2x"></a>Windows Búsqueda de escritorio 2.x

Se desaconseja encarecidamente el uso y el desarrollo de las versiones 2.x de Microsoft Windows Desktop Search (WDS). En lugar de [usar Windows Desktop Search 2.x,](../lwef/-search-2x-wds-overview.md)use Windows [Search](-search-3x-wds-overview.md) y Windows [Search API](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>SDK de plataforma: Servicio de indexación

[SDK de plataforma: El servicio de indexación](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) está obsoleto a Windows XP. En su lugar, [use Windows Search](-search-3x-wds-overview.md) y Windows Search [API](-search-reference-entry-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Guía del desarrollador de búsqueda](-search-developers-guide-entry-page.md)
</dt> <dt>

[Windows Referencia de búsqueda](-search-reference-entry-page.md)
</dt> <dt>

[Windows Ejemplos de código de búsqueda](-search-samples-ovw.md)
</dt> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Windows Glosario de búsqueda](search-glossary.md)
</dt> </dl>

 

 
