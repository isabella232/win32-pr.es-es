---
description: 'Más información acerca de: cláusula ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Cláusula ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153955"
---
# <a name="order-by-clause"></a><span data-ttu-id="18671-103">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="18671-103">ORDER BY Clause</span></span>

<span data-ttu-id="18671-104">La cláusula ORDER BY ordena los resultados en función del valor de una o más columnas especificadas.</span><span class="sxs-lookup"><span data-stu-id="18671-104">The ORDER BY clause sorts the results based on the value of one or more columns you specify.</span></span> <span data-ttu-id="18671-105">A continuación se especifica la sintaxis de la cláusula ORDER BY:</span><span class="sxs-lookup"><span data-stu-id="18671-105">Following is the syntax of the ORDER BY clause:</span></span>


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



<span data-ttu-id="18671-106">El especificador de columna debe ser una columna válida.</span><span class="sxs-lookup"><span data-stu-id="18671-106">The column specifier must be a valid column.</span></span> <span data-ttu-id="18671-107">Puede usar el especificador de columna para hacer referencia a las columnas por el orden en que aparecen en la consulta.</span><span class="sxs-lookup"><span data-stu-id="18671-107">You can use the column specifier to refer to columns by the order that they appear in the query.</span></span> <span data-ttu-id="18671-108">La primera columna de la consulta tiene el número 1.</span><span class="sxs-lookup"><span data-stu-id="18671-108">The first column in the query is numbered 1.</span></span> <span data-ttu-id="18671-109">Puede incluir más de una columna en la cláusula ORDER BY, separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="18671-109">You can include more than one column in the ORDER BY clause, separated by commas.</span></span>

<span data-ttu-id="18671-110">El especificador de dirección opcional puede ser "ASC" para ascendente (inferior a alto) o "DESC" para descendente (de alto a bajo).</span><span class="sxs-lookup"><span data-stu-id="18671-110">The optional direction specifier can be either "ASC" for ascending (low to high) or "DESC" for descending (high to low).</span></span> <span data-ttu-id="18671-111">Si no se proporciona un especificador de dirección, se utiliza el valor predeterminado, ascendente.</span><span class="sxs-lookup"><span data-stu-id="18671-111">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="18671-112">Si especifica más de una columna, pero no especifica todas las direcciones, la dirección que especifique en último lugar se aplicará a cada columna hasta que cambie explícitamente la dirección.</span><span class="sxs-lookup"><span data-stu-id="18671-112">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each column until you explicitly change the direction.</span></span>

<span data-ttu-id="18671-113">Por ejemplo, en la siguiente cláusula ORDER BY, las columnas A, B, C y G se ordenan en orden ascendente, mientras que las columnas D, E y F se ordenan en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="18671-113">For example, in the following ORDER BY clause, the columns A, B, C, and G are sorted in ascending order, while columns D, E, and F are sorted in descending order.</span></span>


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a><span data-ttu-id="18671-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18671-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="18671-115">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="18671-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18671-116">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="18671-116">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="18671-117">RANK BY (cláusula)</span><span class="sxs-lookup"><span data-stu-id="18671-117">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

[<span data-ttu-id="18671-118">Instrucción SELECT</span><span class="sxs-lookup"><span data-stu-id="18671-118">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

<span data-ttu-id="18671-119">**Vista**</span><span class="sxs-lookup"><span data-stu-id="18671-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18671-120">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="18671-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="18671-121">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="18671-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



