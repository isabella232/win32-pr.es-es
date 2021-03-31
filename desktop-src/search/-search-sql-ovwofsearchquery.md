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
# <a name="overview-of-windows-search-sql-syntax"></a><span data-ttu-id="665e4-103">Información general sobre la sintaxis SQL de búsqueda de Windows</span><span class="sxs-lookup"><span data-stu-id="665e4-103">Overview of Windows Search SQL Syntax</span></span>

<span data-ttu-id="665e4-104">Windows Search Lenguaje de consulta estructurado (SQL) es similar a una consulta SQL estándar.</span><span class="sxs-lookup"><span data-stu-id="665e4-104">The Windows Search Structured Query Language (SQL) is similar to a standard SQL query.</span></span> <span data-ttu-id="665e4-105">Se muestra en las dos siguientes sintaxis:</span><span class="sxs-lookup"><span data-stu-id="665e4-105">It is shown in the following two syntaxes:</span></span>


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

<span data-ttu-id="665e4-106">En el siguiente ejemplo de consulta, se devuelven los valores recuento de páginas y fecha de creación para todos los documentos que tienen más de 50 páginas, ordenadas en orden ascendente de recuento de páginas.</span><span class="sxs-lookup"><span data-stu-id="665e4-106">In the following query example, the page count and date created values are returned for all documents which have more than 50 pages, sorted is ascending order of page count.</span></span>

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

<span data-ttu-id="665e4-107">La sintaxis de consulta de búsqueda de Windows admite muchas opciones, lo que permite consultas más complicadas.</span><span class="sxs-lookup"><span data-stu-id="665e4-107">The Windows Search query syntax supports many options, enabling more complicated queries.</span></span>

<span data-ttu-id="665e4-108">En la tabla siguiente se describe cada una de las cláusulas de las instrucciones SELECT o GROUP ON y las características admitidas.</span><span class="sxs-lookup"><span data-stu-id="665e4-108">The following table describes each clause in the SELECT or GROUP ON statements and the features supported.</span></span>

| <span data-ttu-id="665e4-109">Cláusula</span><span class="sxs-lookup"><span data-stu-id="665e4-109">Clause</span></span>                                              | <span data-ttu-id="665e4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="665e4-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="665e4-111">AGRUPAR POR... MÁS de...</span><span class="sxs-lookup"><span data-stu-id="665e4-111">GROUP ON...OVER...</span></span>](-search-sql-group-on-over.md) | <span data-ttu-id="665e4-112">Especifica cómo agrupar los resultados devueltos por la consulta.</span><span class="sxs-lookup"><span data-stu-id="665e4-112">Specifies how to group results returned by the query.</span></span> <span data-ttu-id="665e4-113">Puede especificar los intervalos por los que desea agrupar y especificar más de una columna para la agrupación.</span><span class="sxs-lookup"><span data-stu-id="665e4-113">You can specify the ranges by which to group and specify more than one column for grouping.</span></span> <span data-ttu-id="665e4-114">Por ejemplo, puede agrupar los resultados en un intervalo de tamaños de archivo (Tamaño < 100, 100 <= tamaño < 1000; 1000 <= tamaño) y anidar agrupaciones.</span><span class="sxs-lookup"><span data-stu-id="665e4-114">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size) and nest groupings.</span></span>                                                                                                       |
| [<span data-ttu-id="665e4-115">SELECT</span><span class="sxs-lookup"><span data-stu-id="665e4-115">SELECT</span></span>](-search-sql-select.md)                    | <span data-ttu-id="665e4-116">Especifica las columnas devueltas por la consulta.</span><span class="sxs-lookup"><span data-stu-id="665e4-116">Specifies the columns returned by the query.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="665e4-117">FROM</span><span class="sxs-lookup"><span data-stu-id="665e4-117">FROM</span></span>](-search-sql-from.md)                        | <span data-ttu-id="665e4-118">Especifica el equipo y el catálogo en los que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="665e4-118">Specifies the machine and catalog to search.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="665e4-119">WHERE</span><span class="sxs-lookup"><span data-stu-id="665e4-119">WHERE</span></span>](-search-sql-where.md)                      | <span data-ttu-id="665e4-120">Especifica qué constituye un documento coincidente.</span><span class="sxs-lookup"><span data-stu-id="665e4-120">Specifies what constitutes a matching document.</span></span> <span data-ttu-id="665e4-121">Esta cláusula tiene muchas opciones, lo que permite un control completo de las condiciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="665e4-121">This clause has many options, enabling rich control over the search conditions.</span></span> <span data-ttu-id="665e4-122">Por ejemplo, puede buscar coincidencias con palabras, frases, formatos de palabras con inflexión, cadenas, valores numéricos y bit a bit y matrices multivalor.</span><span class="sxs-lookup"><span data-stu-id="665e4-122">For example, you can match against words, phrases, inflectional word forms, strings, numeric and bitwise values, and multi-valued arrays.</span></span> <span data-ttu-id="665e4-123">También puede aplicar pesos estadísticos a las condiciones de coincidencia y combinar las condiciones coincidentes con los operadores booleanos.</span><span class="sxs-lookup"><span data-stu-id="665e4-123">You can also apply statistical weights to the matching conditions, and combine matching conditions with Boolean operators.</span></span> |
| [<span data-ttu-id="665e4-124">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="665e4-124">ORDER BY</span></span>](-search-sql-orderby.md)                 | <span data-ttu-id="665e4-125">Especifica el criterio de ordenación de los resultados devueltos por la consulta.</span><span class="sxs-lookup"><span data-stu-id="665e4-125">Specifies the sort order for the results returned by the query.</span></span> <span data-ttu-id="665e4-126">Puede especificar más de un campo en el que se ordenen los resultados, y puede usar el orden ascendente o descendente.</span><span class="sxs-lookup"><span data-stu-id="665e4-126">You can specify more than one field on which the results are sorted, and you can use ascending or descending ordering.</span></span>                                                                                                                                                                                                               |

### <a name="code-samples"></a><span data-ttu-id="665e4-127">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="665e4-127">Code samples</span></span>

<span data-ttu-id="665e4-128">En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de SQL.</span><span class="sxs-lookup"><span data-stu-id="665e4-128">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="665e4-129">En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y dos métodos adicionales para recuperar los resultados de la búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="665e4-129">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="665e4-130">Ambos ejemplos están disponibles en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="665e4-130">Both samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

## <a name="related-topics"></a><span data-ttu-id="665e4-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="665e4-131">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="665e4-132">Referencia</span><span class="sxs-lookup"><span data-stu-id="665e4-132">Reference</span></span>

[<span data-ttu-id="665e4-133">Literales</span><span class="sxs-lookup"><span data-stu-id="665e4-133">Literals</span></span>](-search-sql-literals.md)

[<span data-ttu-id="665e4-134">Uso de búsquedas localizadas</span><span class="sxs-lookup"><span data-stu-id="665e4-134">Using Localized Searches</span></span>](-search-sql-usinglocsearches.md)

[<span data-ttu-id="665e4-135">Descripción de los valores de relevancia</span><span class="sxs-lookup"><span data-stu-id="665e4-135">Understanding Relevance Values</span></span>](-search-sql-understandingrelevancevalues.md)

[<span data-ttu-id="665e4-136">Asignaciones de propiedades</span><span class="sxs-lookup"><span data-stu-id="665e4-136">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)

[<span data-ttu-id="665e4-137">Sintaxis de consulta avanzada</span><span class="sxs-lookup"><span data-stu-id="665e4-137">Advanced Query Syntax</span></span>](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a><span data-ttu-id="665e4-138">Conceptual</span><span class="sxs-lookup"><span data-stu-id="665e4-138">Conceptual</span></span>

[<span data-ttu-id="665e4-139">Extensiones SQL en Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="665e4-139">SQL Extensions in Microsoft Windows Search</span></span>](-search-sql-extensions-sps.md)

[<span data-ttu-id="665e4-140">Características de SQL no disponibles en Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="665e4-140">SQL Features Unavailable in Microsoft Windows Search</span></span>](-search-sql-featuresunavailableinspssearch.md)

[<span data-ttu-id="665e4-141">Identificadores</span><span class="sxs-lookup"><span data-stu-id="665e4-141">Identifiers</span></span>](-search-sql-identifiers.md)

[<span data-ttu-id="665e4-142">Distinción de mayúsculas y minúsculas en búsquedas</span><span class="sxs-lookup"><span data-stu-id="665e4-142">Case Sensitivity in Searches</span></span>](-search-sql-casesensitivityinsearches.md)

[<span data-ttu-id="665e4-143">Sensibilidad diacrítica en las búsquedas</span><span class="sxs-lookup"><span data-stu-id="665e4-143">Diacritic Sensitivity in Searches</span></span>](-search-sql-accentinsensitivitysearches.md)

[<span data-ttu-id="665e4-144">Conversión del tipo de datos de una columna</span><span class="sxs-lookup"><span data-stu-id="665e4-144">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)

[<span data-ttu-id="665e4-145">Asignaciones de tipos de datos</span><span class="sxs-lookup"><span data-stu-id="665e4-145">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
