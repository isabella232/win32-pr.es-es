---
description: Microsoft Windows Search, basado en los estándares SQL-92 y SQL-99, mejora las búsquedas basadas en documentos de texto completo en aplicaciones de administración de documentos o de administración de conocimiento.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Extensiones SQL en Microsoft Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540678"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a><span data-ttu-id="f44ba-103">Extensiones SQL en Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="f44ba-103">SQL Extensions in Microsoft Windows Search</span></span>

<span data-ttu-id="f44ba-104">Microsoft Windows Search, basado en los estándares SQL-92 y SQL-99, mejora las búsquedas basadas en documentos de texto completo en aplicaciones de administración de documentos o de administración de conocimiento.</span><span class="sxs-lookup"><span data-stu-id="f44ba-104">Microsoft Windows Search, based on the SQL-92 and SQL-99 standards, improves full-text document-based searches in document-management or knowledge-management applications.</span></span> <span data-ttu-id="f44ba-105">Entre las mejoras de Windows Search se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="f44ba-105">Windows Search improvements include the following:</span></span>

## <a name="128-character-identifier-names"></a><span data-ttu-id="f44ba-106">128: nombres de identificador de caracteres</span><span class="sxs-lookup"><span data-stu-id="f44ba-106">128-Character Identifier Names</span></span>

<span data-ttu-id="f44ba-107">Si bien SQL-92 y SQL-99 restringen la columna y otros identificadores a 18 caracteres, Windows Search admite nombres de columna de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f44ba-107">While SQL-92 and SQL-99 restrict column and other identifiers to 18 characters, Windows Search supports 128-character column names.</span></span> <span data-ttu-id="f44ba-108">Para obtener más información, vea [Identificadores](-search-sql-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="f44ba-108">For more information, see [Identifiers](-search-sql-identifiers.md).</span></span>

## <a name="grouping-results-by-columns"></a><span data-ttu-id="f44ba-109">Agrupar resultados por columnas</span><span class="sxs-lookup"><span data-stu-id="f44ba-109">Grouping Results by Columns</span></span>

<span data-ttu-id="f44ba-110">Las consultas pueden especificar cómo agrupar los resultados.</span><span class="sxs-lookup"><span data-stu-id="f44ba-110">Queries can specify how to group results.</span></span> <span data-ttu-id="f44ba-111">Puede especificar los intervalos por los que desea agrupar y puede especificar más de una columna para la agrupación.</span><span class="sxs-lookup"><span data-stu-id="f44ba-111">You can specify the ranges by which to group, and you can specify more than one column for grouping.</span></span> <span data-ttu-id="f44ba-112">Por ejemplo, puede agrupar los resultados en un intervalo de tamaños de archivo (Tamaño < 100, 100 <= tamaño < 1000; 1000 <= tamaño) y puede anidar agrupaciones.</span><span class="sxs-lookup"><span data-stu-id="f44ba-112">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size), and you can nest groupings.</span></span> <span data-ttu-id="f44ba-113">Para obtener más información, vea [Agrupar por... MÁS de... Instrucción](-search-sql-group-on-over.md).</span><span class="sxs-lookup"><span data-stu-id="f44ba-113">For more information, see [GROUP ON ... OVER... Statement](-search-sql-group-on-over.md).</span></span>

## <a name="diacritic-insensitive-searching"></a><span data-ttu-id="f44ba-114">Búsqueda de Diacritic-Insensitive</span><span class="sxs-lookup"><span data-stu-id="f44ba-114">Diacritic-Insensitive Searching</span></span>

<span data-ttu-id="f44ba-115">Además de la búsqueda que no distingue entre mayúsculas y minúsculas, la búsqueda de Windows admite búsquedas que no se distinguen por signos diacríticos (marcas de acento).</span><span class="sxs-lookup"><span data-stu-id="f44ba-115">In addition to searching that is not case-sensitive, Windows Search supports searching that is not sensitive to diacritics (accent marks).</span></span> <span data-ttu-id="f44ba-116">Para obtener más información, vea [sensibilidad diacríticas en las búsquedas](-search-sql-accentinsensitivitysearches.md).</span><span class="sxs-lookup"><span data-stu-id="f44ba-116">For more information, see [Diacritic Sensitivity in Searches](-search-sql-accentinsensitivitysearches.md).</span></span>

## <a name="column-weighting"></a><span data-ttu-id="f44ba-117">Ponderación de columnas</span><span class="sxs-lookup"><span data-stu-id="f44ba-117">Column Weighting</span></span>

<span data-ttu-id="f44ba-118">Las consultas que buscan más de una columna pueden especificar la importancia de cada columna.</span><span class="sxs-lookup"><span data-stu-id="f44ba-118">Queries that search more than one column can specify the importance of each column.</span></span> <span data-ttu-id="f44ba-119">Los predicados [Contains](-search-sql-contains.md) y [FREETEXT](-search-sql-freetext.md) admiten la ponderación de las columnas.</span><span class="sxs-lookup"><span data-stu-id="f44ba-119">The [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates both support column weighting.</span></span>

## <a name="null-predicate"></a><span data-ttu-id="f44ba-120">Predicado NULL</span><span class="sxs-lookup"><span data-stu-id="f44ba-120">NULL Predicate</span></span>

<span data-ttu-id="f44ba-121">Aunque la indización de contenido de texto completo no tiene ningún conjunto de columnas definido, las consultas pueden requerir que los miembros del conjunto de resultados o no tengan columnas especificadas.</span><span class="sxs-lookup"><span data-stu-id="f44ba-121">Although full-text content indexing has no defined set of columns, queries can require that members of the result set do or do not have specified columns.</span></span> <span data-ttu-id="f44ba-122">No es posible diferenciar entre un documento que tiene una propiedad especificada con el valor establecido en **null** y un documento que no tiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="f44ba-122">It is not possible to differentiate between a document has a specified property with the value set to **NULL**, and a document that does not have the property at all.</span></span>

## <a name="rank-modification"></a><span data-ttu-id="f44ba-123">Modificación de rango</span><span class="sxs-lookup"><span data-stu-id="f44ba-123">Rank Modification</span></span>

<span data-ttu-id="f44ba-124">Puede manipular la clasificación de los resultados de la búsqueda mediante [pesos](-search-sql-understandingrelevancevalues.md) en las propiedades y en grupos de propiedades con alias.</span><span class="sxs-lookup"><span data-stu-id="f44ba-124">You can manipulate the search results ranking by using [weights](-search-sql-understandingrelevancevalues.md) on properties and on aliased groups of properties.</span></span> <span data-ttu-id="f44ba-125">La coerción de rangos admite la manipulación directa de la clasificación de relevancia en función de los criterios que se especifiquen.</span><span class="sxs-lookup"><span data-stu-id="f44ba-125">Rank coercion supports direct manipulation of the relevance ranking based on the criteria you specify.</span></span>

 

 



