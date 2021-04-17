---
description: Windows Search proporciona características de búsqueda y rastreo de contenido que admiten la búsqueda de texto completo. El lenguaje de consulta que usa Windows Search amplía la sintaxis de consulta de base de datos SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Consultar el índice con la sintaxis SQL de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497062"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Consultar el índice con la sintaxis SQL de Windows Search

Windows Search proporciona características de búsqueda y rastreo de contenido que admiten la búsqueda de texto completo. El lenguaje de consulta que usa Windows Search amplía la sintaxis de consulta de base de datos SQL-92 y SQL-99 para mejorar su utilidad con las búsquedas basadas en texto.

Todas las características de Windows Search Lenguaje de consulta estructurado (SQL) son compatibles con Windows Search en Windows Vista y versiones posteriores, incluidas todas las versiones de Windows 10.

En esta sección se proporciona información general sobre la sintaxis de SQL en Windows Search e incluye los temas siguientes:

- [Información general sobre la sintaxis SQL de búsqueda de Windows](-search-sql-ovwofsearchquery.md)
- [Información general del lenguaje de consulta](-search-sql-generalqueryinfo.md)
- [AGRUPAR POR... MÁS de... Privacidad](-search-sql-group-on-over.md)
- [Instrucción SELECT](-search-sql-select.md)
- [Cláusula FROM](-search-sql-from.md)
- [Cláusula WHERE](-search-sql-where.md)
- [Cláusula ORDER BY](-search-sql-orderby.md)
- [RANK BY (cláusula)](-search-sql-rankby.md)
- [SET (instrucción)](-search-sql-set.md)
- [Propiedades del conjunto de filas](-search-sql-rowset-properties.md)

En esta documentación se supone que está familiarizado con la vinculación de objetos y la incrustación de base de datos (OLE DB) y SQL.

## <a name="code-samples"></a>Ejemplos de código

En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de SQL. En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y dos métodos adicionales para recuperar los resultados de la búsqueda de Windows. Ambos ejemplos están disponibles en los [ejemplos de Windows Search](-search-samples-ovw.md) y en el [SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>Temas relacionados

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)

[Uso de enfoques de SQL y AQS para consultar el índice](-search-3x-wds-qryidx-overview.md)

[Consultar el índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Consultar el índice con el protocolo Search-MS](-search-3x-wds-qryidx-searchms.md)

[Consultar el índice con la sintaxis SQL de Windows Search](-search-sql-windowssearch-entry.md)

[Usar la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md)
