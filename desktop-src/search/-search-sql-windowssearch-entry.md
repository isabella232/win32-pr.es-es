---
description: Windows La búsqueda proporciona características de búsqueda y rastreo de contenido que admiten la búsqueda de texto completo. El lenguaje de consulta utilizado por Windows Search amplía la sintaxis de consulta de base de datos estándar SQL-92 y SQL-99 para mejorar su utilidad con búsquedas basadas en texto.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Consulta del índice con la sintaxis Windows búsqueda SQL búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2687e5b35e12dd70cca332de92aa19c466907f102f69373e320c6e8162a3dcf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051618"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Consulta del índice con la sintaxis Windows búsqueda SQL búsqueda

Windows La búsqueda proporciona características de búsqueda y rastreo de contenido que admiten la búsqueda de texto completo. El lenguaje de consulta utilizado por Windows Search amplía la sintaxis de consulta de base de datos estándar SQL-92 y SQL-99 para mejorar su utilidad con búsquedas basadas en texto.

Todas las características de Windows Search Lenguaje de consulta estructurado (SQL) son compatibles con Windows Search en Windows Vista y versiones posteriores, incluidas todas las versiones de Windows 10.

En esta sección se proporciona información general sobre SQL sintaxis de Windows Search e incluye los temas siguientes:

- [Introducción a la sintaxis Windows search SQL search](-search-sql-ovwofsearchquery.md)
- [Información general del lenguaje de consulta](-search-sql-generalqueryinfo.md)
- [GROUP ON ... Sobre... Declaración](-search-sql-group-on-over.md)
- [Instrucción SELECT](-search-sql-select.md)
- [From (cláusula)](-search-sql-from.md)
- [Cláusula WHERE](-search-sql-where.md)
- [CLÁUSULA ORDER BY](-search-sql-orderby.md)
- [RANK BY (cláusula)](-search-sql-rankby.md)
- [SET (Instrucción)](-search-sql-set.md)
- [Propiedades del conjunto de filas](-search-sql-rowset-properties.md)

En esta documentación se supone que está familiarizado con Object Linking and Embedding Database (OLE DB) y SQL.

## <a name="code-samples"></a>Ejemplos de código

El ejemplo de código WSSQL muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de SQL. El ejemplo de código WSOleDB muestra Active Template Library (ATL) OLE DB acceso a aplicaciones de Windows Search y dos métodos adicionales para recuperar resultados de Windows Search. Ambos ejemplos están disponibles en los ejemplos [de Windows Search y](-search-samples-ovw.md) el SDK de [Windows 10.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>Temas relacionados

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)

[Usar SQL y enfoques de AQS para consultar el índice](-search-3x-wds-qryidx-overview.md)

[Consulta del índice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Consulta del índice con el protocolo search-ms](-search-3x-wds-qryidx-searchms.md)

[Consulta del índice con la sintaxis Windows search SQL búsqueda](-search-sql-windowssearch-entry.md)

[Uso de la sintaxis de consulta avanzada mediante programación](-search-3x-advancedquerysyntax.md)
