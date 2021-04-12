---
description: En este tema se describen las tecnologías relacionadas con la búsqueda de Windows.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Tecnologías de búsqueda relacionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153981"
---
# <a name="related-search-technologies"></a>Tecnologías de búsqueda relacionadas

En este tema se describen las tecnologías relacionadas con la [búsqueda de Windows](-search-3x-wds-overview.md).

Este tema se organiza de la siguiente manera:

-   [Búsqueda empresarial](#enterprise-search)
    -   [SharePoint Enterprise Search](#sharepoint-enterprise-search)
-   [Windows Desktop Search 2. x](#windows-desktop-search-2x)
-   [SDK de plataforma: servicio de Index Server](#platform-sdk-indexing-service)
-   [Temas relacionados](#related-topics)

## <a name="enterprise-search"></a>Búsqueda empresarial

Para obtener información general sobre los recursos técnicos de la [búsqueda empresarial de Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), consulte:

-   [Centro de recursos de Enterprise Search](https://developer.microsoft.com/office/docs)
-   [Blog de Microsoft Enterprise Search](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>SharePoint Enterprise Search

SharePoint Foundation 2010 proporciona [consultas desde código del lado servidor](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) y [consultas desde el código del lado cliente](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)). Para obtener más información sobre cómo realizar consultas, buscar contenido nuevo y mejorar la relevancia con SharePoint Server 2010 Enterprise Search, consulte [aspectos básicos de la búsqueda empresarial](/previous-versions/office/ee554857(v=office.14)).

Windows 7 Search admite la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch, que permiten a los usuarios tener acceso a sus datos remotos e interactuar con ellos desde el explorador de Windows. El servidor de búsqueda de SharePoint 2008 y MOSS 2007 SP2 también admiten la búsqueda federada de servidores remotos mediante OpenSearch. Para obtener información acerca de la implementación de Search Server 2008 con Office SharePoint Server 2007, consulte servidor de búsqueda de búsqueda [federada \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)). Para obtener información sobre la búsqueda por facetas de MOSS, en la que se reubican los resultados de búsqueda por categoría, vea [CodePlex](https://www.codeplex.com/FacetedSearch).

Los controladores de protocolo de Windows Search usan especificaciones de diseño similares a las de SharePoint Server y, a menudo, se pueden usar indistintamente. Por lo tanto, cuando los usuarios necesitan buscar bases de datos heredadas, almacenes de correo electrónico u otras estructuras de datos que no son compatibles con la búsqueda de Windows, debe determinar primero si ya existe un controlador de protocolo para ese almacén de datos, quizás para su uso con otra aplicación como SharePoint Server. Si es así, puede instalar el controlador de protocolo en el sistema.

## <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

No se recomienda el uso de y el desarrollo de las versiones 2. x de Microsoft Windows Desktop Search (WDS). En lugar de usar la [búsqueda de escritorio de Windows 2. x](../lwef/-search-2x-wds-overview.md), use [Windows Search](-search-3x-wds-overview.md) y la [API de Windows Search](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>SDK de plataforma: servicio de Index Server

[SDK de la plataforma: el servicio de indización](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) está obsoleto a partir de Windows XP. En su lugar, use [Windows Search](-search-3x-wds-overview.md) y la [API de Windows Search](-search-reference-entry-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Guía del desarrollador de Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Referencia de Windows Search](-search-reference-entry-page.md)
</dt> <dt>

[Ejemplos de código de Windows Search](-search-samples-ovw.md)
</dt> <dt>

[Búsqueda federada en Windows](-search-federated-search-overview.md)
</dt> <dt>

[Glosario de búsqueda de Windows](search-glossary.md)
</dt> </dl>

 

 
