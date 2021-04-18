---
description: Una vez que se devuelve un resultado de una consulta, puede tener acceso a varias propiedades del conjunto de filas.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Propiedades del conjunto de filas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705476"
---
# <a name="rowset-properties"></a><span data-ttu-id="f2736-103">Propiedades del conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="f2736-103">Rowset Properties</span></span>

<span data-ttu-id="f2736-104">Una vez que se devuelve un resultado de una consulta, puede tener acceso a varias propiedades del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="f2736-104">After a result is returned from a query, you can access several properties for the rowset.</span></span>

<span data-ttu-id="f2736-105">Además de las propiedades de conjunto de filas estándar de OLE-DB, Windows Search SQL ofrece las cuatro propiedades personalizadas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f2736-105">In addition to the standard OLE-DB rowset properties, Windows Search SQL offers the following four custom properties.</span></span> <span data-ttu-id="f2736-106">El GUID de este conjunto de propiedades es {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span><span class="sxs-lookup"><span data-stu-id="f2736-106">The GUID for this property set is {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span></span>

<span data-ttu-id="f2736-107">Windows Search admite la propiedad de OLE DB estándar DBPROP \_ COMMANDTIMEOUT del conjunto de propiedades de conjunto de [ \_ filas DBPROPSET](/previous-versions//ms691738(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f2736-107">Windows Search supports the standard OLE-DB property DBPROP\_COMMANDTIMEOUT of the [DBPROPSET\_ROWSET](/previous-versions//ms691738(v=vs.85)) property set.</span></span>



| <span data-ttu-id="f2736-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="f2736-108">Property name</span></span>                  | <span data-ttu-id="f2736-109">PROPID/Type</span><span class="sxs-lookup"><span data-stu-id="f2736-109">PROPID/type</span></span> | <span data-ttu-id="f2736-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2736-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2736-111">DONOTCOMPUTEEXPENSIVEPROPS</span><span class="sxs-lookup"><span data-stu-id="f2736-111">DONOTCOMPUTEEXPENSIVEPROPS</span></span>     | <span data-ttu-id="f2736-112">15/VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="f2736-112">15/VT\_BOOL</span></span> | <span data-ttu-id="f2736-113">Si se establece en true, se evita que se calculen propiedades costosas como los resultados encontrados y el rango máximo que requieren evaluar toda la consulta cuando se tiene acceso a cualquier propiedad de conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="f2736-113">Setting this to true prevents computing expensive properties like Results Found and Max Rank that require evaluating the whole query when any rowset property is accessed.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="f2736-114">Rango máximo ( \_ rango máximo)</span><span class="sxs-lookup"><span data-stu-id="f2736-114">Maximum Rank (MAX\_RANK)</span></span>       | <span data-ttu-id="f2736-115">6/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f2736-115">6/VT\_I4</span></span>    | <span data-ttu-id="f2736-116">La clasificación más alta calculada para cualquier resultado.</span><span class="sxs-lookup"><span data-stu-id="f2736-116">The highest rank computed for any result.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f2736-117">Resultados encontrados (resultados \_ encontrados)</span><span class="sxs-lookup"><span data-stu-id="f2736-117">Results Found (RESULTS\_FOUND)</span></span> | <span data-ttu-id="f2736-118">7/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f2736-118">7/VT\_I4</span></span>    | <span data-ttu-id="f2736-119">Número total de elementos únicos de esta consulta.</span><span class="sxs-lookup"><span data-stu-id="f2736-119">The total number of unique items for this query.</span></span> <span data-ttu-id="f2736-120">En el caso de una consulta SELECT, es el número de elementos del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="f2736-120">For a SELECT query, this is the number of items in the rowset.</span></span> <span data-ttu-id="f2736-121">Para un grupo en consulta, es el número de elementos hoja únicos.</span><span class="sxs-lookup"><span data-stu-id="f2736-121">For a GROUP ON query, this is the number of unique leaf items.</span></span> <span data-ttu-id="f2736-122">Esta propiedad no identifica el número de filas del conjunto de filas de nivel superior (el número de grupos de nivel superior).</span><span class="sxs-lookup"><span data-stu-id="f2736-122">This property does not identify the number of rows in the top-level rowset (the number of top-level groups).</span></span>                                                        |
| <span data-ttu-id="f2736-123">Where ID (WHEREID)</span><span class="sxs-lookup"><span data-stu-id="f2736-123">Where ID (WHEREID)</span></span>             | <span data-ttu-id="f2736-124">8/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f2736-124">8/VT\_I4</span></span>    | <span data-ttu-id="f2736-125">Identificador de las restricciones usadas para una consulta.</span><span class="sxs-lookup"><span data-stu-id="f2736-125">The identifier for the restrictions used for a query.</span></span> <span data-ttu-id="f2736-126">Si un conjunto de filas está abierto cuando se ejecuta una nueva consulta, la nueva consulta puede volver a usar las restricciones de la consulta anterior, con lo que se aprovecha el trabajo ya completado.</span><span class="sxs-lookup"><span data-stu-id="f2736-126">If a rowset is open when a new query is executed, the new query can reuse the restrictions from the older query, thereby taking advantage of the work already completed.</span></span> <span data-ttu-id="f2736-127">Para obtener más información sobre cómo reutilizar las restricciones WHERE, consulte la [función ReuseWhere](-search-sql-reusewhere.md).</span><span class="sxs-lookup"><span data-stu-id="f2736-127">For more information on reusing WHERE restrictions, refer to the [ReuseWhere function](-search-sql-reusewhere.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f2736-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2736-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2736-129">Indexación de los eventos de priorización y de conjunto de filas en Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2736-129">Indexing Prioritization and Rowset Events in Windows 7</span></span>](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
