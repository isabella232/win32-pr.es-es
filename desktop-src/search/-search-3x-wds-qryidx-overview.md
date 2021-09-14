---
description: Hay varias maneras de usar Windows Search para consultar el índice.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Consulta del índice mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262588"
---
# <a name="querying-the-index-programmatically"></a>Consulta del índice mediante programación

Hay varias maneras de usar Windows Search para consultar el índice.

En esta sección se proporciona el marco conceptual para consultar el índice mediante programación:

-   [Usar SQL y enfoques de AQS para consultar el índice](using-sql-and-aqs-to-query-the-index.md)
-   [Consulta del índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Consulta del índice con el protocolo search-ms](-search-3x-wds-qryidx-searchms.md)
-   [Consulta del índice con la sintaxis Windows search SQL búsqueda](-search-sql-windowssearch-entry.md)
-   [Uso de la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md)

> [!Note]  
> Compatibilidad 2x de Microsoft Windows Desktop Search (WDS) heredada: en equipos que ejecutan Windows XP y versiones posteriores, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) está en desuso. En su lugar, los desarrolladores deben usar [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) para obtener una cadena de conexión y analizar la consulta del usuario en Lenguaje de consulta estructurado (SQL) y, a continuación, consultar a través de Object Linking and Embedding Database (OLE DB).

 

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre OLE DB, vea [información general sobre OLE DB programación.](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx) Para obtener información sobre el .NET Framework de datos para OLE DB, vea el espacio de nombres [System.Data.OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Para obtener información adicional sobre el uso de propiedades en las consultas, vea los temas siguientes:
    -   [Sistema de propiedades](../properties/building-property-handlers.md)
    -   [Propiedades del sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Para obtener información sobre cómo crear y modificar carpetas de búsqueda, vea [**ISearchFolderItemFactory Interface**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   Para ver los paneles de mensajes de preguntas y discusión admitidos por la comunidad sobre las tecnologías de búsqueda, vea [Foro de MSDN: Windows desarrollo de búsqueda de escritorio.](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)
-   Para descargar los ejemplos de código del SDK de Search:
    -   Para Windows 7: [Windows search samples on GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   Para Windows Vista: ejemplos [del SDK Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   Para descargar el SDK Windows:
    -   Para Windows 7: [SDK Windows para Windows 7 y .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   Para Windows Vista: [SDK Windows para Windows Vista y .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Guía de desarrollo de búsqueda](-search-developers-guide-entry-page.md)
</dt> <dt>

[Administración del índice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Extender el índice Windows Search](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Extensión de recursos de lenguaje](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
