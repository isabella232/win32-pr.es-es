---
description: Los resultados de una consulta incluyen las filas devueltas por la consulta y un valor de clasificación para cada fila si la columna Rank se incluye en la cláusula SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275263"
---
# <a name="rank-by-clause"></a><span data-ttu-id="84766-103">RANK BY (cláusula)</span><span class="sxs-lookup"><span data-stu-id="84766-103">RANK BY Clause</span></span>

<span data-ttu-id="84766-104">Los resultados de una consulta incluyen las filas devueltas por la consulta y un valor de clasificación para cada fila si la columna Rank se incluye en la cláusula SELECT.</span><span class="sxs-lookup"><span data-stu-id="84766-104">The results from a query include both the rows returned by the query and a rank value for each row if the rank column is included in the SELECT clause.</span></span> <span data-ttu-id="84766-105">Los valores de rango se calculan mediante el motor de búsqueda y se devuelven como enteros en el intervalo comprendido entre cero y 1000.</span><span class="sxs-lookup"><span data-stu-id="84766-105">The rank values are calculated by the Search engine and are returned as integers in the range zero to 1000.</span></span> <span data-ttu-id="84766-106">Para que los resultados de la clasificación sean más significativos, la consulta puede controlar cómo se calculan los valores de clasificación sin formato en la cláusula RANK BY.</span><span class="sxs-lookup"><span data-stu-id="84766-106">To make the rank results more meaningful, the query can control how raw rank values are calculated in the RANK BY clause.</span></span>

<span data-ttu-id="84766-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="84766-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="84766-108">RANK BY (cláusula)</span><span class="sxs-lookup"><span data-stu-id="84766-108">RANK BY Clause</span></span>](#rank-by-clause)
-   [<span data-ttu-id="84766-109">Función WEIGHT</span><span class="sxs-lookup"><span data-stu-id="84766-109">WEIGHT Function</span></span>](#weight-function)
-   [<span data-ttu-id="84766-110">Función de coerción</span><span class="sxs-lookup"><span data-stu-id="84766-110">COERCION Function</span></span>](#coercion-function)

## <a name="rank-by-clause"></a><span data-ttu-id="84766-111">RANK BY (cláusula)</span><span class="sxs-lookup"><span data-stu-id="84766-111">RANK BY Clause</span></span>

<span data-ttu-id="84766-112">La sintaxis de la cláusula RANK BY es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="84766-112">The syntax for the RANK BY clause is as follows:</span></span>


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



<span data-ttu-id="84766-113">La cláusula RANK BY se aplica a la condición de búsqueda \_ inmediatamente anterior, especificando de forma eficaz un rango inferior o superior para las filas devueltas por esa condición de búsqueda que las filas devueltas por otra condición de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84766-113">The RANK BY clause is applied to the search\_condition immediately preceding it, effectively specifying a lower or higher rank for rows returned by that search condition than rows returned by another search condition.</span></span> <span data-ttu-id="84766-114">Los paréntesis que rodean la \_ condición de búsqueda son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="84766-114">The parentheses surrounding the search\_condition are required.</span></span> <span data-ttu-id="84766-115">Los paréntesis que rodean la especificación de rango son opcionales.</span><span class="sxs-lookup"><span data-stu-id="84766-115">The parentheses surrounding the rank specification are optional.</span></span>

<span data-ttu-id="84766-116">Se puede aplicar más de una cláusula RANK BY a una única condición.</span><span class="sxs-lookup"><span data-stu-id="84766-116">More than one RANK BY clause can be applied to a single condition.</span></span> <span data-ttu-id="84766-117">Puede incluir cláusulas RANK BY adicionales una tras otra mediante paréntesis.</span><span class="sxs-lookup"><span data-stu-id="84766-117">You can include additional RANK BY clauses one after the other using parentheses.</span></span>

> [!Note]  
> <span data-ttu-id="84766-118">Los predicados de texto completo devuelven valores de rango en el intervalo comprendido entre 0 y 1000.</span><span class="sxs-lookup"><span data-stu-id="84766-118">Full-text predicates return rank values in the range 0 to 1000.</span></span> <span data-ttu-id="84766-119">Los valores de rango para todos los documentos que coincidan con un predicado de texto no completo son 1000.</span><span class="sxs-lookup"><span data-stu-id="84766-119">Rank values for all documents matched by a non-full-text predicate are 1000.</span></span> <span data-ttu-id="84766-120">Las modificaciones en los valores de clasificación deben tener en cuenta esta información.</span><span class="sxs-lookup"><span data-stu-id="84766-120">Modifications to the rank values should take this information into account.</span></span>

 

<span data-ttu-id="84766-121">La \_ parte de la especificación de rango de la cláusula RANKBY identifica una o más funciones que se van a aplicar a los valores de clasificación.</span><span class="sxs-lookup"><span data-stu-id="84766-121">The rank\_specification portion of the RANKBY clause identifies one or more functions to apply to the rank values.</span></span> <span data-ttu-id="84766-122">La función WEIGHT aplica un multiplicador al valor de rango sin formato de una fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="84766-122">The WEIGHT function applies a multiplier to the raw rank value for a returned row.</span></span> <span data-ttu-id="84766-123">Cuanto menor sea el multiplicador, menor será el valor de rango resultante.</span><span class="sxs-lookup"><span data-stu-id="84766-123">The smaller the multiplier, the lower the resulting rank value.</span></span> <span data-ttu-id="84766-124">La función de coerción se puede usar para multiplicar, agregar o establecer un valor de rango específico para una fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="84766-124">The COERCION function can be used to multiply, add to, or set a specific rank value for a returned row.</span></span> <span data-ttu-id="84766-125">Cada especificación de rango puede incluir una función de peso o cero, y cero o más funciones de coerción.</span><span class="sxs-lookup"><span data-stu-id="84766-125">Each rank specification can include either zero or one WEIGHT function and zero or more COERCION functions.</span></span> <span data-ttu-id="84766-126">Si las funciones de peso y de coerción se incluyen en una cláusula RANK BY, la función WEIGHT debe ser primero.</span><span class="sxs-lookup"><span data-stu-id="84766-126">If both WEIGHT and COERCION functions are included in a RANK BY clause, the WEIGHT function must be first.</span></span>

## <a name="weight-function"></a><span data-ttu-id="84766-127">Función WEIGHT</span><span class="sxs-lookup"><span data-stu-id="84766-127">WEIGHT Function</span></span>

<span data-ttu-id="84766-128">La sintaxis de la función WEIGHT es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="84766-128">The syntax of the WEIGHT function is:</span></span>


```
WEIGHT ( <weight_multipler> ) 
```



<span data-ttu-id="84766-129">El multiplicador debe ser un decimal comprendido entre 0,001 y 1,000.</span><span class="sxs-lookup"><span data-stu-id="84766-129">The multiplier must be a decimal from 0.001 to 1.000.</span></span> <span data-ttu-id="84766-130">El valor de rango sin formato devuelto por el predicado de la condición de búsqueda se multiplica por el multiplicador de peso para establecer un nuevo valor de rango.</span><span class="sxs-lookup"><span data-stu-id="84766-130">The raw rank value returned by the search condition predicate is multiplied by the weight multiplier to set a new rank value.</span></span>

<span data-ttu-id="84766-131">En el ejemplo siguiente, la función WEIGHT proporciona documentos con la palabra "Theresa" en la System.Document. Campo LastAuthor mitad del valor de rango de los documentos con "Theresa" en el campo System. Author:</span><span class="sxs-lookup"><span data-stu-id="84766-131">In the following example, the WEIGHT function gives documents with the word "Theresa" in the System.Document.LastAuthor field half the rank value of documents with "Theresa" in the System.Author field:</span></span>


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> <span data-ttu-id="84766-132">Las características de ponderación de columnas de predicado CONTAINS y FREETEXT admiten un formato abreviado con un signo de dos puntos entre el término de búsqueda y el multiplicador ("software": 0,25).</span><span class="sxs-lookup"><span data-stu-id="84766-132">The CONTAINS and FREETEXT predicate column weighting features support a shorthand format using a colon between the search term and the multiplier ("software":0.25).</span></span> <span data-ttu-id="84766-133">La cláusula RANK BY no admite la forma abreviada.</span><span class="sxs-lookup"><span data-stu-id="84766-133">The RANK BY clause does not support the shortened form.</span></span>

 

<span data-ttu-id="84766-134">Existe una limitación al usar RANK BY WEIGHT: no funciona con cláusulas Contains que usan condiciones booleanas; por ejemplo, no se permite el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="84766-134">There is a limitation when using RANK BY WEIGHT: it does not work with CONTAINS clauses that use Boolean conditions; for example, the following example is not permitted:</span></span>


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a><span data-ttu-id="84766-135">Función de coerción</span><span class="sxs-lookup"><span data-stu-id="84766-135">COERCION Function</span></span>

<span data-ttu-id="84766-136">La función de conversión de rangos se puede usar para cambiar el valor de rango devuelto por la suma o la multiplicación o mediante la asignación de un valor específico.</span><span class="sxs-lookup"><span data-stu-id="84766-136">The rank coercion function can be used to change the returned rank value by addition or multiplication or by assigning it a specific value.</span></span>

<span data-ttu-id="84766-137">La sintaxis de la función de coerción es:</span><span class="sxs-lookup"><span data-stu-id="84766-137">The syntax of the COERCION function is:</span></span>


```
COERCION ( <coercion_operation> , <coercion_value> )
```



<span data-ttu-id="84766-138">El valor de coerción es un valor entero.</span><span class="sxs-lookup"><span data-stu-id="84766-138">The coercion value is an integer value.</span></span>

<span data-ttu-id="84766-139">En la tabla siguiente se describe la configuración de la operación de conversión disponible.</span><span class="sxs-lookup"><span data-stu-id="84766-139">The following table describes the available coercion operation settings.</span></span>



| <span data-ttu-id="84766-140">Operación de coerción</span><span class="sxs-lookup"><span data-stu-id="84766-140">Coercion operation</span></span> | <span data-ttu-id="84766-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="84766-141">Description</span></span>                                                                                    | <span data-ttu-id="84766-142">Intervalo de valores</span><span class="sxs-lookup"><span data-stu-id="84766-142">Value range</span></span>  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="84766-143">ABSOLUTE</span><span class="sxs-lookup"><span data-stu-id="84766-143">ABSOLUTE</span></span>           | <span data-ttu-id="84766-144">El valor de rango devuelto es el valor especificado en el valor de coerción.</span><span class="sxs-lookup"><span data-stu-id="84766-144">The rank value returned is the value specified in the coercion value.</span></span>                          | <span data-ttu-id="84766-145">de 0 a 1000</span><span class="sxs-lookup"><span data-stu-id="84766-145">0 to 1000</span></span>    |
| <span data-ttu-id="84766-146">ADD</span><span class="sxs-lookup"><span data-stu-id="84766-146">ADD</span></span>                | <span data-ttu-id="84766-147">El valor de rango devuelto es la suma del valor de rango sin formato y el valor de coerción especificado.</span><span class="sxs-lookup"><span data-stu-id="84766-147">The rank value returned is the sum of the raw rank value and the specified coercion value.</span></span>     | <span data-ttu-id="84766-148">de 0,001 a 1,0</span><span class="sxs-lookup"><span data-stu-id="84766-148">0.001 to 1.0</span></span> |
| <span data-ttu-id="84766-149">MULTIPLY</span><span class="sxs-lookup"><span data-stu-id="84766-149">MULTIPLY</span></span>           | <span data-ttu-id="84766-150">El valor de rango devuelto es el producto del valor de rango sin formato y el valor de coerción especificado.</span><span class="sxs-lookup"><span data-stu-id="84766-150">The rank value returned is the product of the raw rank value and the specified coercion value.</span></span> | <span data-ttu-id="84766-151">de 0,001 a 1,0</span><span class="sxs-lookup"><span data-stu-id="84766-151">0.001 to 1.0</span></span> |



 

 

> [!IMPORTANT]
> <span data-ttu-id="84766-152">La búsqueda solo puede devolver valores de rango en el intervalo de 0 a 1000.</span><span class="sxs-lookup"><span data-stu-id="84766-152">Search can return rank values only in the range of 0 to 1000.</span></span>

 

 

<span data-ttu-id="84766-153">En el ejemplo siguiente se usa la función de coerción para establecer todos los documentos con "Computer" en el título para que tengan un rango de 1000, mientras que se reduce en un trimestre el rango de documentos que contienen "Computer" y "software" en el título.</span><span class="sxs-lookup"><span data-stu-id="84766-153">The following example uses the COERCION function to set all documents with "computer" in the title to have a rank of 1000, while reducing by one-quarter the rank of documents containing both "computer" and "software" in the title.</span></span>


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



