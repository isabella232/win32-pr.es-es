---
description: En una base de datos relacional, las filas devueltas por una consulta de búsqueda deben cumplir todas las condiciones llamadas por la consulta. Por el contrario, una consulta de búsqueda de Windows puede devolver documentos que cumplan las condiciones de búsqueda a distintos grados.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Descripción de los valores de relevancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907741"
---
# <a name="understanding-relevance-values"></a><span data-ttu-id="20df3-104">Descripción de los valores de relevancia</span><span class="sxs-lookup"><span data-stu-id="20df3-104">Understanding Relevance Values</span></span>

<span data-ttu-id="20df3-105">En una base de datos relacional, las filas devueltas por una consulta de búsqueda deben cumplir todas las condiciones llamadas por la consulta.</span><span class="sxs-lookup"><span data-stu-id="20df3-105">In a relational database, rows that are returned by a search query must meet all the conditions called for by the query.</span></span> <span data-ttu-id="20df3-106">Por el contrario, una consulta de búsqueda de Windows puede devolver documentos que cumplan las condiciones de búsqueda a distintos grados.</span><span class="sxs-lookup"><span data-stu-id="20df3-106">In contrast, a Windows Search query can return documents that meet the search conditions to varying degrees.</span></span>

<span data-ttu-id="20df3-107">Por ejemplo, una búsqueda del término "programa" en una base de datos relacional genera registros que contienen la ortografía específica de la palabra.</span><span class="sxs-lookup"><span data-stu-id="20df3-107">For example, a search for the term "program" in a relational database produces records that contain that specific spelling of the word.</span></span> <span data-ttu-id="20df3-108">El hecho de que un registro contenga una o 100 instancias de la palabra no afecte a los resultados.</span><span class="sxs-lookup"><span data-stu-id="20df3-108">Whether a record contains one or one hundred instances of the word has no impact on the results.</span></span> <span data-ttu-id="20df3-109">En cambio, Windows Search devuelve un valor de relevancia asociado a los documentos coincidentes.</span><span class="sxs-lookup"><span data-stu-id="20df3-109">In contrast, Windows Search returns a relevance value associated with the matching documents.</span></span> <span data-ttu-id="20df3-110">La relevancia de los documentos que tienen "Program" en el título es mayor que los que contienen la palabra solo en el último párrafo.</span><span class="sxs-lookup"><span data-stu-id="20df3-110">The relevance of documents having "program" in the title is higher than those that contain the word only in the last paragraph.</span></span> <span data-ttu-id="20df3-111">De forma similar, los documentos que contienen variaciones del término de búsqueda, por ejemplo, "programas" y "programación" también coinciden con y son devueltos por la consulta.</span><span class="sxs-lookup"><span data-stu-id="20df3-111">Similarly, documents containing variations of the search term, for example "programs" and "programming" also match and are returned by the query.</span></span>

<span data-ttu-id="20df3-112">Las consultas de Windows Search devuelven valores de relevancia de enteros en la columna denominada "Rank".</span><span class="sxs-lookup"><span data-stu-id="20df3-112">Windows Search queries return integer relevance values in the column named "rank".</span></span>

<span data-ttu-id="20df3-113">Asimismo:</span><span class="sxs-lookup"><span data-stu-id="20df3-113">In addition:</span></span>

-   <span data-ttu-id="20df3-114">Los valores de rango devueltos por la consulta son enteros comprendidos entre 0 y 1000.</span><span class="sxs-lookup"><span data-stu-id="20df3-114">Rank values returned by the query are integers ranging from 0 to 1000.</span></span>
-   <span data-ttu-id="20df3-115">Los valores de clasificación más altos indican documentos que coinciden mejor con las condiciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="20df3-115">Higher rank values indicate documents that better match the search conditions.</span></span>
-   <span data-ttu-id="20df3-116">Los valores de rango solo se aplican a la consulta actual, por lo que no se pueden comparar los resultados entre las consultas.</span><span class="sxs-lookup"><span data-stu-id="20df3-116">Rank values apply only to the current query, so they cannot be compared for results across queries.</span></span>
-   <span data-ttu-id="20df3-117">Los valores de rango son relativos a los demás documentos que coinciden con la consulta.</span><span class="sxs-lookup"><span data-stu-id="20df3-117">Rank values are relative to the other documents matching the query.</span></span> <span data-ttu-id="20df3-118">Por lo tanto, el valor de clasificación de un documento determinado depende de otros documentos que también coinciden con la consulta.</span><span class="sxs-lookup"><span data-stu-id="20df3-118">Therefore, the rank value of a particular document depends on the other documents that also match the query.</span></span>
-   <span data-ttu-id="20df3-119">Los valores de rango de los elementos que coinciden con un predicado puramente relacional son 1000.</span><span class="sxs-lookup"><span data-stu-id="20df3-119">Rank values for items matching a purely relational predicate are 1000.</span></span>

<span data-ttu-id="20df3-120">Puede manipular los valores de rango devueltos mediante el uso de pesos de columna en los predicados de la cláusula [Contains](-search-sql-contains.md) y [FREETEXT](-search-sql-freetext.md) , y la cláusula Rank by.</span><span class="sxs-lookup"><span data-stu-id="20df3-120">You can manipulate the returned rank values by using column weights in the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) WHERE clause predicates, and the RANK BY clause.</span></span>

 

 



