---
description: El predicado LIKE realiza una comparación de coincidencia de patrones en la columna especificada.
ms.assetid: d4bcf406-1253-4e56-b770-79edd4a98205
title: LIKE (predicado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba042fb2fe3005e062e7961a048a81a64c0c144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720329"
---
# <a name="like-predicate"></a><span data-ttu-id="59f21-103">LIKE (predicado)</span><span class="sxs-lookup"><span data-stu-id="59f21-103">LIKE Predicate</span></span>

<span data-ttu-id="59f21-104">El predicado LIKE realiza una comparación de coincidencia de patrones en la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="59f21-104">The LIKE predicate performs pattern-matching comparison on the specified column.</span></span> <span data-ttu-id="59f21-105">Utiliza la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="59f21-105">It uses the following syntax:</span></span>


```
...WHERE <column> LIKE '<wildcard_literal>'
```



<span data-ttu-id="59f21-106"><column>Puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado.</span><span class="sxs-lookup"><span data-stu-id="59f21-106">The <column> can be a regular or delimited [identifier](-search-sql-identifiers.md).</span></span> <span data-ttu-id="59f21-107">La columna está limitada a las propiedades del almacén de propiedades.</span><span class="sxs-lookup"><span data-stu-id="59f21-107">The column is limited to the properties in the property store.</span></span>

<span data-ttu-id="59f21-108">El <literal de carácter comodín \_> es un literal de cadena.</span><span class="sxs-lookup"><span data-stu-id="59f21-108">The <wildcard\_literal> is a string literal.</span></span> <span data-ttu-id="59f21-109">Está entre comillas y, opcionalmente, puede contener caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="59f21-109">It is enclosed in quotation marks and optionally can contain wildcard characters.</span></span> <span data-ttu-id="59f21-110">La cadena de coincidencia puede contener varios caracteres comodín si es necesario.</span><span class="sxs-lookup"><span data-stu-id="59f21-110">The match string can contain multiple wildcard characters if needed.</span></span> <span data-ttu-id="59f21-111">En la tabla siguiente se describen los caracteres comodín que reconoce el predicado LIKE.</span><span class="sxs-lookup"><span data-stu-id="59f21-111">The following table describes the wildcard characters that the LIKE predicate recognizes.</span></span>



| <span data-ttu-id="59f21-112">Wildcard (Carácter comodín)</span><span class="sxs-lookup"><span data-stu-id="59f21-112">Wildcard</span></span>                | <span data-ttu-id="59f21-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="59f21-113">Description</span></span>                                                                                                                                                                                     | <span data-ttu-id="59f21-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59f21-114">Example</span></span>                                                                                                                                                                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f21-115">% (porcentaje)</span><span class="sxs-lookup"><span data-stu-id="59f21-115">% (percent)</span></span>             | <span data-ttu-id="59f21-116">Coincide con cero o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="59f21-116">Matches zero or more of any characters.</span></span>                                                                                                                                                         | <span data-ttu-id="59f21-117">' COMP% r ' coincide con ' Comp ' seguido de cero o más caracteres, terminando en r.</span><span class="sxs-lookup"><span data-stu-id="59f21-117">'comp%r' matches 'comp' followed by zero or more of any characters, ending in an r.</span></span>                                                                                                                                  |
| <span data-ttu-id="59f21-118">\_ (subrayado)</span><span class="sxs-lookup"><span data-stu-id="59f21-118">\_ (underscore)</span></span>         | <span data-ttu-id="59f21-119">Coincidencia con cualquier carácter individual.</span><span class="sxs-lookup"><span data-stu-id="59f21-119">Matches any single character.</span></span>                                                                                                                                                                   | <span data-ttu-id="59f21-120">' COMP \_ ter ' coincide con ' Comp ' seguido de exactamente un carácter, seguido de ' ter '.</span><span class="sxs-lookup"><span data-stu-id="59f21-120">'comp\_ter' matches 'comp' followed by exactly one of any character, followed by 'ter'.</span></span>                                                                                                                              |
| <span data-ttu-id="59f21-121">\[\](corchetes)</span><span class="sxs-lookup"><span data-stu-id="59f21-121">\[ \] (square brackets)</span></span> | <span data-ttu-id="59f21-122">Coincide con cualquier carácter individual del intervalo o conjunto especificado.</span><span class="sxs-lookup"><span data-stu-id="59f21-122">Matches any single character within the specified range or set.</span></span> <span data-ttu-id="59f21-123">Por ejemplo, \[ a-z \] especifica un intervalo; \[ AEIOU \] especifica el conjunto de vocales.</span><span class="sxs-lookup"><span data-stu-id="59f21-123">For example, \[a-z\] specifies a range; \[aeiou\] specifies the set of vowels.</span></span>                                                  | <span data-ttu-id="59f21-124">' COMP \[ a-z \] re ' coincide con ' Comp ' seguido de un solo carácter en el intervalo de la a a la z, seguido de ' is '.</span><span class="sxs-lookup"><span data-stu-id="59f21-124">'comp\[a-z\]re' matches 'comp' followed by a single character in the range of a through z, followed by 're'.</span></span> <span data-ttu-id="59f21-125">' COMP \[ AO \] ' coincide con ' Comp ' seguido de un carácter único que debe ser un o un o.</span><span class="sxs-lookup"><span data-stu-id="59f21-125">'comp\[ao\]' matches 'comp' followed by a single character that must be either an a or an o.</span></span><br/> |
| <span data-ttu-id="59f21-126">\[^ \] intercalación</span><span class="sxs-lookup"><span data-stu-id="59f21-126">\[^ \] (caret)</span></span>          | <span data-ttu-id="59f21-127">Coincide con cualquier carácter individual que no esté dentro del intervalo o conjunto especificado.</span><span class="sxs-lookup"><span data-stu-id="59f21-127">Matches any single character that is not within the specified range or set.</span></span> <span data-ttu-id="59f21-128">Por ejemplo, \[ ^ a-z \] especifica un intervalo que excluye de la a a la z; \[ ^ AEIOU \] especifica un conjunto que excluye las vocales.</span><span class="sxs-lookup"><span data-stu-id="59f21-128">For example, \[^a-z\] specifies a range that excludes a through z; \[^aeiou\] specifies a set that excludes vowels.</span></span> | <span data-ttu-id="59f21-129">' COMP \[ ^ u \] ' coincide con ' Comp ' seguido de cualquier carácter individual que no sea un u.</span><span class="sxs-lookup"><span data-stu-id="59f21-129">'comp\[^u\]' matches 'comp' followed by any single character that is not a u.</span></span>                                                                                                                                        |



 

<span data-ttu-id="59f21-130">Si crea predicados con varios intervalos, los intervalos deben estar en orden.</span><span class="sxs-lookup"><span data-stu-id="59f21-130">If you create predicates with multiple ranges, the ranges must be in order.</span></span>

> [!Note]  
> <span data-ttu-id="59f21-131">Para buscar coincidencias con los caracteres comodín como caracteres literales para buscar coincidencias y no como caracteres comodín, coloque el carácter entre corchetes.</span><span class="sxs-lookup"><span data-stu-id="59f21-131">To match the wildcard characters as literal characters for matching and not as wildcard characters, place the character inside square brackets.</span></span> <span data-ttu-id="59f21-132">Por ejemplo, para que coincida con el signo de porcentaje, use ' \[ % \] '.</span><span class="sxs-lookup"><span data-stu-id="59f21-132">For example, to match the percent sign, use '\[%\]'</span></span>

 

## <a name="examples"></a><span data-ttu-id="59f21-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="59f21-133">Examples</span></span>


```
...WHERE System.ItemNameDisplay LIKE 'financ%'
```



## <a name="related-topics"></a><span data-ttu-id="59f21-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59f21-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="59f21-135">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="59f21-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="59f21-136">Comparación de valores literales</span><span class="sxs-lookup"><span data-stu-id="59f21-136">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="59f21-137">Comparaciones de varios valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="59f21-137">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="59f21-138">Predicado NULL</span><span class="sxs-lookup"><span data-stu-id="59f21-138">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="59f21-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="59f21-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="59f21-140">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="59f21-140">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="59f21-141">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="59f21-141">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 




