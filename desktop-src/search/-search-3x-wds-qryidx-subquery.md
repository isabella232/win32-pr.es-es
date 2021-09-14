---
description: Obtenga información sobre el argumento SUBQUERY en Windows Search. Una subconsulta es un archivo de búsqueda guardado que puede usar como filtro para una nueva consulta.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argumento SUBQUERY (Windows search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363267"
---
# <a name="subquery-argument-windows-search"></a>Argumento SUBQUERY (Windows search)

Una subconsulta es un archivo de búsqueda guardado (.search-ms) que puede usar como \* filtro para una nueva consulta. Los resultados de la subconsulta se usan como origen de la nueva consulta. Por ejemplo, supongamos que tiene varios archivos de búsqueda guardados que restringen una consulta por lista de distribución de correo electrónico: mydepartment.search-ms, teamproject.search-ms y corporatewide.search-ms. El uso `subquery` del argumento permite limitar las búsquedas de correo electrónico a cualquiera de estas búsquedas guardadas o a todas ellas.

Este tema se organiza de la siguiente manera:

-   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="example"></a>Ejemplo


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con Parameter-Value argumentos](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos del identificador de configuración regional](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento CRUMB](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argumento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



