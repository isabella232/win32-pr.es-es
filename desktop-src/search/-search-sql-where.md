---
description: Las condiciones que determinan si un documento se incluye en los resultados devueltos por la consulta se especifican mediante la cláusula WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Cláusula WHERE (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686618"
---
# <a name="where-clause-windows-search"></a><span data-ttu-id="51d96-103">Cláusula WHERE (búsqueda de Windows)</span><span class="sxs-lookup"><span data-stu-id="51d96-103">WHERE Clause (Windows Search)</span></span>

<span data-ttu-id="51d96-104">Las condiciones que determinan si un documento se incluye en los resultados devueltos por la consulta se especifican mediante la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="51d96-104">The conditions that determine whether a document is included in the results returned by the query are specified by the WHERE clause.</span></span> <span data-ttu-id="51d96-105">En el nivel más alto, hay dos partes de la sintaxis de la cláusula WHERE:</span><span class="sxs-lookup"><span data-stu-id="51d96-105">At the highest level, there are two parts to the WHERE clause syntax:</span></span>


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



<span data-ttu-id="51d96-106">La parte opcional <\_ alias de grupo> de la cláusula simplifica las consultas complejas asignando un alias a un grupo de una o varias columnas.</span><span class="sxs-lookup"><span data-stu-id="51d96-106">The optional <group\_alias> portion of the clause simplifies complex queries by assigning an alias to a group of one or more columns.</span></span> <span data-ttu-id="51d96-107">Esto puede mejorar la legibilidad de las consultas complejas que buscan la misma información en varias columnas especificadas por las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="51d96-107">This can improve the readability of complex queries that search for the same information across multiple columns specified by URLs.</span></span> <span data-ttu-id="51d96-108">Para obtener más información acerca de los alias de grupo, consulte [con el predicado de alias de grupo](-search-sql-with-as.md).</span><span class="sxs-lookup"><span data-stu-id="51d96-108">For more information about group aliases, see [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).</span></span>

<span data-ttu-id="51d96-109">La <search condition> parte de la cláusula WHERE es uno o más predicados de búsqueda que especifican los criterios de coincidencia de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51d96-109">The <search condition> portion of the WHERE clause is one or more search predicates that specify matching criteria for the search.</span></span> <span data-ttu-id="51d96-110">Los predicados de búsqueda son expresiones que imponen algún hecho sobre algún valor.</span><span class="sxs-lookup"><span data-stu-id="51d96-110">Search predicates are expressions that assert some fact about some value.</span></span>

<span data-ttu-id="51d96-111">El resultado de una condición de búsqueda es un valor booleano, **true** si el documento cumple las condiciones de búsqueda especificadas, o bien **false** si no lo hace.</span><span class="sxs-lookup"><span data-stu-id="51d96-111">The result of a search condition is a Boolean value, either **TRUE** if the document meets the specified search conditions, or **FALSE** if it does not.</span></span> <span data-ttu-id="51d96-112">Si el resultado es **true**, se devuelve el documento.</span><span class="sxs-lookup"><span data-stu-id="51d96-112">If the result is **TRUE**, the document is returned.</span></span> <span data-ttu-id="51d96-113">Si el resultado es **false**, no se devuelve el documento.</span><span class="sxs-lookup"><span data-stu-id="51d96-113">If the result is **FALSE**, the document is not returned.</span></span> <span data-ttu-id="51d96-114">A los documentos devueltos en una consulta de búsqueda de Microsoft Windows se les asignan valores de clasificación según el grado de coincidencia de las condiciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51d96-114">Documents returned in a Microsoft Windows Search query are assigned rank values according to how well they match the search conditions.</span></span> <span data-ttu-id="51d96-115">Cada una de las condiciones de búsqueda de consultas puede incluir una cláusula [RANKBY](-search-sql-rankby.md) que admite la modificación de los valores de rango devueltos.</span><span class="sxs-lookup"><span data-stu-id="51d96-115">Each of the query search conditions can include a [RANKBY](-search-sql-rankby.md) clause that supports modifying the returned rank values.</span></span>

<span data-ttu-id="51d96-116">La [función ReuseWhere](-search-sql-reusewhere.md) hace que varias consultas que usan las mismas condiciones de búsqueda sean más eficaces.</span><span class="sxs-lookup"><span data-stu-id="51d96-116">The [ReuseWhere function](-search-sql-reusewhere.md) makes multiple queries that use the some of the same search conditions more efficient.</span></span> <span data-ttu-id="51d96-117">La cláusula WHERE de una consulta especifica el conjunto de elementos que coinciden en una consulta.</span><span class="sxs-lookup"><span data-stu-id="51d96-117">The WHERE clause in a query specifies the set of items that match in a query.</span></span> <span data-ttu-id="51d96-118">Las consultas posteriores pueden compartir el trabajo realizado para la evaluación anterior mediante el uso de la función ReuseWhere en la cláusula WHERE de la nueva consulta.</span><span class="sxs-lookup"><span data-stu-id="51d96-118">Subsequent queries can share the work performed for the previous evalution by using the ReuseWhere function in the new query WHERE clause.</span></span>

## <a name="search-predicates"></a><span data-ttu-id="51d96-119">Predicados de búsqueda</span><span class="sxs-lookup"><span data-stu-id="51d96-119">Search Predicates</span></span>

<span data-ttu-id="51d96-120">Una condición de búsqueda consta de uno o varios predicados o condiciones de búsqueda que describen lo que busca el usuario (por ejemplo, donde System. DateCreated > ' 2006-04-19 ').</span><span class="sxs-lookup"><span data-stu-id="51d96-120">A search condition consists of one or more predicates or search conditions that describe what the user is searching for (for example, WHERE System.DateCreated >'2006-04-19').</span></span> <span data-ttu-id="51d96-121">Los predicados de búsqueda se pueden combinar mediante los operadores lógicos **and**, **or** o **Not**.</span><span class="sxs-lookup"><span data-stu-id="51d96-121">Search predicates can be combined using the logical operators **AND**, **OR**, or **NOT**.</span></span> <span data-ttu-id="51d96-122">El operador unario opcional **no** se puede usar solo con **y** y solo para negar el valor lógico de un predicado o una condición de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51d96-122">The optional unary operator **NOT** can be used only with **AND** and only to negate the logical value of a predicate or search condition.</span></span> <span data-ttu-id="51d96-123">Puede usar paréntesis para agrupar y anidar términos lógicos.</span><span class="sxs-lookup"><span data-stu-id="51d96-123">You can use parentheses to group and nest logical terms.</span></span>

<span data-ttu-id="51d96-124">En la tabla siguiente se muestra el orden de prioridad de los operadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="51d96-124">The following table shows the order of precedence for the logical operators.</span></span>



| <span data-ttu-id="51d96-125">Orden (precedencia)</span><span class="sxs-lookup"><span data-stu-id="51d96-125">Order (precedence)</span></span> | <span data-ttu-id="51d96-126">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="51d96-126">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="51d96-127">Primero (más alto)</span><span class="sxs-lookup"><span data-stu-id="51d96-127">First (highest)</span></span>    | <span data-ttu-id="51d96-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="51d96-128">**NOT**</span></span>          |
| <span data-ttu-id="51d96-129">Segundo</span><span class="sxs-lookup"><span data-stu-id="51d96-129">Second</span></span>             | <span data-ttu-id="51d96-130">**AND**</span><span class="sxs-lookup"><span data-stu-id="51d96-130">**AND**</span></span>          |
| <span data-ttu-id="51d96-131">Tercer (el más bajo)</span><span class="sxs-lookup"><span data-stu-id="51d96-131">Third (lowest)</span></span>     | <span data-ttu-id="51d96-132">**OR**</span><span class="sxs-lookup"><span data-stu-id="51d96-132">**OR**</span></span>           |



 

<span data-ttu-id="51d96-133">Los operadores lógicos del mismo tipo son asociativos y no hay ningún orden de cálculo especificado.</span><span class="sxs-lookup"><span data-stu-id="51d96-133">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="51d96-134">Por ejemplo, (A **y** b) **y** (C **y** d) se pueden calcular (a **y** d) **y** (B **y** C) sin ningún cambio en el resultado lógico.</span><span class="sxs-lookup"><span data-stu-id="51d96-134">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (A **AND** D) **AND** (B **AND** C) with no change in the logical result.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="51d96-135">Incorrecto: donde **no** contiene (' equipo ')</span><span class="sxs-lookup"><span data-stu-id="51d96-135">Incorrect: WHERE **NOT** CONTAINS ('computer')</span></span>
>
> <span data-ttu-id="51d96-136">Correcto: donde contiene (' software ') **y no** contiene (' equipo ')</span><span class="sxs-lookup"><span data-stu-id="51d96-136">Correct: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')</span></span>

 

<span data-ttu-id="51d96-137">En las consultas complejas, es posible que desee poner más énfasis en las coincidencias en algunas columnas que en otras.</span><span class="sxs-lookup"><span data-stu-id="51d96-137">In complex queries, you might want to place more emphasis on matches in some columns than in others.</span></span> <span data-ttu-id="51d96-138">Por ejemplo, al buscar documentos que analizan "diseño de software", es más probable que buscar el término de búsqueda en el título del documento sea una buena coincidencia que buscar las palabras individuales en el texto del documento.</span><span class="sxs-lookup"><span data-stu-id="51d96-138">For example, when searching for documents that discuss "software design", finding the search term in the document title is more likely to be a good match than finding the individual words in the text of the document.</span></span> <span data-ttu-id="51d96-139">Para influir en la clasificación de los documentos de esta manera, el lenguaje de consulta de Microsoft Windows Search admite la ponderación de las condiciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51d96-139">To influence the ranking of documents in this manner, the Microsoft Windows Search query language supports weighting the search conditions.</span></span> <span data-ttu-id="51d96-140">Para obtener más información acerca de la ponderación de las columnas, vea [Contains](-search-sql-contains.md) Predicate y [FREETEXT Predicate](-search-sql-freetext.md).</span><span class="sxs-lookup"><span data-stu-id="51d96-140">For more information about column weighting, see [CONTAINS Predicate](-search-sql-contains.md) and [FREETEXT Predicate](-search-sql-freetext.md).</span></span>

<span data-ttu-id="51d96-141">Hay tres grupos de predicados de búsqueda en Windows Search: búsquedas de texto completo, de texto no completo y de profundidad de carpeta.</span><span class="sxs-lookup"><span data-stu-id="51d96-141">There are three groups of search predicates in Windows Search: full-text, non-full-text, and folder depth searches.</span></span> <span data-ttu-id="51d96-142">Los predicados de búsqueda de texto completo suelen coincidir con el significado del contenido, el título y otras columnas, y admiten la coincidencia lingüística (por ejemplo, formas de palabras, frases y búsqueda de proximidad).</span><span class="sxs-lookup"><span data-stu-id="51d96-142">Full-text search predicates typically match the meaning of the content, title, and other columns, and support linguistic matching (for example, alternative word forms, phrases, and proximity searching).</span></span> <span data-ttu-id="51d96-143">En cambio, los predicados de búsqueda no de texto completo coinciden con el valor de las columnas especificadas y no incluyen ningún procesamiento lingüístico especial, pero en varios casos ofrecen coincidencia de patrones basada en caracteres.</span><span class="sxs-lookup"><span data-stu-id="51d96-143">In contrast, non-full-text search predicates match the value of the specified columns and do not include any special linguistic processing, but in several cases offer character-based pattern matching.</span></span> <span data-ttu-id="51d96-144">Los predicados de profundidad de carpeta restringen el ámbito de búsqueda a una ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="51d96-144">Folder depth predicates restrict the search scope to a specified path.</span></span>

> [!Note]  
> <span data-ttu-id="51d96-145">Si la consulta devuelve un documento porque un predicado que no es de texto completo se evalúa como **true** para ese documento, el valor de rango se calcula como 1000.</span><span class="sxs-lookup"><span data-stu-id="51d96-145">If the query returns a document because a non-full-text predicate evaluates to **TRUE** for that document, the rank value is calculated as 1000.</span></span> <span data-ttu-id="51d96-146">El uso de la [función de conversión de rangos](-search-sql-rankby.md) puede modificar el valor de clasificación.</span><span class="sxs-lookup"><span data-stu-id="51d96-146">Using the [rank coercion function](-search-sql-rankby.md) can modify the rank value.</span></span>

 

<span data-ttu-id="51d96-147">En las tablas siguientes se describen los predicados de búsqueda de texto completo, no completo y de profundidad de carpeta.</span><span class="sxs-lookup"><span data-stu-id="51d96-147">The following tables describe the full-text, non-full-text, and folder depth search predicates.</span></span>



| <span data-ttu-id="51d96-148">Predicado de texto completo</span><span class="sxs-lookup"><span data-stu-id="51d96-148">Full-text predicate</span></span>                  | <span data-ttu-id="51d96-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="51d96-149">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d96-150">CONTAINS</span><span class="sxs-lookup"><span data-stu-id="51d96-150">CONTAINS</span></span>](-search-sql-contains.md) | <span data-ttu-id="51d96-151">Admite búsquedas complejas de términos en columnas de texto de documento (por ejemplo, título, contenido).</span><span class="sxs-lookup"><span data-stu-id="51d96-151">Supports complex searches for terms in document text columns (for example, title, contents).</span></span> <span data-ttu-id="51d96-152">Puede buscar formas derivadas de los términos de búsqueda, probar la proximidad de los términos y realizar comparaciones lógicas.</span><span class="sxs-lookup"><span data-stu-id="51d96-152">Can search for inflected forms of the search terms, test for proximity of the terms, and perform logical comparisons.</span></span> <span data-ttu-id="51d96-153">Los términos de búsqueda pueden incluir caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="51d96-153">Search terms can include wildcard characters.</span></span> |
| [<span data-ttu-id="51d96-154">FREETEXT</span><span class="sxs-lookup"><span data-stu-id="51d96-154">FREETEXT</span></span>](-search-sql-freetext.md) | <span data-ttu-id="51d96-155">Busca documentos que coincidan con el significado de la frase de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51d96-155">Searches for documents that match the meaning of the search phrase.</span></span> <span data-ttu-id="51d96-156">Las palabras relacionadas y las frases similares coincidirán, con la columna de rango calculada en función del grado de coincidencia del documento con la frase de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="51d96-156">Related words and similar phrases will match, with the rank column calculated based on how closely the document matches the search phrase.</span></span> <span data-ttu-id="51d96-157">Los términos de búsqueda no pueden incluir caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="51d96-157">Search terms cannot include wildcard characters.</span></span>  |



 



| <span data-ttu-id="51d96-158">Predicado de texto no completo</span><span class="sxs-lookup"><span data-stu-id="51d96-158">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="51d96-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="51d96-159">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d96-160">LIKE</span><span class="sxs-lookup"><span data-stu-id="51d96-160">LIKE</span></span>](-search-sql-like.md)                                               | <span data-ttu-id="51d96-161">Los valores de columna se comparan usando la coincidencia de patrones simple con caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="51d96-161">Column values are compared using simple pattern matching with wildcard characters.</span></span>                                                                                                    |
| [<span data-ttu-id="51d96-162">Comparación de valores literales</span><span class="sxs-lookup"><span data-stu-id="51d96-162">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="51d96-163">Los valores de columna se comparan con cadenas, fechas, marcas de tiempo, números y otros valores literales.</span><span class="sxs-lookup"><span data-stu-id="51d96-163">Column values are compared against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="51d96-164">Este predicado admite igualdad y desigualdades, como mayor que y menor que.</span><span class="sxs-lookup"><span data-stu-id="51d96-164">This predicate supports equality and inequalities such as greater than and less than.</span></span> |
| [<span data-ttu-id="51d96-165">Comparaciones de varios valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="51d96-165">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="51d96-166">Las columnas con varios valores se comparan con una matriz de literales de varios valores.</span><span class="sxs-lookup"><span data-stu-id="51d96-166">Multivalued columns are compared against a multivalued array of literals.</span></span>                                                                                                             |
| [<span data-ttu-id="51d96-167">NULL</span><span class="sxs-lookup"><span data-stu-id="51d96-167">NULL</span></span>](-search-sql-null.md)                                               | <span data-ttu-id="51d96-168">Los valores de columna no definidos para el documento se pueden detectar mediante el predicado **null** .</span><span class="sxs-lookup"><span data-stu-id="51d96-168">Column values that are undefined for the document can be detected by using the **NULL** predicate.</span></span>                                                                                    |



 



| <span data-ttu-id="51d96-169">Profundidad de carpeta</span><span class="sxs-lookup"><span data-stu-id="51d96-169">Folder Depth</span></span>                             | <span data-ttu-id="51d96-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="51d96-170">Description</span></span>                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51d96-171">ID</span><span class="sxs-lookup"><span data-stu-id="51d96-171">SCOPE</span></span>](-search-sql-folderdepth.md)     | <span data-ttu-id="51d96-172">Realiza un recorrido profundo de la ruta de acceso especificada, incluida la carpeta específica y todas las subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="51d96-172">Performs a deep traversal of the specified path, including the specific folder and all subfolders.</span></span> |
| [<span data-ttu-id="51d96-173">Active</span><span class="sxs-lookup"><span data-stu-id="51d96-173">DIRECTORY</span></span>](-search-sql-folderdepth.md) | <span data-ttu-id="51d96-174">Realiza un recorrido superficial de la ruta de acceso especificada, buscando solo en la carpeta específica.</span><span class="sxs-lookup"><span data-stu-id="51d96-174">Performs a shallow traversal of the specified path, searching only the specific folder.</span></span>            |



 

## <a name="examples"></a><span data-ttu-id="51d96-175">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51d96-175">Examples</span></span>

<span data-ttu-id="51d96-176">Para obtener ejemplos de la cláusula WHERE, vea los temas de predicado individuales vinculados en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="51d96-176">For examples of the WHERE clause, see the individual predicate topics linked in the preceding table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51d96-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="51d96-177">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="51d96-178">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="51d96-178">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="51d96-179">ReuseWhere función)</span><span class="sxs-lookup"><span data-stu-id="51d96-179">ReuseWhere function</span></span>](-search-sql-reusewhere.md)
</dt> <dt>

[<span data-ttu-id="51d96-180">Propiedades del conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="51d96-180">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> <dt>

[<span data-ttu-id="51d96-181">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="51d96-181">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="51d96-182">Información general de la sintaxis de búsqueda de SQL</span><span class="sxs-lookup"><span data-stu-id="51d96-182">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="51d96-183">CON el predicado de alias de grupo AS</span><span class="sxs-lookup"><span data-stu-id="51d96-183">WITH -- AS Group Alias Predicate</span></span>](-search-sql-with-as.md)
</dt> <dt>

[<span data-ttu-id="51d96-184">Predicados de ámbito y directorio</span><span class="sxs-lookup"><span data-stu-id="51d96-184">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> <dt>

[<span data-ttu-id="51d96-185">RANK BY (cláusula)</span><span class="sxs-lookup"><span data-stu-id="51d96-185">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

<span data-ttu-id="51d96-186">**Vista**</span><span class="sxs-lookup"><span data-stu-id="51d96-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="51d96-187">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="51d96-187">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="51d96-188">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="51d96-188">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



