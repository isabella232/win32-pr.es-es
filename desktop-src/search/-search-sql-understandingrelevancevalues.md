---
description: En una base de datos relacional, las filas devueltas por una consulta de búsqueda deben cumplir todas las condiciones llamadas por la consulta. En cambio, una consulta Windows Search puede devolver documentos que cumplan las condiciones de búsqueda en distintos grados.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Descripción de los valores de relevancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d28efba26d12e0260d76e02fc4e042e72612df34d383a0e22a34f4be9d9fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226810"
---
# <a name="understanding-relevance-values"></a>Descripción de los valores de relevancia

En una base de datos relacional, las filas devueltas por una consulta de búsqueda deben cumplir todas las condiciones llamadas por la consulta. En cambio, una consulta Windows Search puede devolver documentos que cumplan las condiciones de búsqueda en distintos grados.

Por ejemplo, una búsqueda del término "programa" en una base de datos relacional genera registros que contienen esa ortografía específica de la palabra. Si un registro contiene una o cien instancias de la palabra no tiene ningún impacto en los resultados. Por el contrario, Windows search devuelve un valor de relevancia asociado a los documentos correspondientes. La relevancia de los documentos que tienen "programa" en el título es mayor que las que contienen la palabra solo en el último párrafo. De forma similar, los documentos que contienen variaciones del término de búsqueda, por ejemplo , "programas" y "programación" también coinciden y son devueltos por la consulta.

Windows Las consultas de búsqueda devuelven valores de relevancia de enteros en la columna denominada "rank".

Asimismo:

-   Los valores de rango devueltos por la consulta son enteros comprendidos entre 0 y 1000.
-   Los valores de rango superiores indican documentos que coinciden mejor con las condiciones de búsqueda.
-   Los valores de clasificación solo se aplican a la consulta actual, por lo que no se pueden comparar con los resultados de las consultas.
-   Los valores de rango son relativos a los demás documentos que coinciden con la consulta. Por lo tanto, el valor de clasificación de un documento determinado depende de los demás documentos que también coinciden con la consulta.
-   Los valores de clasificación de los elementos que coinciden con un predicado puramente relacional son 1000.

Puede manipular los valores de rango devueltos mediante ponderaciones de columna en los predicados de cláusula [CONTAINS](-search-sql-contains.md) y [FREETEXT](-search-sql-freetext.md) WHERE y la cláusula RANK BY.

 

 



