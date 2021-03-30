---
description: El predicado CONTAINS forma parte de la cláusula WHERE y admite la búsqueda de palabras y frases en columnas de texto.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: Predicado CONTAINS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907743"
---
# <a name="contains-predicate"></a><span data-ttu-id="735da-103">Predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="735da-103">CONTAINS Predicate</span></span>

<span data-ttu-id="735da-104">El predicado CONTAINS forma parte de la cláusula WHERE y admite la búsqueda de palabras y frases en columnas de texto.</span><span class="sxs-lookup"><span data-stu-id="735da-104">The CONTAINS predicate is part of the WHERE clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="735da-105">El predicado CONTAINS tiene características para buscar palabras coincidentes, buscar coincidencias de formas con inflexión de palabras, buscar mediante caracteres comodín y realizar búsquedas con proximidad.</span><span class="sxs-lookup"><span data-stu-id="735da-105">The CONTAINS predicate has features for matching words, matching inflectional forms of words, searching using wildcard characters, and searching using proximity.</span></span> <span data-ttu-id="735da-106">También puede aplicar pesos en un predicado CONTAINS para establecer la importancia de las columnas en las que se encuentra el término de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="735da-106">You can also apply weights in a CONTAINS predicate to set the importance of the columns where the search term is found.</span></span> <span data-ttu-id="735da-107">El predicado CONTAINS es más adecuado para las coincidencias exactas, al contrario que el predicado [FREETEXT](-search-sql-freetext.md) , que es más adecuado para buscar documentos que contengan combinaciones de las palabras de búsqueda distribuidas en toda la columna.</span><span class="sxs-lookup"><span data-stu-id="735da-107">The CONTAINS predicate is better suited for exact matches, in contrast to the [FREETEXT](-search-sql-freetext.md) predicate, which is better suited to finding documents containing combinations of the search words spread throughout the column.</span></span> <span data-ttu-id="735da-108">Las búsquedas no distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="735da-108">Searches are not case-sensitive.</span></span>

<span data-ttu-id="735da-109">A continuación se muestra la sintaxis básica del predicado CONTAINS:</span><span class="sxs-lookup"><span data-stu-id="735da-109">The following is the basic syntax of the CONTAINS predicate:</span></span>

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

<span data-ttu-id="735da-110">La \_ referencia de columna fulltext es opcional.</span><span class="sxs-lookup"><span data-stu-id="735da-110">The fulltext\_column reference is optional.</span></span> <span data-ttu-id="735da-111">Con él, puede limitar la búsqueda a una sola columna o a un grupo de columnas en el que se prueba el predicado CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="735da-111">With it, you can limit the search to a single column or a column group against which the CONTAINS predicate is tested.</span></span> <span data-ttu-id="735da-112">Cuando la columna fulltext se especifica como "ALL" o " \* ", se busca en todas las propiedades de texto indizadas.</span><span class="sxs-lookup"><span data-stu-id="735da-112">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="735da-113">Aunque no es necesario que la columna sea una propiedad de texto, los resultados podrían no tener sentido si la columna es algún otro tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="735da-113">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="735da-114">El nombre de la columna puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado, y debe separarlo de la condición mediante una coma.</span><span class="sxs-lookup"><span data-stu-id="735da-114">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="735da-115">Si no se especifica ninguna columna de texto completo, se usa la columna System. Search. Contents, que es el cuerpo del documento.</span><span class="sxs-lookup"><span data-stu-id="735da-115">If no fulltext column is specified, the System.Search.Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="735da-116">La parte LCID del predicado especifica la configuración regional de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="735da-116">The LCID portion of the predicate specifies the search locale.</span></span> <span data-ttu-id="735da-117">Esto indica al motor de búsqueda que utilice el separador de palabras y las formas con inflexión adecuadas para la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="735da-117">This instructs the search engine to use the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="735da-118">Para especificar la configuración regional, proporcione el identificador de código de idioma (LCID) estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="735da-118">To specify the locale, provide the Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="735da-119">Por ejemplo, 1033 es el LCID para Estados Unidos-English.</span><span class="sxs-lookup"><span data-stu-id="735da-119">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="735da-120">Coloque el LCID como el último elemento dentro de los paréntesis de la cláusula Contains.</span><span class="sxs-lookup"><span data-stu-id="735da-120">Place the LCID as the last item inside the parentheses of the CONTAINS clause.</span></span> <span data-ttu-id="735da-121">Para obtener información importante acerca de la búsqueda y los lenguajes, consulte [uso de búsquedas localizadas](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="735da-121">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="735da-122">La configuración regional de búsqueda predeterminada es la configuración regional predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="735da-122">The default search locale is the system default locale.</span></span>

<span data-ttu-id="735da-123">La parte de la condición Contains \_ debe ir entre comillas simples para palabras individuales o comillas dobles para frases, y consta de uno o varios términos de búsqueda de contenido que se combinan mediante los operadores lógicos **and** u **or**.</span><span class="sxs-lookup"><span data-stu-id="735da-123">The contains\_condition portion must be enclosed in single quotation marks for single words or double quotation marks for phrases, and consists of one or more content search terms that are combined using the logical operators **AND** or **OR**.</span></span> <span data-ttu-id="735da-124">Puede usar el operador unario opcional **no** después de un operador **and** para negar el valor lógico de un término de búsqueda de contenido.</span><span class="sxs-lookup"><span data-stu-id="735da-124">You can use the optional unary operator **NOT** after an **AND** operator to negate the logical value of a content search term.</span></span>

> [!NOTE]  
> <span data-ttu-id="735da-125">El operador **Not** solo puede aparecer después **de y**.</span><span class="sxs-lookup"><span data-stu-id="735da-125">The **NOT** operator can occur only after **AND**.</span></span> <span data-ttu-id="735da-126">No se puede usar el operador **Not** si solo hay una condición de coincidencia o después del operador **or** .</span><span class="sxs-lookup"><span data-stu-id="735da-126">You cannot use the **NOT** operator if there is only one match condition, or after the **OR** operator.</span></span>

<span data-ttu-id="735da-127">Puede usar paréntesis para agrupar y anidar términos de búsqueda de contenido.</span><span class="sxs-lookup"><span data-stu-id="735da-127">You can use parentheses to group and nest content search terms.</span></span> <span data-ttu-id="735da-128">En la tabla siguiente se describe el orden de prioridad de los operadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="735da-128">The following table describes the order of precedence for the logical operators.</span></span>

| <span data-ttu-id="735da-129">Orden (precedencia)</span><span class="sxs-lookup"><span data-stu-id="735da-129">Order (precedence)</span></span> | <span data-ttu-id="735da-130">Operador lógico</span><span class="sxs-lookup"><span data-stu-id="735da-130">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="735da-131">Primero (más alto)</span><span class="sxs-lookup"><span data-stu-id="735da-131">First (highest)</span></span>    | <span data-ttu-id="735da-132">**NOT**</span><span class="sxs-lookup"><span data-stu-id="735da-132">**NOT**</span></span>          |
| <span data-ttu-id="735da-133">Segundo</span><span class="sxs-lookup"><span data-stu-id="735da-133">Second</span></span>             | <span data-ttu-id="735da-134">**AND**</span><span class="sxs-lookup"><span data-stu-id="735da-134">**AND**</span></span>          |
| <span data-ttu-id="735da-135">Tercer (el más bajo)</span><span class="sxs-lookup"><span data-stu-id="735da-135">Third (lowest)</span></span>     | <span data-ttu-id="735da-136">**OR**</span><span class="sxs-lookup"><span data-stu-id="735da-136">**OR**</span></span>           |

<span data-ttu-id="735da-137">Los operadores lógicos del mismo tipo son asociativos y no hay ningún orden de cálculo especificado.</span><span class="sxs-lookup"><span data-stu-id="735da-137">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="735da-138">Por ejemplo, (A **y** B) **y** (C **y** d) se pueden calcular (B **y** C) **y** (A **y** D) sin ningún cambio en el resultado lógico.</span><span class="sxs-lookup"><span data-stu-id="735da-138">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (B **AND** C) **AND** (A **AND** D) with no change in the logical result.</span></span>

<span data-ttu-id="735da-139">En la tabla siguiente se describen los tipos de términos de búsqueda de contenido.</span><span class="sxs-lookup"><span data-stu-id="735da-139">The following table describes the types of content search terms.</span></span>

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="735da-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="735da-140">Type</span></span></th>
<th><span data-ttu-id="735da-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="735da-141">Description</span></span></th>
<th><span data-ttu-id="735da-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="735da-142">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="735da-143">Word</span><span class="sxs-lookup"><span data-stu-id="735da-143">Word</span></span></td>
<td><span data-ttu-id="735da-144">Una sola palabra sin espacios u otros signos de puntuación.</span><span class="sxs-lookup"><span data-stu-id="735da-144">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="735da-145">No es necesario incluir comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="735da-145">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="735da-146">Frase</span><span class="sxs-lookup"><span data-stu-id="735da-146">Phrase</span></span></td>
<td><span data-ttu-id="735da-147">Varias palabras o espacios incluidos.</span><span class="sxs-lookup"><span data-stu-id="735da-147">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="735da-148">Wildcard (Carácter comodín)</span><span class="sxs-lookup"><span data-stu-id="735da-148">Wildcard</span></span></td>
<td><span data-ttu-id="735da-149">Palabras o frases con el asterisco (\*) agregados al final.</span><span class="sxs-lookup"><span data-stu-id="735da-149">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="735da-150">Para obtener más información, vea <a href="-search-sql-wildcards.md">usar caracteres comodín en el predicado CONtains</a>.</span><span class="sxs-lookup"><span data-stu-id="735da-150">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="735da-151">Columna de texto completo</span><span class="sxs-lookup"><span data-stu-id="735da-151">Full-text Column</span></span></td>
<td><span data-ttu-id="735da-152">Nombre de la columna de propiedad con la que se va a hacer coincidir la consulta restante.</span><span class="sxs-lookup"><span data-stu-id="735da-152">A property column name against which to match the remaining query.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="735da-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="735da-153">Boolean</span></span></td>
<td><span data-ttu-id="735da-154">Palabras, frases y cadenas comodín combinadas mediante los operadores booleanos <strong>and</strong>, <strong>or</strong>o <strong>Not</strong>.</span><span class="sxs-lookup"><span data-stu-id="735da-154">Words, phrases, and wildcard strings combined by using the Boolean operators <strong>AND</strong>, <strong>OR</strong>, or <strong>NOT</strong>.</span></span> <span data-ttu-id="735da-155">Incluya los términos booleanos entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="735da-155">Enclose the Boolean terms in double quotation marks.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="735da-156">Near</span><span class="sxs-lookup"><span data-stu-id="735da-156">Near</span></span></td>
<td><span data-ttu-id="735da-157">Palabras, frases o caracteres comodín separados por la función NEAR.</span><span class="sxs-lookup"><span data-stu-id="735da-157">Words, phrases, or wildcards separated by the function NEAR.</span></span> <span data-ttu-id="735da-158">Para obtener más información, vea <a href="-search-sql-near.md">Near term</a>.</span><span class="sxs-lookup"><span data-stu-id="735da-158">For more information, see <a href="-search-sql-near.md">NEAR Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="735da-159">FormsOf</span><span class="sxs-lookup"><span data-stu-id="735da-159">FormsOf</span></span></td>
<td><span data-ttu-id="735da-160">Coincide con una palabra y con las versiones con inflexión de esa palabra.</span><span class="sxs-lookup"><span data-stu-id="735da-160">Matches a word and the inflectional versions of that word.</span></span> <span data-ttu-id="735da-161">Para obtener más información, vea el <a href="-search-sql-formsof.md">término FORMSOF</a>.</span><span class="sxs-lookup"><span data-stu-id="735da-161">For more information, see <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="735da-162">IsAbout</span><span class="sxs-lookup"><span data-stu-id="735da-162">IsAbout</span></span></td>
<td><span data-ttu-id="735da-163">Combina los resultados de búsqueda de coincidencias en varios términos de palabras, frases o caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="735da-163">Combines matching results over multiple word, phrase, or wildcard search terms.</span></span> <span data-ttu-id="735da-164">Opcionalmente, se puede ponderar cada término de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="735da-164">Each search term can optionally be weighted.</span></span> <span data-ttu-id="735da-165">Opcionalmente, puede especificar el método de cálculo de clasificación, que combina los pesos y el número de elementos que coinciden con el documento.</span><span class="sxs-lookup"><span data-stu-id="735da-165">You can optionally specify the rank calculation method, which combines the weights and how many of the items the document matches.</span></span> <span data-ttu-id="735da-166">Para obtener más información, consulte <a href="-search-sql-isabout.md">isabout term</a>.</span><span class="sxs-lookup"><span data-stu-id="735da-166">For more information, see <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

<span data-ttu-id="735da-167">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="735da-167">This section includes the following topics:</span></span>

- [<span data-ttu-id="735da-168">Usar caracteres comodín en el predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="735da-168">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
- [<span data-ttu-id="735da-169">Términos de FORMs</span><span class="sxs-lookup"><span data-stu-id="735da-169">FORMSOF Term</span></span>](-search-sql-formsof.md)
- [<span data-ttu-id="735da-170">Término ISABOUT</span><span class="sxs-lookup"><span data-stu-id="735da-170">ISABOUT Term</span></span>](-search-sql-isabout.md)
- [<span data-ttu-id="735da-171">A corto plazo</span><span class="sxs-lookup"><span data-stu-id="735da-171">NEAR Term</span></span>](-search-sql-near.md)

## <a name="related-topics"></a><span data-ttu-id="735da-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="735da-172">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="735da-173">Referencia</span><span class="sxs-lookup"><span data-stu-id="735da-173">Reference</span></span>

[<span data-ttu-id="735da-174">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="735da-174">WHERE Clause</span></span>](-search-sql-where.md)

### <a name="conceptual"></a><span data-ttu-id="735da-175">Conceptual</span><span class="sxs-lookup"><span data-stu-id="735da-175">Conceptual</span></span>

[<span data-ttu-id="735da-176">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="735da-176">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)

[<span data-ttu-id="735da-177">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="735da-177">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
