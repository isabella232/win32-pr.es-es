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
# <a name="set-statement"></a>SET (instrucción)

La instrucción SET especifica las opciones PROPERTYNAME y RANKMETHOD para la consulta.

## <a name="propertyname"></a>PROPERTYNAME

Puede asociar una propiedad a un alias descriptivo para la consulta mediante la sintaxis siguiente:


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a>RANKMETHOD

Puede especificar el método de rango para las consultas con el término ISABOUT con la siguiente sintaxis:


```
SET RANKMETHOD <rankmethod>      
```



Los métodos de RANKMETHOD que se pueden especificar mediante la instrucción SET son el coeficiente de JACCARD, el coeficiente de los dados y el producto interno.

 

 



