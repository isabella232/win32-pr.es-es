---
description: El Windows search Lenguaje de consulta estructurado (SQL) es similar a una consulta SQL estándar.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Información general sobre la Windows de SQL search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f34f321bef35ab9f5198345a2630d20b80275b794f53a0c47aabf7667f2e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594745"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Información general sobre la Windows de SQL search

El Windows search Lenguaje de consulta estructurado (SQL) es similar a una consulta SQL estándar. Se muestra en las dos sintaxis siguientes:


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

En el ejemplo de consulta siguiente, se devuelven los valores de recuento de páginas y fecha de creación para todos los documentos que tienen más de 50 páginas, ordenados por orden ascendente de recuento de páginas.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

La sintaxis Windows search admite muchas opciones, lo que permite consultas más complicadas.

En la tabla siguiente se describe cada cláusula de las instrucciones SELECT o GROUP ON y las características admitidas.

| Cláusula                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GROUP ON... Sobre...](-search-sql-group-on-over.md) | Especifica cómo agrupar los resultados devueltos por la consulta. Puede especificar los intervalos por los que se va a agrupar y especificar más de una columna para la agrupación. Por ejemplo, puede agrupar los resultados en un intervalo de tamaños de archivo (tamaño < 100, 100 <= tamaño < 1000; 1000 <= tamaño) y agrupaciones de anidamiento.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Especifica las columnas devueltas por la consulta.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Especifica la máquina y el catálogo en los que se buscará.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Especifica lo que constituye un documento que coincide. Esta cláusula tiene muchas opciones, lo que permite un control completo sobre las condiciones de búsqueda. Por ejemplo, puede buscar coincidencias con palabras, frases, formas de palabras inflectionales, cadenas, valores numéricos y bit a bit y matrices con varios valores. También puede aplicar ponderaciones estadísticas a las condiciones de coincidencia y combinar condiciones de coincidencia con operadores booleanos. |
| [ORDER BY](-search-sql-orderby.md)                 | Especifica el criterio de ordenación de los resultados devueltos por la consulta. Puede especificar más de un campo en el que se ordenan los resultados y puede usar una ordenación ascendente o descendente.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Ejemplos de código

El ejemplo de código WSSQL muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de SQL. En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB acceso a aplicaciones de Windows Search y dos métodos adicionales para recuperar resultados de Windows Search. Ambos ejemplos están disponibles en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[Literales](-search-sql-literals.md)

[Uso de búsquedas localizadas](-search-sql-usinglocsearches.md)

[Descripción de los valores de relevancia](-search-sql-understandingrelevancevalues.md)

[Asignaciones de propiedades](-search-3x-wds-propertymappings.md)

[Sintaxis de consulta avanzada](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Conceptual

[SQL Extensiones en Microsoft Windows Search](-search-sql-extensions-sps.md)

[SQL Características no disponibles en Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Identificadores](-search-sql-identifiers.md)

[Confidencialidad de mayúsculas y minúsculas en las búsquedas](-search-sql-casesensitivityinsearches.md)

[Confidencialidad diacrítica en las búsquedas](-search-sql-accentinsensitivitysearches.md)

[Conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md)

[Asignaciones de tipo de datos](-search-sql-datatypemappings.md)
