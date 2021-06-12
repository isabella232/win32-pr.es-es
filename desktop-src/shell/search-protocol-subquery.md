---
description: Obtenga información sobre el argumento SUBQUERY en el Shell de Windows. Una subconsulta es un archivo de búsqueda guardado que puede usar como filtro para una nueva consulta.
title: Argumento SUBQUERY (Shell de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010668"
---
# <a name="subquery-argument-the-windows-shell"></a>Argumento SUBQUERY (Shell de Windows)

Una subconsulta es un archivo de búsqueda guardado (.search-ms) que puede usar como \* filtro para una nueva consulta. Los resultados de la subconsulta se usan como origen de la nueva consulta. Por ejemplo, digamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: mydepartment.search-ms, teamproject.search-ms y corporatewide.search-ms. El uso del `subquery` argumento permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas o a todas ellas.

## <a name="example"></a>Ejemplo


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Información de argumentos



|                          |                                         |
|--------------------------|-----------------------------------------|
| Sistema operativo mínimo | Windows Vista con Service Pack 1 (SP1) |



 

 

 



