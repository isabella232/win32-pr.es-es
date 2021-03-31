---
description: Windows Search Lenguaje de consulta estructurado (SQL) es similar a una consulta SQL estándar.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Información general sobre la sintaxis SQL de búsqueda de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082019"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Información general sobre la sintaxis SQL de búsqueda de Windows

Windows Search Lenguaje de consulta estructurado (SQL) es similar a una consulta SQL estándar. Se muestra en las dos siguientes sintaxis:


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

En el siguiente ejemplo de consulta, se devuelven los valores recuento de páginas y fecha de creación para todos los documentos que tienen más de 50 páginas, ordenadas en orden ascendente de recuento de páginas.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

La sintaxis de consulta de búsqueda de Windows admite muchas opciones, lo que permite consultas más complicadas.

En la tabla siguiente se describe cada una de las cláusulas de las instrucciones SELECT o GROUP ON y las características admitidas.

| Cláusula                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AGRUPAR POR... MÁS de...](-search-sql-group-on-over.md) | Especifica cómo agrupar los resultados devueltos por la consulta. Puede especificar los intervalos por los que desea agrupar y especificar más de una columna para la agrupación. Por ejemplo, puede agrupar los resultados en un intervalo de tamaños de archivo (Tamaño < 100, 100 <= tamaño < 1000; 1000 <= tamaño) y anidar agrupaciones.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Especifica las columnas devueltas por la consulta.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Especifica el equipo y el catálogo en los que se va a buscar.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Especifica qué constituye un documento coincidente. Esta cláusula tiene muchas opciones, lo que permite un control completo de las condiciones de búsqueda. Por ejemplo, puede buscar coincidencias con palabras, frases, formatos de palabras con inflexión, cadenas, valores numéricos y bit a bit y matrices multivalor. También puede aplicar pesos estadísticos a las condiciones de coincidencia y combinar las condiciones coincidentes con los operadores booleanos. |
| [ORDER BY](-search-sql-orderby.md)                 | Especifica el criterio de ordenación de los resultados devueltos por la consulta. Puede especificar más de un campo en el que se ordenen los resultados, y puede usar el orden ascendente o descendente.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Ejemplos de código

En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de SQL. En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y dos métodos adicionales para recuperar los resultados de la búsqueda de Windows. Ambos ejemplos están disponibles en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[Literales](-search-sql-literals.md)

[Uso de búsquedas localizadas](-search-sql-usinglocsearches.md)

[Descripción de los valores de relevancia](-search-sql-understandingrelevancevalues.md)

[Asignaciones de propiedades](-search-3x-wds-propertymappings.md)

[Sintaxis de consulta avanzada](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Conceptual

[Extensiones SQL en Microsoft Search](-search-sql-extensions-sps.md)

[Características de SQL no disponibles en Microsoft Search](-search-sql-featuresunavailableinspssearch.md)

[Identificadores](-search-sql-identifiers.md)

[Distinción de mayúsculas y minúsculas en búsquedas](-search-sql-casesensitivityinsearches.md)

[Sensibilidad diacrítica en las búsquedas](-search-sql-accentinsensitivitysearches.md)

[Conversión del tipo de datos de una columna](-search-sql-castingdatacolumntype.md)

[Asignaciones de tipos de datos](-search-sql-datatypemappings.md)
