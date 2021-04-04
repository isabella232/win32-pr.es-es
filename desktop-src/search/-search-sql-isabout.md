---
description: El término ISABOUT coincide con las columnas de un grupo de uno o más términos de búsqueda.
ms.assetid: e2629c4c-4b44-4427-ac1d-17f55fd969e3
title: Término ISABOUT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f79fc2fa4a56b3ca6b3b412141f096b282e3aa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808936"
---
# <a name="isabout-term"></a><span data-ttu-id="71230-103">Término ISABOUT</span><span class="sxs-lookup"><span data-stu-id="71230-103">ISABOUT Term</span></span>

<span data-ttu-id="71230-104">**En desuso**</span><span class="sxs-lookup"><span data-stu-id="71230-104">**Deprecated**</span></span>

<span data-ttu-id="71230-105">Esta característica se ha quitado de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71230-105">This feature has been removed as of Windows 8.</span></span> <span data-ttu-id="71230-106">Si escribe nuevas aplicaciones, evite usar esta característica en desuso.</span><span class="sxs-lookup"><span data-stu-id="71230-106">If you write new applications, avoid using this deprecated feature.</span></span> <span data-ttu-id="71230-107">Si modifica las aplicaciones existentes, le recomendamos encarecidamente que quite todas las dependencias de esta característica.</span><span class="sxs-lookup"><span data-stu-id="71230-107">If you modify existing applications, you are strongly encouraged to remove any dependency on this feature.</span></span>

<span data-ttu-id="71230-108">El término ISABOUT coincide con las columnas de un grupo de uno o más términos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="71230-108">The ISABOUT term matches columns against a group of one or more search terms.</span></span> <span data-ttu-id="71230-109">Tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="71230-109">It has the following syntax:</span></span>


```
ISABOUT(<components>) [RANKMETHOD <method>]
```



<span data-ttu-id="71230-110">El término RANKMETHOD opcional especifica el método de cálculo que se usa para clasificar los documentos que coinciden con uno o varios de los componentes.</span><span class="sxs-lookup"><span data-stu-id="71230-110">The optional RANKMETHOD term specifies the calculation method used to rank the documents that match one or more of the components.</span></span> <span data-ttu-id="71230-111">Si no se especifica RANKMETHOD, se usa el método predeterminado de clasificación de coeficientes de Jaccard.</span><span class="sxs-lookup"><span data-stu-id="71230-111">If no RANKMETHOD is specified, the default Jaccard Coefficient ranking method is used.</span></span>

<span data-ttu-id="71230-112">El término ISABOUT puede tener uno o más componentes.</span><span class="sxs-lookup"><span data-stu-id="71230-112">The ISABOUT term can have one or more components.</span></span> <span data-ttu-id="71230-113">Las columnas especificadas en el predicado [Contains](-search-sql-contains.md) se prueban en cada componente.</span><span class="sxs-lookup"><span data-stu-id="71230-113">The columns specified in the [CONTAINS](-search-sql-contains.md) predicate are tested against each component.</span></span> <span data-ttu-id="71230-114">El documento se incluye en los resultados si al menos uno de los componentes coincide con.</span><span class="sxs-lookup"><span data-stu-id="71230-114">The document is included in the results if at least one of the components matches.</span></span> <span data-ttu-id="71230-115">Las comas separan varios componentes.</span><span class="sxs-lookup"><span data-stu-id="71230-115">Commas separate multiple components.</span></span>

<span data-ttu-id="71230-116">La parte del componente tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="71230-116">The component part has the following syntax:</span></span>


```
<match_term> [<weight_term>]
```



<span data-ttu-id="71230-117">Puede usar el término de PONDERAción opcional para cambiar la importancia relativa de cada término dentro del término ISABOUT.</span><span class="sxs-lookup"><span data-stu-id="71230-117">You can use the optional WEIGHT term to change the relative importance of each term within the ISABOUT term.</span></span> <span data-ttu-id="71230-118">Si no se aplica ningún término de peso, se implica el peso predeterminado 1,0.</span><span class="sxs-lookup"><span data-stu-id="71230-118">If no weight term is applied, the default 1.0 weight is implied.</span></span>

<span data-ttu-id="71230-119">En la tabla siguiente se describen los posibles tipos de términos de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="71230-119">The following table describes possible match term types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71230-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="71230-120">Type</span></span></th>
<th><span data-ttu-id="71230-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="71230-121">Description</span></span></th>
<th><span data-ttu-id="71230-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71230-122">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71230-123">Word</span><span class="sxs-lookup"><span data-stu-id="71230-123">Word</span></span></td>
<td><span data-ttu-id="71230-124">Una sola palabra sin espacios u otros signos de puntuación.</span><span class="sxs-lookup"><span data-stu-id="71230-124">A single word without spaces or other punctuation.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer&quot;,&quot;software&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="71230-125">Frase</span><span class="sxs-lookup"><span data-stu-id="71230-125">Phrase</span></span></td>
<td><span data-ttu-id="71230-126">Varias palabras o espacios incluidos.</span><span class="sxs-lookup"><span data-stu-id="71230-126">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;computer software&quot;,&quot;hardware&quot;)&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71230-127">Wildcard (Carácter comodín)</span><span class="sxs-lookup"><span data-stu-id="71230-127">Wildcard</span></span></td>
<td><span data-ttu-id="71230-128">Palabras o frases con el asterisco (\*) agregados al final.</span><span class="sxs-lookup"><span data-stu-id="71230-128">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="71230-129">Para obtener más información, vea <a href="-search-sql-wildcards.md">usar caracteres comodín en el predicado CONtains</a>.</span><span class="sxs-lookup"><span data-stu-id="71230-129">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
 (&#39;ISABOUT (&quot;compu*&quot;,&quot;soft*&quot;)&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;, &quot;computation&quot;, 
and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="isabout-column-weighting"></a><span data-ttu-id="71230-130">Ponderación de columnas de ISABOUT</span><span class="sxs-lookup"><span data-stu-id="71230-130">ISABOUT Column Weighting</span></span>

<span data-ttu-id="71230-131">El término ISABOUT clasifica los documentos coincidentes en función del grado de coincidencia de cada documento con el conjunto de términos coincidentes de la consulta.</span><span class="sxs-lookup"><span data-stu-id="71230-131">The ISABOUT term ranks matching documents based on how closely each document matches the set of match terms in the query.</span></span> <span data-ttu-id="71230-132">Puede usar la ponderación de columnas para hacer más importante la coincidencia de algunos términos de coincidencia que otros.</span><span class="sxs-lookup"><span data-stu-id="71230-132">You can use column weighting to place more importance on matching some match terms than others.</span></span> <span data-ttu-id="71230-133">Cada término coincidente en el término ISABOUT puede tener un valor de peso aplicado.</span><span class="sxs-lookup"><span data-stu-id="71230-133">Each match term in the ISABOUT term can have a weight value applied.</span></span> <span data-ttu-id="71230-134">El peso se aplica a un único término de coincidencia y se indica mediante la palabra clave "WEIGHT".</span><span class="sxs-lookup"><span data-stu-id="71230-134">The weight is applied to a single match term and is indicated by the keyword "WEIGHT".</span></span> <span data-ttu-id="71230-135">El término de PONDERAción tiene dos sintaxis alternativas:</span><span class="sxs-lookup"><span data-stu-id="71230-135">The WEIGHT term has two alternative syntaxes:</span></span>


```
<match_term> WEIGHT(<weight_value>)
<match_term>:(<weight_value>)
```



<span data-ttu-id="71230-136">El valor de peso debe estar entre 0 y 1,0, sin más de tres posiciones decimales.</span><span class="sxs-lookup"><span data-stu-id="71230-136">The weight value must be between 0 and 1.0, with no more than three decimal places.</span></span> <span data-ttu-id="71230-137">Si se especifica un valor de peso fuera de este intervalo, se genera un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="71230-137">Specifying a weight value outside this range results in an error message.</span></span> <span data-ttu-id="71230-138">El valor de clasificación no ponderado para un término se multiplica por el valor de peso del término.</span><span class="sxs-lookup"><span data-stu-id="71230-138">The unweighted ranking value for a term is multiplied by the weight value for the term.</span></span>

<span data-ttu-id="71230-139">Si no se especifica ningún peso para un término de coincidencia, se implica el valor predeterminado, 1,0.</span><span class="sxs-lookup"><span data-stu-id="71230-139">If no weight is specified for a match term, the default value, 1.0, is implied.</span></span>

### <a name="example"></a><span data-ttu-id="71230-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71230-140">Example</span></span>

<span data-ttu-id="71230-141">En el ejemplo siguiente se aplican pesos a los dos términos de coincidencia de ISABOUT, con la sintaxis Long y Short para los valores de ponderación.</span><span class="sxs-lookup"><span data-stu-id="71230-141">The following example applies weights to the two ISABOUT match terms, using both the long and short syntax for weight values.</span></span>


```
WHERE CONTAINS( System.FileName,
      'ISABOUT("computer" WEIGHT (0.75),"software":0.25)')
```



## <a name="related-topics"></a><span data-ttu-id="71230-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71230-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="71230-143">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="71230-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="71230-144">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="71230-144">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="71230-145">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="71230-145">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



