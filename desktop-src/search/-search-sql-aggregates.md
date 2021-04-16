---
description: Una función de agregado realiza un cálculo en un conjunto de valores y devuelve un valor. Si lo hace, es posible generar estadísticas de resumen para los grupos de varios niveles con poca sobrecarga.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funciones de agregado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570305"
---
# <a name="aggregate-functions"></a><span data-ttu-id="3ce8a-104">Funciones de agregado</span><span class="sxs-lookup"><span data-stu-id="3ce8a-104">Aggregate Functions</span></span>

<span data-ttu-id="3ce8a-105">Una función de agregado realiza un cálculo en un conjunto de valores y devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-105">An aggregate function performs a calculation on a set of values and returns a value.</span></span> <span data-ttu-id="3ce8a-106">Si lo hace, es posible generar estadísticas de resumen para los grupos de varios niveles con poca sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-106">Doing so makes it possible to generate summary statistics for multi-level groups with little overhead.</span></span>

## <a name="about-aggregate-functions"></a><span data-ttu-id="3ce8a-107">Acerca de las funciones de agregado</span><span class="sxs-lookup"><span data-stu-id="3ce8a-107">About Aggregate Functions</span></span>

<span data-ttu-id="3ce8a-108">Las funciones de agregado en Lenguaje de consulta estructurado de Windows Search (SQL) tienen la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="3ce8a-108">Aggregate functions in Windows Search Structured Query Language (SQL) have the following syntax:</span></span>


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



<span data-ttu-id="3ce8a-109">La parte de la función puede incluir cualquiera de las siguientes funciones y sintaxis:</span><span class="sxs-lookup"><span data-stu-id="3ce8a-109">The function portion can include any of the following functions and syntax:</span></span>



| <span data-ttu-id="3ce8a-110">Función</span><span class="sxs-lookup"><span data-stu-id="3ce8a-110">Function</span></span>                                                              | <span data-ttu-id="3ce8a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ce8a-111">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce8a-112">AVG ( <column> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-112">AVG(<column>)</span></span>                                                   | <span data-ttu-id="3ce8a-113">Devuelve el promedio de los valores de un grupo.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-113">Returns the average of the values in a group.</span></span> <span data-ttu-id="3ce8a-114">Solo se aplica a números.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-114">Applies only to numbers.</span></span>                                                                                                                                      |
| <span data-ttu-id="3ce8a-115">BYFREQUENCY ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-115">BYFREQUENCY(<column>, <N>)</span></span>                                | <span data-ttu-id="3ce8a-116">Devuelve los valores de columna N más frecuentes de los resultados del grupo.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-116">Returns the most frequent N column values from the results in the group.</span></span> <span data-ttu-id="3ce8a-117">También incluye un recuento del número de veces que se produjo cada valor y los identificadores de documento de los resultados que contienen cada valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-117">Also includes a count of how many times each value occurred and document identifiers for results that contain each returned value.</span></span> |
| <span data-ttu-id="3ce8a-118">CHILDCOUNT ()</span><span class="sxs-lookup"><span data-stu-id="3ce8a-118">CHILDCOUNT()</span></span>                                                          | <span data-ttu-id="3ce8a-119">Devuelve el número de elementos de un grupo (sin incluir los subgrupos).</span><span class="sxs-lookup"><span data-stu-id="3ce8a-119">Returns the number of items in a group (excluding subgroups).</span></span> <span data-ttu-id="3ce8a-120">Si hay varios niveles de agrupación, devuelve el número de grupos secundarios inmediatos.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-120">If there are multiple levels of grouping, this returns the number of immediate child groups.</span></span>                                                  |
| <span data-ttu-id="3ce8a-121">COUNT ()</span><span class="sxs-lookup"><span data-stu-id="3ce8a-121">COUNT()</span></span>                                                               | <span data-ttu-id="3ce8a-122">Devuelve el número de elementos de un grupo y todos los subgrupos.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-122">Returns the number of items in a group and all subgroups.</span></span>                                                                                                                                                   |
| <span data-ttu-id="3ce8a-123">DATERANGE ( <column> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-123">DATERANGE(<column>)</span></span>                                             | <span data-ttu-id="3ce8a-124">Devuelve los límites inferior y superior de los valores de columna que se encuentran en el grupo de resultados del grupo.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-124">Returns the lower and upper bounds of the column values found in the group results group.</span></span> <span data-ttu-id="3ce8a-125">Solo es válido para las propiedades de FILETIME.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-125">Valid only for filetime properties.</span></span>                                                                               |
| <span data-ttu-id="3ce8a-126">PRIMERO ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-126">FIRST(<column>, <N>)</span></span>                                      | <span data-ttu-id="3ce8a-127">Devuelve los N primeros valores de columna de los resultados hoja encontrados en un grupo.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-127">Returns the first N column values from leaf results found in a group.</span></span>                                                                                                                                       |
| <span data-ttu-id="3ce8a-128">MAX ( <column> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-128">MAX(<column>)</span></span>                                                   | <span data-ttu-id="3ce8a-129">Devuelve el valor máximo de la expresión.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-129">Returns the maximum value in the expression.</span></span> <span data-ttu-id="3ce8a-130">Solo se aplica a números o fechas.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-130">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="3ce8a-131">MIN ( <column> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-131">MIN(<column>)</span></span>                                                   | <span data-ttu-id="3ce8a-132">Devuelve el valor mínimo de la expresión.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-132">Returns the minimum value in the expression.</span></span> <span data-ttu-id="3ce8a-133">Solo se aplica a números o fechas.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-133">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="3ce8a-134">Representador ( <column> , <idRepresentative> , <N> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-134">REPRESENTATIVEOF(<column>, <idRepresentative>, <N>)</span></span> | <span data-ttu-id="3ce8a-135">Devuelve N valores idRepresentative, cada uno de los cuales se selecciona de uno de los subconjuntos de resultados que tiene un valor de columna único.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-135">Returns N idRepresentative values, each selected from one of the result subsets that has a unique column value.</span></span> <span data-ttu-id="3ce8a-136">Cada valor también se devuelve con un identificador de documento que tiene el valor idRepresentative.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-136">Each value is also returned with a document identifier that has the idRepresentative value.</span></span> |
| <span data-ttu-id="3ce8a-137">SUM ( <column> )</span><span class="sxs-lookup"><span data-stu-id="3ce8a-137">SUM(<column>)</span></span>                                                   | <span data-ttu-id="3ce8a-138">Devuelve la suma de los valores de un grupo.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-138">Returns the sum of the values in a group.</span></span> <span data-ttu-id="3ce8a-139">Solo se aplica a números.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-139">Applies only to numbers.</span></span>                                                                                                                                          |



 

 

> [!Note]  
> <span data-ttu-id="3ce8a-140">Los agregados se devuelven como columnas individuales.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-140">Aggregates are returned as individual columns.</span></span> <span data-ttu-id="3ce8a-141">Son principalmente tipos simples, excepto ByFrequency, First, DateRange y representativo, que se devuelven como tipos compuestos.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-141">They are mostly simple types except for ByFrequency, First, DateRange, and RepresentativeOf which are returned as compound types.</span></span>

 

<span data-ttu-id="3ce8a-142">Puede usar cualquier columna numérica o de fecha para las agregaciones, y no solo las que se encuentran en la cláusula SELECT.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-142">You can use any numeric or date column for aggregations, and not only those that are in the SELECT clause.</span></span> <span data-ttu-id="3ce8a-143">Sin embargo, no se puede agrupar en agregados.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-143">However, you cannot group on aggregates.</span></span> <span data-ttu-id="3ce8a-144">Si el argumento de columna pasado no es un tipo numérico o de fecha, se devuelve un error de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-144">A syntax error is returned if the column argument passed in is not either a numeric or date type.</span></span>

<span data-ttu-id="3ce8a-145">La parte de la etiqueta es opcional y proporciona un alias más legible para la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-145">The label portion is optional and provides a more readable alias for the label.</span></span> <span data-ttu-id="3ce8a-146">Si no incluye una etiqueta de alias, Windows Search transforma el nombre de la función y de la columna en una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-146">If you do not include an alias label, then Windows Search transforms the function and column name into a label.</span></span> <span data-ttu-id="3ce8a-147">Por ejemplo, MAX (System.Document. WordCount) se convierte en MAX \_ SystemDocumentWordCount.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-147">For example, MAX(System.Document.WordCount) becomes MAX\_SystemDocumentWordCount.</span></span>

## <a name="multi-level-groups-and-counting"></a><span data-ttu-id="3ce8a-148">Agrupación y recuento de varios niveles</span><span class="sxs-lookup"><span data-stu-id="3ce8a-148">Multi-level Groups and Counting</span></span>

<span data-ttu-id="3ce8a-149">Los agregados se definen en hojas y se duplican.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-149">Aggregates are defined over leaves and are duplicated.</span></span> <span data-ttu-id="3ce8a-150">Un agregado toma como entrada las hojas del grupo que lo define (documentos), en lugar de los subgrupos de sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-150">An aggregate takes as input the leaves of the group that defines it (documents), rather than the subgroups of its children.</span></span> <span data-ttu-id="3ce8a-151">Esta funcionalidad se conoce como agrupación de varios niveles.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-151">This functionality is referred to as multi-level grouping.</span></span>

<span data-ttu-id="3ce8a-152">Además de los agregados que se definen en hojas y duplicados, se cuentan solo una vez.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-152">In addition to aggregates being defined over leaves and duplicated, they are counted only once.</span></span> <span data-ttu-id="3ce8a-153">Aunque el mismo documento puede representarse varias veces en un grupo, los agregados solo lo considerarían una vez.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-153">While the same document might be represented multiple times under one group, aggregates would only consider it once.</span></span> <span data-ttu-id="3ce8a-154">En el siguiente gráfico se ilustra este concepto.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-154">The following graphic illustrates this concept.</span></span>

![diagrama que muestra que los agregados se definen en hojas y se duplican, y se cuentan solo una vez](images/aggregates.png)

## <a name="aggregate-examples"></a><span data-ttu-id="3ce8a-156">Ejemplos de agregado</span><span class="sxs-lookup"><span data-stu-id="3ce8a-156">Aggregate Examples</span></span>

<span data-ttu-id="3ce8a-157">A continuación se muestran ejemplos de funciones de agregado dentro de la cláusula GROUP ON:</span><span class="sxs-lookup"><span data-stu-id="3ce8a-157">The following are examples of aggregate functions within the GROUP ON clause:</span></span>


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a><span data-ttu-id="3ce8a-158">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ce8a-158">Return Value</span></span>

<span data-ttu-id="3ce8a-159">El valor devuelto es una variante que se encuentra en el conjunto de filas como una propiedad personalizada, ya sea como alias especificados o como "agregados" si no se especifica ninguna etiqueta de alias.</span><span class="sxs-lookup"><span data-stu-id="3ce8a-159">The return value is a variant found on the rowset as a custom property, either as the specified aliases or as "Aggregates" if no alias label is specified.</span></span>

 

 



