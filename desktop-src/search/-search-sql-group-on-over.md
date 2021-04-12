---
description: El grupo en...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: AGRUPAR POR... MÁS DE... Privacidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153958"
---
# <a name="group-on--over--statement"></a><span data-ttu-id="e3790-103">AGRUPAR POR... MÁS DE... Privacidad</span><span class="sxs-lookup"><span data-stu-id="e3790-103">GROUP ON ... OVER ... Statement</span></span>

<span data-ttu-id="e3790-104">El grupo en... MÁS de... la instrucción devuelve un conjunto de filas jerárquico en el que los resultados de la búsqueda se dividen en grupos basándose en una columna especificada y en los intervalos de agrupación opcionales.</span><span class="sxs-lookup"><span data-stu-id="e3790-104">The GROUP ON... OVER... statement returns a hierarchical rowset in which search results are divided into groups based on a specified column and optional grouping ranges.</span></span> <span data-ttu-id="e3790-105">Si agrupa en la columna [System. Kind](../properties/props-system-kind.md) , el conjunto de resultados se divide en varios grupos: uno para los documentos, otro para las comunicaciones, etc.</span><span class="sxs-lookup"><span data-stu-id="e3790-105">If you group on the [System.Kind](../properties/props-system-kind.md) column, the result set is divided into multiple groups: one for documents, one for communications, and so on.</span></span> <span data-ttu-id="e3790-106">Si agrupa en [System. Size](../properties/props-system-size.md) y group Range 100 KB, el conjunto de resultados se divide en tres grupos: elementos de tamaño < 100 KB, elementos de tamaño >= 100 KB y elementos sin valor de tamaño.</span><span class="sxs-lookup"><span data-stu-id="e3790-106">If you group on [System.Size](../properties/props-system-size.md) and group range 100 KB, the result set is divided into three groups: items of size < 100 KB, items of size >= 100 KB, and items with no size value.</span></span> <span data-ttu-id="e3790-107">También puede Agregar agrupaciones con funciones.</span><span class="sxs-lookup"><span data-stu-id="e3790-107">You can also aggregate groupings with functions.</span></span>

<span data-ttu-id="e3790-108">En este tema se tratan los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="e3790-108">This topic covers the following subjects:</span></span>

-   [<span data-ttu-id="e3790-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3790-109">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="e3790-110">Intervalos de grupo</span><span class="sxs-lookup"><span data-stu-id="e3790-110">Group Ranges</span></span>](#group-ranges)
-   [<span data-ttu-id="e3790-111">Etiquetar grupos</span><span class="sxs-lookup"><span data-stu-id="e3790-111">Labeling Groups</span></span>](#labeling-groups)
-   [<span data-ttu-id="e3790-112">Ordenar grupos</span><span class="sxs-lookup"><span data-stu-id="e3790-112">Ordering Groups</span></span>](#ordering-groups)
-   [<span data-ttu-id="e3790-113">Anidar grupos</span><span class="sxs-lookup"><span data-stu-id="e3790-113">Nesting Groups</span></span>](#nesting-groups)
-   [<span data-ttu-id="e3790-114">Agrupar en propiedades de vector</span><span class="sxs-lookup"><span data-stu-id="e3790-114">Grouping on Vector Properties</span></span>](#grouping-on-vector-properties)
-   [<span data-ttu-id="e3790-115">Más ejemplos</span><span class="sxs-lookup"><span data-stu-id="e3790-115">More Examples</span></span>](#more-examples)
-   [<span data-ttu-id="e3790-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3790-116">Related topics</span></span>](#related-topics)

## <a name="syntax"></a><span data-ttu-id="e3790-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3790-117">Syntax</span></span>

<span data-ttu-id="e3790-118">El grupo en... MÁS DE... la instrucción tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e3790-118">The GROUP ON ... OVER ... statement has the following syntax:</span></span>


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



<span data-ttu-id="e3790-119">donde los intervalos de agrupación se definen de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="e3790-119">where grouping ranges are defined as follows:</span></span>


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



<span data-ttu-id="e3790-120">El grupo en <column> puede ser un [identificador](-search-sql-identifiers.md) normal o delimitado para una propiedad en el almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e3790-120">The GROUP ON <column> can be a regular or delimited [identifier](-search-sql-identifiers.md) for a property in the property store.</span></span>

<span data-ttu-id="e3790-121">El opcional <group ranges> es una lista de uno o más valores (número, fecha o cadena) que se usan para dividir los resultados en grupos.</span><span class="sxs-lookup"><span data-stu-id="e3790-121">The optional <group ranges> is a list of one or more values (number, date, or string) used for dividing the results into groups.</span></span> <span data-ttu-id="e3790-122"><range limit>Identifica un punto de división en el conjunto de resultados devuelto y el <label> identifica una etiqueta descriptiva para un grupo.</span><span class="sxs-lookup"><span data-stu-id="e3790-122">The <range limit> identifies a division point in the returned result set, and the <label> identifies a user-friendly label for a group.</span></span> <span data-ttu-id="e3790-123">Puede dividir el conjunto de resultados en tantos grupos como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e3790-123">You can divide the result set into as many groups as you need.</span></span>

<span data-ttu-id="e3790-124">El primer grupo de resultados incluye elementos con el valor mínimo posible para la propiedad especificada hasta el límite del primer intervalo, sin incluirlo.</span><span class="sxs-lookup"><span data-stu-id="e3790-124">The first group of results includes items with the minimum possible value for the specified property up to but not including the first range limit.</span></span> <span data-ttu-id="e3790-125">Se puede hacer referencia a este grupo con la palabra clave MINVALUE.</span><span class="sxs-lookup"><span data-stu-id="e3790-125">This group can be referred to with the MINVALUE keyword.</span></span> <span data-ttu-id="e3790-126">Se puede hacer referencia al segundo grupo con el especificador de límite de intervalo en sí e incluye los elementos cuyo valor de la propiedad especificada es igual o mayor que el límite de intervalo.</span><span class="sxs-lookup"><span data-stu-id="e3790-126">The second group can be referred to with the range limit specifier itself and includes items whose value for the specified property is equal to or greater than the range limit.</span></span> <span data-ttu-id="e3790-127">Los elementos que no tienen un valor para la propiedad especificada se devuelven en último lugar y se puede hacer referencia a ellos con la palabra clave **null** .</span><span class="sxs-lookup"><span data-stu-id="e3790-127">Any items that do not have a value for the specified property are returned last and can be referred to with the **NULL** keyword.</span></span>

<span data-ttu-id="e3790-128">Por ejemplo, un límite de intervalo de ' 2006-01-01 ' para la propiedad [System. DateCreated](../properties/props-system-datecreated.md) divide el conjunto de resultados en elementos con fechas anteriores a 2006-01-01 (grupo MINVALUE), elementos con fechas de la 2006-01-01 (grupo de 2006-01-01) y elementos sin fecha (grupo **null** ).</span><span class="sxs-lookup"><span data-stu-id="e3790-128">For example, a range limit of '2006-01-01' for the [System.DateCreated](../properties/props-system-datecreated.md) property divides the result set into items with dates before 2006-01-01 (MINVALUE group), items with dates on or after 2006-01-01 (2006-01-01 group), and items with no date (**NULL** group).</span></span>

<span data-ttu-id="e3790-129">Dentro de cada grupo, los resultados se ordenan por los valores de la columna AGRUPAr por de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e3790-129">Within each group, the results are sorted by the values in the GROUP ON column by default.</span></span> <span data-ttu-id="e3790-130">La cláusula [order by](-search-sql-orderby.md) opcional puede contener un especificador de dirección de ASC para ascendente (de menor a mayor) o DESC para descendente (de alto a bajo) y el [orden en la cláusula Group by](-search-sql-orderingroup.md) puede ordenar cada grupo mediante reglas diferentes.</span><span class="sxs-lookup"><span data-stu-id="e3790-130">The optional [ORDER BY](-search-sql-orderby.md) clause can contain a direction specifier of either ASC for ascending (low to high) or DESC for descending (high to low), and the [ORDER IN GROUP BY](-search-sql-orderingroup.md) clause can order each group using different rules.</span></span> <span data-ttu-id="e3790-131">Vea la sección [grupos de ordenación](#ordering-groups) a continuación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e3790-131">See the [Ordering Groups](#ordering-groups) section below for more information.</span></span>

## <a name="group-ranges"></a><span data-ttu-id="e3790-132">Intervalos de grupo</span><span class="sxs-lookup"><span data-stu-id="e3790-132">Group Ranges</span></span>

<span data-ttu-id="e3790-133">En la tabla siguiente se muestra cómo los resultados se dividen en grupos basados en los límites de intervalo:</span><span class="sxs-lookup"><span data-stu-id="e3790-133">The following table demonstrates how results are divided into groups based the range limits:</span></span>



| <span data-ttu-id="e3790-134">Ejemplo ( <column> \[ intervalos de grupo \] )</span><span class="sxs-lookup"><span data-stu-id="e3790-134">Example (<column> \[group ranges\])</span></span>        | <span data-ttu-id="e3790-135">Resultado</span><span class="sxs-lookup"><span data-stu-id="e3790-135">Result</span></span>                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3790-136">System. Size \[ 1000, 5000\]</span><span class="sxs-lookup"><span data-stu-id="e3790-136">System.Size \[1000, 5000\]</span></span>                       | <span data-ttu-id="e3790-137">Los resultados se agrupan en cuatro cubos: **MINVALUE**: Size < 1000</span><span class="sxs-lookup"><span data-stu-id="e3790-137">Results are grouped into four buckets: **MINVALUE**: Size < 1000</span></span><br/> <span data-ttu-id="e3790-138">**1000:** 1000 <= tamaño < 5000</span><span class="sxs-lookup"><span data-stu-id="e3790-138">**1000:** 1000 <= Size < 5000</span></span><br/> <span data-ttu-id="e3790-139">**5000:** Tamaño >= 5000</span><span class="sxs-lookup"><span data-stu-id="e3790-139">**5000:** Size >= 5000</span></span><br/> <span data-ttu-id="e3790-140">**Null:** Ningún valor para el tamaño</span><span class="sxs-lookup"><span data-stu-id="e3790-140">**NULL:** No value for Size</span></span><br/>                                                                      |
| <span data-ttu-id="e3790-141">System. Author \[ before (' m '), After (' r ')\]</span><span class="sxs-lookup"><span data-stu-id="e3790-141">System.Author \[BEFORE('m'),AFTER('r')\]</span></span>         | <span data-ttu-id="e3790-142">Los resultados se agrupan en cuatro cubos: **MINVALUE:** autor < carácter antes que "m"</span><span class="sxs-lookup"><span data-stu-id="e3790-142">Results are grouped into four buckets: **MINVALUE:** Author < character before "m"</span></span><br/> <span data-ttu-id="e3790-143">**m:** carácter antes de "m" <= autor < carácter después de "r"</span><span class="sxs-lookup"><span data-stu-id="e3790-143">**m:** character before "m" <= Author < character after "r"</span></span><br/> <span data-ttu-id="e3790-144">**r:** carácter después de "r" <= autor</span><span class="sxs-lookup"><span data-stu-id="e3790-144">**r:** character after "r" <= Author</span></span><br/> <span data-ttu-id="e3790-145">**Null:** No hay ningún valor para autor</span><span class="sxs-lookup"><span data-stu-id="e3790-145">**NULL:** No value for Author</span></span><br/>      |
| <span data-ttu-id="e3790-146">System. Author \[ MINVALUE/' a to l ', ' m '/i a z '\]</span><span class="sxs-lookup"><span data-stu-id="e3790-146">System.Author \[MINVALUE/'a to l',"m"/'m to z'\]</span></span> | <span data-ttu-id="e3790-147">Los resultados se agrupan en tres depósitos: a **a l:** autor < "m"</span><span class="sxs-lookup"><span data-stu-id="e3790-147">Results are grouped into three buckets: **a to l:** Author < "m"</span></span><br/> <span data-ttu-id="e3790-148">**de m a z:** "m" <= autor</span><span class="sxs-lookup"><span data-stu-id="e3790-148">**m to z:** "m" <= Author</span></span> <br/> <span data-ttu-id="e3790-149">**Null:** No hay ningún valor para autor</span><span class="sxs-lookup"><span data-stu-id="e3790-149">**NULL:** No value for Author</span></span><br/>                                                                                                               |
| <span data-ttu-id="e3790-150">System. DateCreated \[ ' 2005-1-01 ', ' 2006-6-01 '\]</span><span class="sxs-lookup"><span data-stu-id="e3790-150">System.DateCreated \['2005-1-01','2006-6-01'\]</span></span>   | <span data-ttu-id="e3790-151">Los resultados se agrupan en cuatro cubos:</span><span class="sxs-lookup"><span data-stu-id="e3790-151">Results are grouped into four buckets:</span></span><br/> <span data-ttu-id="e3790-152">**MINVALUE:** DateCreated < 2005-1-01</span><span class="sxs-lookup"><span data-stu-id="e3790-152">**MINVALUE:** DateCreated < 2005-1-01</span></span><br/> <span data-ttu-id="e3790-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="e3790-153">**2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01</span></span><br/> <span data-ttu-id="e3790-154">**2006-1-01:** DateCreated >= 2006-6-01</span><span class="sxs-lookup"><span data-stu-id="e3790-154">**2006-1-01:** DateCreated >= 2006-6-01</span></span><br/> <span data-ttu-id="e3790-155">**Null:** Ningún valor para DateCreated</span><span class="sxs-lookup"><span data-stu-id="e3790-155">**NULL:** No value for DateCreated</span></span><br/> |



 

 

> [!IMPORTANT]
>
> <span data-ttu-id="e3790-156">Errónea `GROUP ON System.Author['m','z','a']`</span><span class="sxs-lookup"><span data-stu-id="e3790-156">Incorrect: `GROUP ON System.Author['m','z','a']`</span></span>
>
> <span data-ttu-id="e3790-157">Correcto `GROUP ON System.Author['a','m','z']`</span><span class="sxs-lookup"><span data-stu-id="e3790-157">Correct: `GROUP ON System.Author['a','m','z']`</span></span>

 

 

## <a name="labeling-groups"></a><span data-ttu-id="e3790-158">Etiquetar grupos</span><span class="sxs-lookup"><span data-stu-id="e3790-158">Labeling Groups</span></span>

<span data-ttu-id="e3790-159">Para mejorar la legibilidad, puede etiquetar los grupos con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="e3790-159">To improve readability, you can label groups using the following syntax:</span></span>


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



<span data-ttu-id="e3790-160">La etiqueta se separa del límite de intervalo con una marca de barra diagonal y se escribe entre comillas simples.</span><span class="sxs-lookup"><span data-stu-id="e3790-160">The label is separated from the range limit with a slash mark and is enclosed in single quotation marks.</span></span> <span data-ttu-id="e3790-161">Si no especifica una etiqueta, el nombre de grupo es la cadena de límite de intervalo.</span><span class="sxs-lookup"><span data-stu-id="e3790-161">If you do not specify a label, the group name is the range limit string.</span></span>

<span data-ttu-id="e3790-162">El siguiente es un ejemplo de grupos de etiquetas:</span><span class="sxs-lookup"><span data-stu-id="e3790-162">The following is an example of labeling groups:</span></span>


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



<span data-ttu-id="e3790-163">En Windows 7 o versiones posteriores, también puede usar una \[ etiqueta genérica \] de otro para combinar varios intervalos de agrupación.</span><span class="sxs-lookup"><span data-stu-id="e3790-163">In Windows 7 or later, you can also use a generic \[OTHER\] label to combine multiple grouping ranges.</span></span> <span data-ttu-id="e3790-164">Los resultados de todos los grupos identificados con esta etiqueta se combinarán en un grupo con esta etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e3790-164">Results from all groups identified with this label will be combined into one group with this label.</span></span> <span data-ttu-id="e3790-165">Este grupo de resultados se devuelve después de todos los demás grupos excepto el grupo **null** .</span><span class="sxs-lookup"><span data-stu-id="e3790-165">This group of results is returned after all other groups except for the **NULL** group.</span></span> <span data-ttu-id="e3790-166">El grupo **null** contiene los resultados de los elementos que no tienen un valor para la propiedad especificada.</span><span class="sxs-lookup"><span data-stu-id="e3790-166">The **NULL** group contains results for items that do not have a value for the specified property.</span></span> <span data-ttu-id="e3790-167">Antes de Windows 7, la \[ otra \] etiqueta se trata como cualquier otra etiqueta de grupo.</span><span class="sxs-lookup"><span data-stu-id="e3790-167">Prior to Windows 7 the \[OTHER\] label is treated like any other group label.</span></span>

<span data-ttu-id="e3790-168">El código siguiente es un ejemplo del uso de la \[ otra \] etiqueta para los grupos que se crearían en Windows 7 o posterior:</span><span class="sxs-lookup"><span data-stu-id="e3790-168">The following code is an example of using the \[OTHER\] label for groups that would be created in Windows 7 or later:</span></span>


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



<span data-ttu-id="e3790-169">En la tabla siguiente se muestran los grupos que se crearían con el código de agrupación anterior en Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e3790-169">The following table shows the groups that would be created by the preceding grouping code in Windows 7 or later.</span></span>



| <span data-ttu-id="e3790-170">Grupo</span><span class="sxs-lookup"><span data-stu-id="e3790-170">Group</span></span>     | <span data-ttu-id="e3790-171">System.Author</span><span class="sxs-lookup"><span data-stu-id="e3790-171">System.Author</span></span> | <span data-ttu-id="e3790-172">System. FileName</span><span class="sxs-lookup"><span data-stu-id="e3790-172">System.FileName</span></span> |
|-----------|---------------|-----------------|
| <span data-ttu-id="e3790-173">0</span><span class="sxs-lookup"><span data-stu-id="e3790-173">0</span></span>         | <span data-ttu-id="e3790-174">1Bill</span><span class="sxs-lookup"><span data-stu-id="e3790-174">1Bill</span></span>         | <span data-ttu-id="e3790-175">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-175">Lorem.docx</span></span>      |
| <span data-ttu-id="e3790-176">Q</span><span class="sxs-lookup"><span data-stu-id="e3790-176">Q</span></span>         | <span data-ttu-id="e3790-177">Reina</span><span class="sxs-lookup"><span data-stu-id="e3790-177">Queen</span></span>         | <span data-ttu-id="e3790-178">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-178">Ipsum.docx</span></span>      |
|           | <span data-ttu-id="e3790-179">Robin</span><span class="sxs-lookup"><span data-stu-id="e3790-179">Robin</span></span>         | <span data-ttu-id="e3790-180">dolor.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-180">dolor.docx</span></span>      |
| <span data-ttu-id="e3790-181">Y</span><span class="sxs-lookup"><span data-stu-id="e3790-181">Y</span></span>         | <span data-ttu-id="e3790-182">Zara</span><span class="sxs-lookup"><span data-stu-id="e3790-182">Zara</span></span>          | <span data-ttu-id="e3790-183">amet.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-183">amet.docx</span></span>       |
| <span data-ttu-id="e3790-184">\[DISTINTA\]</span><span class="sxs-lookup"><span data-stu-id="e3790-184">\[OTHER\]</span></span> | <span data-ttu-id="e3790-185">Abner</span><span class="sxs-lookup"><span data-stu-id="e3790-185">Abner</span></span>         | <span data-ttu-id="e3790-186">nonummy.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-186">nonummy.docx</span></span>    |
|           | <span data-ttu-id="e3790-187">Bob</span><span class="sxs-lookup"><span data-stu-id="e3790-187">Bob</span></span>           | <span data-ttu-id="e3790-188">laoreet.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-188">laoreet.docx</span></span>    |
|           | <span data-ttu-id="e3790-189">Xaria</span><span class="sxs-lookup"><span data-stu-id="e3790-189">Xaria</span></span>         | <span data-ttu-id="e3790-190">magna.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-190">magna.docx</span></span>      |
| <span data-ttu-id="e3790-191">**NULL**</span><span class="sxs-lookup"><span data-stu-id="e3790-191">**NULL**</span></span>  |               | <span data-ttu-id="e3790-192">aliquam.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-192">aliquam.docx</span></span>    |



 

## <a name="ordering-groups"></a><span data-ttu-id="e3790-193">Ordenar grupos</span><span class="sxs-lookup"><span data-stu-id="e3790-193">Ordering Groups</span></span>

<span data-ttu-id="e3790-194">Hay tres maneras de ordenar los elementos de los grupos:</span><span class="sxs-lookup"><span data-stu-id="e3790-194">There are three ways to order items in groups:</span></span>

-   <span data-ttu-id="e3790-195">Ordenación predeterminada: Si no se especifica lo contrario, los resultados se ordenan por los valores de la columna AGRUPAr por en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="e3790-195">Default ordering: If you do not specify otherwise, the results are ordered by the values in the GROUP ON column, in ascending order.</span></span>
-   <span data-ttu-id="e3790-196">ORDER BY: puede especificar el orden descendente en una cláusula ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="e3790-196">ORDER BY: You can specify descending order in an ORDER BY clause.</span></span> <span data-ttu-id="e3790-197">Debe ordenar los resultados por el grupo en la columna.</span><span class="sxs-lookup"><span data-stu-id="e3790-197">You must order the results by the GROUP ON column.</span></span>
-   <span data-ttu-id="e3790-198">ORDENAR por AGRUPAr por: puede especificar un orden diferente para cada grupo.</span><span class="sxs-lookup"><span data-stu-id="e3790-198">ORDER IN GROUP BY: You can specify a different order for each group.</span></span> <span data-ttu-id="e3790-199">Si agrupa en [System. Kind](../properties/props-system-kind.md), puede ordenar documentos por System. [Author](../properties/props-system-author.md) y música por [System. Music. artista](../properties/props-system-music-artist.md).</span><span class="sxs-lookup"><span data-stu-id="e3790-199">If you group on [System.Kind](../properties/props-system-kind.md), you can order documents by [System.Author](../properties/props-system-author.md) and music by [System.Music.Artist](../properties/props-system-music-artist.md).</span></span>

<span data-ttu-id="e3790-200">Para obtener más información sobre la ordenación de los resultados, vea las páginas de referencia de cláusula [order by](-search-sql-orderby.md) y [Order in Group](-search-sql-orderingroup.md) .</span><span class="sxs-lookup"><span data-stu-id="e3790-200">For more information on ordering results, see the [ORDER BY Clause](-search-sql-orderby.md) and [ORDER IN GROUP Clause](-search-sql-orderingroup.md) reference pages.</span></span>

## <a name="nesting-groups"></a><span data-ttu-id="e3790-201">Anidar grupos</span><span class="sxs-lookup"><span data-stu-id="e3790-201">Nesting Groups</span></span>

<span data-ttu-id="e3790-202">Puede anidar grupos con varias cláusulas GROUP BY.</span><span class="sxs-lookup"><span data-stu-id="e3790-202">You can nest groups with multiple GROUP ON clauses.</span></span> <span data-ttu-id="e3790-203">El orden especificado en la consulta se refleja directamente en la jerarquía de grupos de salida, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e3790-203">The order specified in the query is directly reflected in the output group hierarchy, as shown in the following example.</span></span>


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| <span data-ttu-id="e3790-204">System. Kind</span><span class="sxs-lookup"><span data-stu-id="e3790-204">System.Kind</span></span>    | <span data-ttu-id="e3790-205">System.Author</span><span class="sxs-lookup"><span data-stu-id="e3790-205">System.Author</span></span> | <span data-ttu-id="e3790-206">System. DateCreated</span><span class="sxs-lookup"><span data-stu-id="e3790-206">System.DateCreated</span></span> |
|----------------|---------------|--------------------|
| <span data-ttu-id="e3790-207">perdidos</span><span class="sxs-lookup"><span data-stu-id="e3790-207">documents</span></span>      | <span data-ttu-id="e3790-208">Willa</span><span class="sxs-lookup"><span data-stu-id="e3790-208">Willa</span></span>         | <span data-ttu-id="e3790-209">2006-01-02</span><span class="sxs-lookup"><span data-stu-id="e3790-209">2006-01-02</span></span>         |
|                |               | <span data-ttu-id="e3790-210">2006-01-05</span><span class="sxs-lookup"><span data-stu-id="e3790-210">2006-01-05</span></span>         |
|                | <span data-ttu-id="e3790-211">Zara</span><span class="sxs-lookup"><span data-stu-id="e3790-211">Zara</span></span>          | <span data-ttu-id="e3790-212">2007-06-02</span><span class="sxs-lookup"><span data-stu-id="e3790-212">2007-06-02</span></span>         |
|                |               | <span data-ttu-id="e3790-213">2007-09-10</span><span class="sxs-lookup"><span data-stu-id="e3790-213">2007-09-10</span></span>         |
| <span data-ttu-id="e3790-214">comunicaciones</span><span class="sxs-lookup"><span data-stu-id="e3790-214">communications</span></span> | <span data-ttu-id="e3790-215">Abner</span><span class="sxs-lookup"><span data-stu-id="e3790-215">Abner</span></span>         | <span data-ttu-id="e3790-216">2006-04-16</span><span class="sxs-lookup"><span data-stu-id="e3790-216">2006-04-16</span></span>         |
|                | <span data-ttu-id="e3790-217">José</span><span class="sxs-lookup"><span data-stu-id="e3790-217">Jean</span></span>          | <span data-ttu-id="e3790-218">2007-02-20</span><span class="sxs-lookup"><span data-stu-id="e3790-218">2007-02-20</span></span>         |
|                | <span data-ttu-id="e3790-219">Willa</span><span class="sxs-lookup"><span data-stu-id="e3790-219">Willa</span></span>         | <span data-ttu-id="e3790-220">2006-10-15</span><span class="sxs-lookup"><span data-stu-id="e3790-220">2006-10-15</span></span>         |
|                | <span data-ttu-id="e3790-221">Zara</span><span class="sxs-lookup"><span data-stu-id="e3790-221">Zara</span></span>          | <span data-ttu-id="e3790-222">2008-01-02</span><span class="sxs-lookup"><span data-stu-id="e3790-222">2008-01-02</span></span>         |



 

 

## <a name="grouping-on-vector-properties"></a><span data-ttu-id="e3790-223">Agrupar en propiedades de vector</span><span class="sxs-lookup"><span data-stu-id="e3790-223">Grouping on Vector Properties</span></span>

<span data-ttu-id="e3790-224">Agrupar en propiedades de Vector, propiedades que pueden contener uno o varios valores simultáneamente, compara los valores de vector individualmente de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e3790-224">Grouping on vector properties, properties that can contain one or more values simultaneously, compares the vector values individually by default.</span></span> <span data-ttu-id="e3790-225">Por ejemplo, si hay un documento, Lorem.docx, con la propiedad System. Author como "Theresa;" Zara "y otro documento, Ipsum.docx, con la propiedad System. Author como" Zara ", la consulta devuelve el conjunto de resultados en dos grupos, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="e3790-225">For example, if there is one document, Lorem.docx, with the System.Author property as "Theresa;Zara" and another document, Ipsum.docx, with the System.Author property as "Zara", the query returns the result set in two groups as shown here:</span></span>


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| <span data-ttu-id="e3790-226">System.Author</span><span class="sxs-lookup"><span data-stu-id="e3790-226">System.Author</span></span> | <span data-ttu-id="e3790-227">System. FileName</span><span class="sxs-lookup"><span data-stu-id="e3790-227">System.FileName</span></span> |
|---------------|-----------------|
| <span data-ttu-id="e3790-228">Theresa</span><span class="sxs-lookup"><span data-stu-id="e3790-228">Theresa</span></span>       | <span data-ttu-id="e3790-229">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-229">Lorem.docx</span></span>      |
| <span data-ttu-id="e3790-230">Zara</span><span class="sxs-lookup"><span data-stu-id="e3790-230">Zara</span></span>          | <span data-ttu-id="e3790-231">Lorem.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-231">Lorem.docx</span></span>      |
|               | <span data-ttu-id="e3790-232">Ipsum.docx</span><span class="sxs-lookup"><span data-stu-id="e3790-232">Ipsum.docx</span></span>      |



 

<span data-ttu-id="e3790-233">Como puede ver, la agrupación en propiedades de vector devuelve filas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="e3790-233">As you can see, grouping on vector properties returns duplicate rows.</span></span> <span data-ttu-id="e3790-234">Lorem.docx aparece dos veces porque tiene dos autores.</span><span class="sxs-lookup"><span data-stu-id="e3790-234">Lorem.docx appears twice because it has two authors.</span></span>

 

## <a name="more-examples"></a><span data-ttu-id="e3790-235">Más ejemplos</span><span class="sxs-lookup"><span data-stu-id="e3790-235">More Examples</span></span>


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a><span data-ttu-id="e3790-236">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3790-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3790-237">Funciones de agregado</span><span class="sxs-lookup"><span data-stu-id="e3790-237">Aggregate Functions</span></span>](-search-sql-aggregates.md)
</dt> <dt>

[<span data-ttu-id="e3790-238">Cláusula ORDER BY</span><span class="sxs-lookup"><span data-stu-id="e3790-238">ORDER BY Clause</span></span>](-search-sql-orderby.md)
</dt> <dt>

[<span data-ttu-id="e3790-239">ORDER IN GROUP (cláusula)</span><span class="sxs-lookup"><span data-stu-id="e3790-239">ORDER IN GROUP Clause</span></span>](-search-sql-orderingroup.md)
</dt> </dl>

 

 
