---
description: El término próximo se usa para especificar que dos términos de búsqueda de contenido deben estar relativamente cerca de otro para que se reconozcan como coincidencia para el predicado CONTAINS.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: A corto plazo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360190"
---
# <a name="near-term"></a><span data-ttu-id="89b3b-103">A corto plazo</span><span class="sxs-lookup"><span data-stu-id="89b3b-103">NEAR Term</span></span>

<span data-ttu-id="89b3b-104">El término próximo se usa para especificar que dos términos de búsqueda de contenido deben estar relativamente cerca de otro para que se reconozcan como coincidencia para el predicado [Contains](-search-sql-contains.md) .</span><span class="sxs-lookup"><span data-stu-id="89b3b-104">The NEAR term is used to specify that two content search terms must be relatively close to one another to be recognized as matching for the [CONTAINS](-search-sql-contains.md) predicate.</span></span>

<span data-ttu-id="89b3b-105">La sintaxis para el término próximo es:</span><span class="sxs-lookup"><span data-stu-id="89b3b-105">The syntax for the NEAR term is:</span></span>


```
<content_search_term> NEAR | ~ <content_search_term>
```



<span data-ttu-id="89b3b-106">El término próximo se puede representar mediante la palabra clave "NEAR" o una tilde (~).</span><span class="sxs-lookup"><span data-stu-id="89b3b-106">The NEAR term can be represented by the keyword "NEAR" or by a tilde (~).</span></span>

<span data-ttu-id="89b3b-107">Cuando las palabras Unidas cerca de la consulta se encuentran en unas 50 palabras aproximadamente entre sí dentro de la columna en la que se busca, el término próximo devuelve una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="89b3b-107">When the words joined by NEAR in the query are found within approximately 50 words of each other inside the column being searched, the NEAR term returns a match.</span></span> <span data-ttu-id="89b3b-108">Cuanto más se acerquen las dos palabras, mayor será el rango calculado para el término próximo.</span><span class="sxs-lookup"><span data-stu-id="89b3b-108">The closer together the two words are, the higher the calculated rank for the NEAR term.</span></span> <span data-ttu-id="89b3b-109">Cuanto más lejos se encuentran las dos palabras, menor es el rango.</span><span class="sxs-lookup"><span data-stu-id="89b3b-109">The farther apart the two words are, the lower the rank.</span></span>

> [!Note]  
> <span data-ttu-id="89b3b-110">El número de palabras entre los términos de búsqueda encontrados es aproximado y depende de la apariencia de las palabras irrelevantes, como "a" o "The", y cómo wordbreakers el texto de tokens.</span><span class="sxs-lookup"><span data-stu-id="89b3b-110">The number of words between found search terms is approximate and depends on the appearance of noise words, like "a" or "the", and how wordbreakers tokenize text.</span></span> <span data-ttu-id="89b3b-111">Puede ser inferior a 50.</span><span class="sxs-lookup"><span data-stu-id="89b3b-111">It may be less than 50.</span></span>

 


<span data-ttu-id="89b3b-112">En la tabla siguiente se describen los tipos de términos de búsqueda de contenido que se pueden usar con un término cercano en un predicado CONTAINS.</span><span class="sxs-lookup"><span data-stu-id="89b3b-112">The following table describes content search term types that can be used with a NEAR term in a CONTAINS predicate.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89b3b-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="89b3b-113">Type</span></span></th>
<th><span data-ttu-id="89b3b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="89b3b-114">Description</span></span></th>
<th><span data-ttu-id="89b3b-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="89b3b-115">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89b3b-116">Word</span><span class="sxs-lookup"><span data-stu-id="89b3b-116">Word</span></span></td>
<td><span data-ttu-id="89b3b-117">Una sola palabra sin espacios u otros signos de puntuación.</span><span class="sxs-lookup"><span data-stu-id="89b3b-117">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="89b3b-118">No es necesario incluir comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="89b3b-118">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="89b3b-119">Frase</span><span class="sxs-lookup"><span data-stu-id="89b3b-119">Phrase</span></span></td>
<td><span data-ttu-id="89b3b-120">Varias palabras o espacios incluidos.</span><span class="sxs-lookup"><span data-stu-id="89b3b-120">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89b3b-121">Wildcard (Carácter comodín)</span><span class="sxs-lookup"><span data-stu-id="89b3b-121">Wildcard</span></span></td>
<td><span data-ttu-id="89b3b-122">Palabras o frases con el asterisco (\*) agregados al final.</span><span class="sxs-lookup"><span data-stu-id="89b3b-122">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="89b3b-123">Para obtener más información, vea <a href="-search-sql-wildcards.md">usar caracteres comodín en el predicado CONtains</a>.</span><span class="sxs-lookup"><span data-stu-id="89b3b-123">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="89b3b-124">Si las palabras coincidentes especificadas con el término próximo se encuentran en la columna que se está buscando, pero se encuentran más allá de las 50 palabras, el resultado sigue siendo devuelto, pero tiene un [rango](-search-sql-understandingrelevancevalues.md) de 0.</span><span class="sxs-lookup"><span data-stu-id="89b3b-124">If the match words specified with the NEAR term are both found in the column being searched, but are farther apart than 50 words, the result is still returned, but has a [rank](-search-sql-understandingrelevancevalues.md) of 0.</span></span>

 

### <a name="example"></a><span data-ttu-id="89b3b-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89b3b-125">Example</span></span>

<span data-ttu-id="89b3b-126">En el ejemplo siguiente se muestra el encadenamiento de términos cercanos, usando las formas corto y largo del término:</span><span class="sxs-lookup"><span data-stu-id="89b3b-126">The following example shows chaining of NEAR terms, using both the short and long forms of the term:</span></span>


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a><span data-ttu-id="89b3b-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89b3b-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="89b3b-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="89b3b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="89b3b-129">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="89b3b-129">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="89b3b-130">**Vista**</span><span class="sxs-lookup"><span data-stu-id="89b3b-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="89b3b-131">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="89b3b-131">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="89b3b-132">Usar caracteres comodín en el predicado CONTAINS</span><span class="sxs-lookup"><span data-stu-id="89b3b-132">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
</dt> </dl>

 

 



