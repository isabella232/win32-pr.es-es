---
description: Las columnas almacenadas en el índice de contenido pueden tener varios valores, y esas columnas multivalor se pueden comparar utilizando el predicado de comparación de matrices.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Comparaciones de varios valores (matriz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808930"
---
# <a name="multi-valued-array-comparisons"></a><span data-ttu-id="38f83-103">Comparaciones de varios valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="38f83-103">Multi-Valued (ARRAY) Comparisons</span></span>

<span data-ttu-id="38f83-104">Las columnas almacenadas en el índice de contenido pueden tener varios valores, y esas columnas multivalor se pueden comparar utilizando el predicado de comparación de matrices.</span><span class="sxs-lookup"><span data-stu-id="38f83-104">Columns stored in the content index can have multiple values, and those multivalued columns can be compared by using the ARRAY comparison predicate.</span></span>

<span data-ttu-id="38f83-105">El predicado de comparación de matrices tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="38f83-105">The ARRAY comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



<span data-ttu-id="38f83-106">Se devuelve un error si la referencia de columna no es una columna de varios valores.</span><span class="sxs-lookup"><span data-stu-id="38f83-106">An error is returned if the column reference is not a multivalued column.</span></span> <span data-ttu-id="38f83-107">El tipo de datos de la columna debe ser compatible con los elementos de la lista de comparación.</span><span class="sxs-lookup"><span data-stu-id="38f83-107">The column data type must be compatible with the elements of the comparison list.</span></span> <span data-ttu-id="38f83-108">Si es necesario, la referencia de columna se puede [convertir](-search-sql-castingdatacolumntype.md) en otro tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="38f83-108">If necessary, the column reference can be [cast](-search-sql-castingdatacolumntype.md) as another data type.</span></span>

<span data-ttu-id="38f83-109">El operador de comparación (COMP \_ OP) puede ser cualquiera de los operadores de comparación normales.</span><span class="sxs-lookup"><span data-stu-id="38f83-109">The comparison operator (comp\_op) can be any of the normal comparison operators.</span></span> <span data-ttu-id="38f83-110">En una comparación de varios valores, los operadores de comparación tienen significados ligeramente diferentes en función de si se usa un cuantificador.</span><span class="sxs-lookup"><span data-stu-id="38f83-110">In a multivalued comparison, the comparison operators have slightly different meanings depending on whether a quantifier is used.</span></span> <span data-ttu-id="38f83-111">Los cuantificadores identifican si se debe realizar una comparación con todos o algunos de los valores de la lista de comparación.</span><span class="sxs-lookup"><span data-stu-id="38f83-111">Quantifiers identify whether a comparison should be made against all or some of the values in the comparison list.</span></span> <span data-ttu-id="38f83-112">Las funciones de los operadores de comparación se proporcionan en las tablas que describen cada cuantificador (todos y algunos) más adelante en este documento.</span><span class="sxs-lookup"><span data-stu-id="38f83-112">The functions of the comparison operators are given in the tables describing each quantifier (ALL and SOME) later in this document.</span></span>

<span data-ttu-id="38f83-113">El valor después del operador especifica un único valor literal que se compara con todos los elementos de la columna de varios valores.</span><span class="sxs-lookup"><span data-stu-id="38f83-113">The value after the operator specifies a single literal value that is compared against all elements of the multivalued column.</span></span> <span data-ttu-id="38f83-114">Si algún elemento coincide con el valor, el predicado es true.</span><span class="sxs-lookup"><span data-stu-id="38f83-114">If any element matches the value, the predicate is true.</span></span>

<span data-ttu-id="38f83-115">La lista de comparación especifica una matriz de valores literales que se comparan con la columna de varios valores.</span><span class="sxs-lookup"><span data-stu-id="38f83-115">The comparison list specifies an array of literal values that are compared against the multivalued column.</span></span> <span data-ttu-id="38f83-116">La sintaxis de la lista de comparación es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="38f83-116">The syntax for the comparison list follows:</span></span>


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> <span data-ttu-id="38f83-117">Tenga en cuenta la sintaxis de la lista de comparación.</span><span class="sxs-lookup"><span data-stu-id="38f83-117">Be aware of the comparison list syntax.</span></span> <span data-ttu-id="38f83-118">El grupo de literales que conforman la lista de comparación debe ir entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="38f83-118">The group of literals that make up the comparison list must be surrounded by square brackets.</span></span> <span data-ttu-id="38f83-119">No incluya los elementos individuales de la lista de comparación entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="38f83-119">Do not surround individual elements of the comparison list by square brackets.</span></span> <span data-ttu-id="38f83-120">Por lo tanto, las matrices \[ 1 \] y \[ 1, 2, 3 \] son válidas, pero la matriz \[ 1 \[ , 2 \] \[ , 3 \] \] no.</span><span class="sxs-lookup"><span data-stu-id="38f83-120">Therefore, ARRAY \[1\] and ARRAY \[1,2,3\] are valid, but ARRAY \[1\[,2\]\[,3\]\] is not.</span></span>

 

<span data-ttu-id="38f83-121">El método que se usa para determinar si la comparación multivalor devuelve true o false lo especifica el cuantificador opcional.</span><span class="sxs-lookup"><span data-stu-id="38f83-121">The method used to determine whether the multivalued comparison returns true or false is specified by the optional quantifier.</span></span> <span data-ttu-id="38f83-122">En las secciones siguientes se describe cada cuantificador y cómo funciona cada operador de comparación cuando se utiliza el cuantificador.</span><span class="sxs-lookup"><span data-stu-id="38f83-122">The following sections describe each quantifier, and how each comparison operator works when the quantifier is used.</span></span>

## <a name="absent-quantifier"></a><span data-ttu-id="38f83-123">Cuantificador ausente</span><span class="sxs-lookup"><span data-stu-id="38f83-123">Absent Quantifier</span></span>

<span data-ttu-id="38f83-124">Si no se especifica ningún cuantificador, cada elemento en el lado izquierdo de la comparación se compara con el elemento de la misma posición del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-124">If no quantifier is specified, each element on the left side of the comparison is compared to the element in the same position on the right side.</span></span> <span data-ttu-id="38f83-125">La comparación comienza con el primer elemento de las matrices y progresa a través del último elemento.</span><span class="sxs-lookup"><span data-stu-id="38f83-125">The comparison begins with the first element in the arrays, and progresses through the last element.</span></span> <span data-ttu-id="38f83-126">Si todos los elementos del lado izquierdo son equivalentes a los elementos correspondientes del lado derecho, se usa el número de elementos de matriz para determinar qué matriz es mayor.</span><span class="sxs-lookup"><span data-stu-id="38f83-126">If all the elements on the left side are equivalent to the corresponding elements on the right side, the number of array elements is used to determine which array is greater.</span></span>

<span data-ttu-id="38f83-127">En la tabla siguiente se muestra la operación de los operadores de comparación cuando no se especifica ningún cuantificador y se proporciona una breve descripción de cada uno.</span><span class="sxs-lookup"><span data-stu-id="38f83-127">The following table shows the operation of the comparison operators when no quantifier is specified and provides a brief description of each.</span></span>



| <span data-ttu-id="38f83-128">Operator</span><span class="sxs-lookup"><span data-stu-id="38f83-128">Operator</span></span>       | <span data-ttu-id="38f83-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="38f83-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="38f83-130">' Igual a ' devuelve true cuando cada elemento del lado izquierdo tiene el mismo valor que el elemento de la derecha correspondiente, y ambas matrices tienen el mismo número de elementos.</span><span class="sxs-lookup"><span data-stu-id="38f83-130">'Equal to' returns true when each left-side element has the same value as the corresponding right-side element, and both arrays have the same number of elements.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="38f83-131">! = o <></span><span class="sxs-lookup"><span data-stu-id="38f83-131">!= or <></span></span> | <span data-ttu-id="38f83-132">' No es igual a ' devuelve true cuando uno o más elementos del lado izquierdo tienen valores que difieren de los elementos del lado derecho correspondientes, o cuando las matrices del lado izquierdo y derecho no tienen el mismo número de elementos.</span><span class="sxs-lookup"><span data-stu-id="38f83-132">'Not equal to' returns true when one or more left-side elements have values that differ from the corresponding right-side elements, or when the left-side and right-side arrays do not have the same number of elements.</span></span>                                                                                                                                                              |
| >           | <span data-ttu-id="38f83-133">' Mayor que ' devuelve true cuando el valor de cada elemento de la izquierda es mayor que el valor del elemento correspondiente del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-133">'Greater than' returns true when the value of each left-side element is greater than the value of the corresponding right-side element.</span></span> <span data-ttu-id="38f83-134">Si todos los valores de los elementos del lado izquierdo coinciden exactamente con los elementos del lado derecho correspondientes y la matriz del lado izquierdo tiene más elementos que la matriz del lado derecho, ' mayor que ' devuelve true.</span><span class="sxs-lookup"><span data-stu-id="38f83-134">If all the left-side element values exactly match the corresponding right-side elements and the left-side array has more elements than the right-side array, 'greater than' returns true.</span></span>                                                     |
| >=          | <span data-ttu-id="38f83-135">' Mayor o igual que ' devuelve true cuando el valor de cada elemento del lado izquierdo es mayor o igual que el valor del elemento correspondiente del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-135">'Greater than or equal to' returns true when the value of every left-side element is greater than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="38f83-136">Si todos los valores de los elementos del lado izquierdo son iguales o mayores que los elementos correspondientes del lado derecho y la matriz del lado izquierdo tiene los mismos elementos que la matriz del lado derecho, ' Greater Than ' devuelve true.</span><span class="sxs-lookup"><span data-stu-id="38f83-136">If all the left-side element values are equal to or greater than the corresponding right-side elements and the left-side array has the same or more elements than the right-side array, 'greater than' returns true.</span></span> |
| <           | <span data-ttu-id="38f83-137">' Less than ' devuelve true cuando el valor de cada elemento de la izquierda es menor que el valor del elemento correspondiente del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-137">'Less than' returns true when the value of each left-side element is less than the value of the corresponding right-side element.</span></span> <span data-ttu-id="38f83-138">' Menor que ' también devuelve true cuando el lado izquierdo tiene menos elementos que el lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-138">'Less than' also returns true when the left-side side has fewer elements than the right-side side.</span></span>                                                                                                                                                  |
| <=          | <span data-ttu-id="38f83-139">' Menor o igual que ' devuelve true cuando el valor de todos los elementos del lado izquierdo es menor o igual que el valor del elemento correspondiente del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-139">'Less than or equal to' returns true when the value of every left-side element is less than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="38f83-140">Si todos los valores de los elementos del lado izquierdo son iguales o menores que los elementos correspondientes del lado derecho y la matriz del lado izquierdo tiene el mismo o menos elementos que la matriz del lado derecho, ' mayor que ' devuelve true.</span><span class="sxs-lookup"><span data-stu-id="38f83-140">If all the left-side element values are equal to or less than the corresponding right-side elements and the left-side array has the same or fewer elements than the right-side array, 'greater than' returns true.</span></span>         |



 

## <a name="all-quantifier"></a><span data-ttu-id="38f83-141">Todos los cuantificadores</span><span class="sxs-lookup"><span data-stu-id="38f83-141">ALL Quantifier</span></span>

<span data-ttu-id="38f83-142">El cuantificador ALL especifica que cada elemento del lado izquierdo se compara con cada elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-142">The ALL quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="38f83-143">Para devolver true, la comparación debe ser true para cada elemento del lado izquierdo cuando se comparan con cada elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-143">To return true, the comparison must be true for each element on the left side when compared to every element on the right side.</span></span> <span data-ttu-id="38f83-144">El número de elementos de los lados izquierdo y derecho de la matriz no tiene ningún efecto en el resultado.</span><span class="sxs-lookup"><span data-stu-id="38f83-144">The number of elements in the left and right array sides has no effect on the result.</span></span>

<span data-ttu-id="38f83-145">En la tabla siguiente se muestra cómo cada operador de comparación funciona con el cuantificador todos.</span><span class="sxs-lookup"><span data-stu-id="38f83-145">The following table shows how each comparison operator functions with the ALL quantifier.</span></span>



| <span data-ttu-id="38f83-146">Operator</span><span class="sxs-lookup"><span data-stu-id="38f83-146">Operator</span></span>       | <span data-ttu-id="38f83-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="38f83-147">Description</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="38f83-148">' Igual a ' devuelve true cuando cada valor del elemento de la izquierda es igual que todos los valores de elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-148">'Equal to' returns true when each left-side element value is the same as every right-side element value.</span></span>                              |
| <span data-ttu-id="38f83-149">! = o <></span><span class="sxs-lookup"><span data-stu-id="38f83-149">!= or <></span></span> | <span data-ttu-id="38f83-150">' No es igual a ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es diferente de cualquiera de los valores de los elementos del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-150">'Not equal to' returns true when at least one of the left-side element values is different from any of the right-side element values.</span></span> |
| >           | <span data-ttu-id="38f83-151">' Mayor que ' devuelve true cuando cada valor del elemento de la izquierda es mayor que todos los valores de elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-151">'Greater than' returns true when each left-side element value is greater than every right-side element value.</span></span>                         |
| >=          | <span data-ttu-id="38f83-152">' Mayor o igual que ' devuelve true cuando cada valor del elemento de la izquierda es mayor o igual que cada valor de elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-152">'Greater than or equal to' returns true when each left-side element value is greater than or equal to every right-side element value.</span></span> |
| <           | <span data-ttu-id="38f83-153">' Less than ' devuelve true cuando cada valor de elemento del lado izquierdo es menor que cada valor de elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-153">'Less than' returns true when each left-side element value is less than every right-side element value.</span></span>                               |
| <=          | <span data-ttu-id="38f83-154">' Menor o igual que ' devuelve true cuando cada valor del elemento de la izquierda es menor o igual que cada valor de elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-154">'Less than or equal to' returns true when each left-side element value is less than or equal to every right-side element value.</span></span>       |



 

## <a name="some-or-any-quantifier"></a><span data-ttu-id="38f83-155">UN cuantificador (o cualquiera)</span><span class="sxs-lookup"><span data-stu-id="38f83-155">SOME (or ANY) Quantifier</span></span>

<span data-ttu-id="38f83-156">El cuantificador y el cuantificador ANY se pueden usar indistintamente.</span><span class="sxs-lookup"><span data-stu-id="38f83-156">The SOME quantifier and the ANY quantifier can be used interchangeably.</span></span> <span data-ttu-id="38f83-157">Al igual que el cuantificador ALL, el cuantificador SOME especifica que cada elemento del lado izquierdo se compara con cada elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-157">Like the ALL quantifier, the SOME quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="38f83-158">Para devolver true, la comparación debe ser true para al menos uno de los elementos del lado izquierdo cuando se comparan con cualquier elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-158">To return true, the comparison must be true for at least one of the elements on the left side when compared to any element on the right side.</span></span> <span data-ttu-id="38f83-159">El número de elementos de las matrices de la izquierda y la derecha no tiene ningún efecto en el resultado.</span><span class="sxs-lookup"><span data-stu-id="38f83-159">The number of elements on the left and right side arrays has no effect on the result.</span></span>

<span data-ttu-id="38f83-160">En la tabla siguiente se muestra cómo cada operador de comparación funciona con el cuantificador.</span><span class="sxs-lookup"><span data-stu-id="38f83-160">The following table shows how each comparison operator functions with the SOME quantifier.</span></span>



| <span data-ttu-id="38f83-161">Operator</span><span class="sxs-lookup"><span data-stu-id="38f83-161">Operator</span></span>       | <span data-ttu-id="38f83-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="38f83-162">Description</span></span>                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="38f83-163">' Equal to ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es igual que cualquiera de los valores de los elementos del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-163">'Equal to' returns true when at least one of the left-side element values is the same as any of the right-side element values.</span></span>                                  |
| <span data-ttu-id="38f83-164">! = o <></span><span class="sxs-lookup"><span data-stu-id="38f83-164">!= or <></span></span> | <span data-ttu-id="38f83-165">' No es igual a ' devuelve true cuando ninguno de los valores de los elementos del lado izquierdo es igual que ninguno de los valores de elemento del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-165">'Not equal to' returns true when none of the left-side element values is the same as any of the right-side element values.</span></span>                                      |
| >           | <span data-ttu-id="38f83-166">' Greater Than ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es mayor que uno de los valores de los elementos del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-166">'Greater than' returns true when at least one of the left-side element values is greater than any one of the right-side element values.</span></span>                         |
| >=          | <span data-ttu-id="38f83-167">' Mayor o igual que ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es mayor o igual que uno de los valores de los elementos del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-167">'Greater than or equal to' returns true when at least one of the left-side element values is greater than or equal to any one of the right-side element values.</span></span> |
| <           | <span data-ttu-id="38f83-168">' Less than ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es menor que uno de los valores de los elementos del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-168">'Less than' returns true when at least one of the left-side element values is less than any one of the right-side element values.</span></span>                               |
| <=          | <span data-ttu-id="38f83-169">' Menor o igual que ' devuelve true cuando al menos uno de los valores de los elementos del lado izquierdo es menor o igual que uno de los valores de los elementos del lado derecho.</span><span class="sxs-lookup"><span data-stu-id="38f83-169">'Less than or equal to' returns true when at least one of the left-side element values is less than or equal to any one of the right-side element values.</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="38f83-170">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="38f83-170">Examples</span></span>

<span data-ttu-id="38f83-171">En el ejemplo siguiente se comprueba si los documentos se encuentran en las categorías "Finance" o "Planning":</span><span class="sxs-lookup"><span data-stu-id="38f83-171">The following example checks whether documents are in the "Finance" or "Planning" categories:</span></span>


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



<span data-ttu-id="38f83-172">Las siguientes comparaciones se evalúan como true.</span><span class="sxs-lookup"><span data-stu-id="38f83-172">The following comparisons all evaluate true.</span></span> <span data-ttu-id="38f83-173">Recuerde que, en el uso real, la sintaxis de consulta de búsqueda requiere que el lado izquierdo sea una propiedad, no un valor literal.</span><span class="sxs-lookup"><span data-stu-id="38f83-173">Remember that in actual use, the search query syntax requires the left side to be a property, not a literal value.</span></span>


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a><span data-ttu-id="38f83-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38f83-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="38f83-175">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="38f83-175">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38f83-176">LIKE (predicado)</span><span class="sxs-lookup"><span data-stu-id="38f83-176">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="38f83-177">Comparación de valores literales</span><span class="sxs-lookup"><span data-stu-id="38f83-177">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="38f83-178">Predicado NULL</span><span class="sxs-lookup"><span data-stu-id="38f83-178">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="38f83-179">**Vista**</span><span class="sxs-lookup"><span data-stu-id="38f83-179">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38f83-180">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="38f83-180">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="38f83-181">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="38f83-181">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



