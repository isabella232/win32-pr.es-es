---
description: Los alias de grupo de columnas proporcionan una manera de usar nombres más cortos en lugar del nombre de una columna o un grupo de columnas. El predicado de alias de grupo opcional forma parte de la cláusula WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: CON el predicado de alias de grupo AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808924"
---
# <a name="with----as-group-alias-predicate"></a><span data-ttu-id="8572f-104">CON el predicado de alias de grupo AS</span><span class="sxs-lookup"><span data-stu-id="8572f-104">WITH -- AS Group Alias Predicate</span></span>

<span data-ttu-id="8572f-105">Los alias de grupo de columnas proporcionan una manera de usar nombres más cortos en lugar del nombre de una columna o un grupo de columnas.</span><span class="sxs-lookup"><span data-stu-id="8572f-105">Column group aliases provide a way to use shorter names in place of the name of a column or a group of columns.</span></span> <span data-ttu-id="8572f-106">El predicado de alias de grupo opcional forma parte de la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="8572f-106">The optional group alias predicate is part of the WHERE clause.</span></span> <span data-ttu-id="8572f-107">Su sintaxis es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="8572f-107">Its syntax follows:</span></span>


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



<span data-ttu-id="8572f-108">Puede especificar más de un alias de grupo, separando la... COMO predicados por comas.</span><span class="sxs-lookup"><span data-stu-id="8572f-108">You can specify more than one group alias, separating the WITH...AS predicates by commas.</span></span>

<span data-ttu-id="8572f-109">Cuando se hace referencia a un alias de grupo en un predicado de la cláusula WHERE, la condición se aplica a cada columna del grupo.</span><span class="sxs-lookup"><span data-stu-id="8572f-109">When a group alias is referred to in a WHERE clause predicate, the condition is applied to each column in the group.</span></span> <span data-ttu-id="8572f-110">Los valores lógicos resultantes de la coincidencia de cada columna se combinan mediante el operador lógico **or** .</span><span class="sxs-lookup"><span data-stu-id="8572f-110">The logical values resulting from matching each column are combined by using the logical **OR** operator.</span></span>

<span data-ttu-id="8572f-111">Se debe definir un alias antes de poder usarlo y solo se puede usar dentro de la cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="8572f-111">An alias must be defined before it can be used, and it can be used only within the WHERE clause.</span></span> <span data-ttu-id="8572f-112">El nombre del alias debe ser un identificador normal precedido por un signo de almohadilla ( \# ) necesario.</span><span class="sxs-lookup"><span data-stu-id="8572f-112">The alias name must be a regular identifier preceded by a required pound sign (\#).</span></span>

<span data-ttu-id="8572f-113">El especificador de columna puede contener uno o más especificadores de columna, separados por comas.</span><span class="sxs-lookup"><span data-stu-id="8572f-113">The column specifier can contain one or more column specifiers, separated by commas.</span></span> <span data-ttu-id="8572f-114">La lista de columnas debe ir entre paréntesis y la ponderación se puede asignar a cada una.</span><span class="sxs-lookup"><span data-stu-id="8572f-114">The list of columns must be enclosed in parentheses and weighting can be assigned to each.</span></span> <span data-ttu-id="8572f-115">Cada columna tiene la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="8572f-115">Each column has the following syntax:</span></span>


```
<column_identifier> [<weight_assignment>]
```



<span data-ttu-id="8572f-116">Para obtener información sobre cómo especificar los pesos de las columnas, vea [predicado FREETEXT](-search-sql-freetext.md) and [Contains Predicate](-search-sql-contains.md).</span><span class="sxs-lookup"><span data-stu-id="8572f-116">For information on specifying column weights, see [FREETEXT Predicate](-search-sql-freetext.md) and [CONTAINS Predicate](-search-sql-contains.md).</span></span>

<span data-ttu-id="8572f-117">El identificador de columna puede ser normal o delimitado.</span><span class="sxs-lookup"><span data-stu-id="8572f-117">The column identifier can be regular or delimited.</span></span>

## <a name="examples"></a><span data-ttu-id="8572f-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8572f-118">Examples</span></span>

<span data-ttu-id="8572f-119">Los siguientes ejemplos de la cláusula WHERE muestran Cuándo y cómo se puede usar el predicado de alias de grupo.</span><span class="sxs-lookup"><span data-stu-id="8572f-119">The following WHERE clause examples demonstrate when and how you can use the group alias predicate.</span></span> <span data-ttu-id="8572f-120">EN el primer ejemplo se muestra una cláusula WHERE más repetitiva que no usa el alias de grupo.</span><span class="sxs-lookup"><span data-stu-id="8572f-120">The first example shows a more repetitive WHERE clause that does not use group aliasing.</span></span>


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



<span data-ttu-id="8572f-121">El ejemplo anterior se puede simplificar mediante el uso de un alias de grupo, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="8572f-121">The preceding example can be simplified by using a group alias, as shown in the following example.</span></span>


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="8572f-122">A continuación se ofrece un ejemplo de ponderación positiva en la que la propiedad **title** tiene más peso para determinar el rango relativo.</span><span class="sxs-lookup"><span data-stu-id="8572f-122">The following is an example of positive weighting where the **Title** property is given more weight in determining the relative rank.</span></span>


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="8572f-123">A continuación se proporciona un ejemplo de ponderación negativa donde no se tiene en cuenta la propiedad **title** con el peso de 0.</span><span class="sxs-lookup"><span data-stu-id="8572f-123">The following is an example of negative weighting where the **Title** property with weight of 0 is not considered.</span></span>


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a><span data-ttu-id="8572f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8572f-124">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8572f-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8572f-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8572f-126">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="8572f-126">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

<span data-ttu-id="8572f-127">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8572f-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8572f-128">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="8572f-128">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="8572f-129">Predicados que no son de texto completo</span><span class="sxs-lookup"><span data-stu-id="8572f-129">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



