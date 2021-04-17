---
description: La cláusula WHERE de una consulta especifica un conjunto de elementos con los que buscar coincidencias.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705477"
---
# <a name="reusewhere-function"></a><span data-ttu-id="57533-103">ReuseWhere función)</span><span class="sxs-lookup"><span data-stu-id="57533-103">ReuseWhere Function</span></span>

<span data-ttu-id="57533-104">La cláusula [Where](-search-sql-where.md) de una consulta especifica un conjunto de elementos con los que buscar coincidencias.</span><span class="sxs-lookup"><span data-stu-id="57533-104">The [WHERE](-search-sql-where.md) clause in a query specifies a set of items to match results against.</span></span> <span data-ttu-id="57533-105">Las consultas posteriores pueden compartir el trabajo realizado para una consulta anterior mediante la función ReuseWhere en una nueva cláusula WHERE de consulta.</span><span class="sxs-lookup"><span data-stu-id="57533-105">Subsequent queries can share the work performed for a previous query by using the ReuseWhere function in a new query WHERE clause.</span></span> <span data-ttu-id="57533-106">Las consultas que aprovechan esta función se ejecutan más rápido.</span><span class="sxs-lookup"><span data-stu-id="57533-106">Queries that take advantage of this function execute faster.</span></span>

## <a name="examples"></a><span data-ttu-id="57533-107">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="57533-107">Examples</span></span>

<span data-ttu-id="57533-108">En el escenario siguiente se muestra cómo usar la función ReuseWhere:</span><span class="sxs-lookup"><span data-stu-id="57533-108">The following scenario shows how to use the ReuseWhere function:</span></span>

1.  <span data-ttu-id="57533-109">Se emite la siguiente consulta:</span><span class="sxs-lookup"><span data-stu-id="57533-109">You issue the following query:</span></span>
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  <span data-ttu-id="57533-110">En el conjunto de filas devuelto, se obtiene un [identificador Where](-search-sql-rowset-properties.md), *Query1WhereID*.</span><span class="sxs-lookup"><span data-stu-id="57533-110">From the returned rowset, you get a [Where ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span></span>

    <span data-ttu-id="57533-111">Donde ID es una propiedad de conjunto de filas con PROPSET {aa6ee6b0-e828-11d0-B2-3e-00-AA-00-47-FC-01}, PROPID 8 y Type UI4.</span><span class="sxs-lookup"><span data-stu-id="57533-111">The Where ID is a rowset property with PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8, and type UI4.</span></span>

3.  <span data-ttu-id="57533-112">Se emite una segunda consulta con la función ReuseWhere, pasando el *Query1WhereID* del paso 2:</span><span class="sxs-lookup"><span data-stu-id="57533-112">You issue a second query with the ReuseWhere function, passing in the *Query1WhereID* from step 2:</span></span>
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

<span data-ttu-id="57533-113">La segunda consulta es equivalente a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="57533-113">The second query is equivalent to the following:</span></span>


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



<span data-ttu-id="57533-114">Se puede usar la función ReuseWhere en la cláusula [Where](-search-sql-where.md) .</span><span class="sxs-lookup"><span data-stu-id="57533-114">The ReuseWhere function can be used anwhere in the [WHERE](-search-sql-where.md) clause.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57533-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57533-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="57533-116">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="57533-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57533-117">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="57533-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="57533-118">Propiedades del conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="57533-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



