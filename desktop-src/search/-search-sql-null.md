---
description: El predicado NULL indica si el documento tiene un valor para la columna indicada.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicado NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705480"
---
# <a name="null-predicate"></a><span data-ttu-id="75635-103">Predicado NULL</span><span class="sxs-lookup"><span data-stu-id="75635-103">NULL Predicate</span></span>

<span data-ttu-id="75635-104">El predicado **null** indica si el documento tiene un valor para la columna indicada.</span><span class="sxs-lookup"><span data-stu-id="75635-104">The **NULL** predicate indicates whether the document has a value for the indicated column.</span></span>

<span data-ttu-id="75635-105">El predicado **null** tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="75635-105">The **NULL** predicate has the following syntax:</span></span>


```
...WHERE <column> IS [NOT] NULL
```



<span data-ttu-id="75635-106">La palabra clave NOT opcional niega el resultado.</span><span class="sxs-lookup"><span data-stu-id="75635-106">The optional NOT keyword negates the result.</span></span> <span data-ttu-id="75635-107">La columna puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado.</span><span class="sxs-lookup"><span data-stu-id="75635-107">The column can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75635-108">Para comprobar si una columna tiene el valor **null** , debe usar el predicado **null** .</span><span class="sxs-lookup"><span data-stu-id="75635-108">To test whether a column has the **NULL** value, you must use the **NULL** predicate.</span></span> <span data-ttu-id="75635-109">No es válido usar el valor **null** en un predicado de comparación.</span><span class="sxs-lookup"><span data-stu-id="75635-109">It is not valid to use the **NULL** value in a comparison predicate.</span></span> <span data-ttu-id="75635-110">"Donde la columna es **null**" es correcta.</span><span class="sxs-lookup"><span data-stu-id="75635-110">"WHERE column IS **NULL**" is correct.</span></span> <span data-ttu-id="75635-111">"WHERE Column = **null**" no es válido.</span><span class="sxs-lookup"><span data-stu-id="75635-111">"WHERE column = **NULL**" is not valid.</span></span>

 

## <a name="example"></a><span data-ttu-id="75635-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="75635-112">Example</span></span>

<span data-ttu-id="75635-113">En el ejemplo siguiente se devuelven documentos que no tienen un valor System. video. Director.</span><span class="sxs-lookup"><span data-stu-id="75635-113">The following example returns documents that do not have a System.Video.Director value.</span></span>


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a><span data-ttu-id="75635-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75635-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="75635-115">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="75635-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75635-116">LIKE (predicado)</span><span class="sxs-lookup"><span data-stu-id="75635-116">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="75635-117">Comparación de valores literales</span><span class="sxs-lookup"><span data-stu-id="75635-117">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="75635-118">Comparaciones de varios valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="75635-118">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="75635-119">**Vista**</span><span class="sxs-lookup"><span data-stu-id="75635-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75635-120">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="75635-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="75635-121">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="75635-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



