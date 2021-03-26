---
description: Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta.
title: Argumento de subconsulta (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 43e4a5b904d5e769eb43acad05aa5d8ce37ebde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997885"
---
# <a name="subquery-argument-the-windows-shell"></a>Argumento de subconsulta (Shell de Windows)

Una subconsulta es un archivo de búsqueda guardado ( \* . Search-MS) que puede usar como filtro para una nueva consulta. Los resultados de la subconsulta se usan como origen de la nueva consulta. Por ejemplo, supongamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: Departamento. Search-MS, teamproject. Search-MS y corporatewide. Search-ms. El uso del `subquery` argumento le permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas.

## <a name="example"></a>Ejemplo


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Información de argumentos



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo mínimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 



