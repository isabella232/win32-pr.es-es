---
description: La instrucción SET especifica las opciones PROPERTYNAME y RANKMETHOD para la consulta.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: SET (instrucción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153952"
---
# <a name="set-statement"></a><span data-ttu-id="671ac-103">SET (instrucción)</span><span class="sxs-lookup"><span data-stu-id="671ac-103">SET Statement</span></span>

<span data-ttu-id="671ac-104">La instrucción SET especifica las opciones PROPERTYNAME y RANKMETHOD para la consulta.</span><span class="sxs-lookup"><span data-stu-id="671ac-104">The SET statement specifies PROPERTYNAME and RANKMETHOD options for the query.</span></span>

## <a name="propertyname"></a><span data-ttu-id="671ac-105">PROPERTYNAME</span><span class="sxs-lookup"><span data-stu-id="671ac-105">PROPERTYNAME</span></span>

<span data-ttu-id="671ac-106">Puede asociar una propiedad a un alias descriptivo para la consulta mediante la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="671ac-106">You can associate a property with a friendly alias for the query by using the following syntax:</span></span>


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a><span data-ttu-id="671ac-107">RANKMETHOD</span><span class="sxs-lookup"><span data-stu-id="671ac-107">RANKMETHOD</span></span>

<span data-ttu-id="671ac-108">Puede especificar el método de rango para las consultas con el término ISABOUT con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="671ac-108">You can specify the rank method for queries with the ISABOUT term by using the following syntax:</span></span>


```
SET RANKMETHOD <rankmethod>      
```



<span data-ttu-id="671ac-109">Los métodos de RANKMETHOD que se pueden especificar mediante la instrucción SET son el coeficiente de JACCARD, el coeficiente de los dados y el producto interno.</span><span class="sxs-lookup"><span data-stu-id="671ac-109">The RANKMETHOD methods that can be specified by using the SET statement are JACCARD COEFFICIENT, DICE COEFFICIENT, and INNER PRODUCT.</span></span>

 

 



