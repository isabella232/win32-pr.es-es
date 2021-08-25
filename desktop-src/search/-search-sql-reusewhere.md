---
description: La cláusula WHERE de una consulta especifica un conjunto de elementos con los que se va a hacer coincidir los resultados.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere (Función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f073a7ac0d5faf5973d08ff53ccebdacf8bead080a53e2d9a4a6ae9ed5724db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944674"
---
# <a name="reusewhere-function"></a>ReuseWhere (Función)

La [cláusula WHERE](-search-sql-where.md) de una consulta especifica un conjunto de elementos con los que se va a hacer coincidir los resultados. Las consultas posteriores pueden compartir el trabajo realizado para una consulta anterior mediante la función ReuseWhere en una nueva cláusula WHERE de consulta. Las consultas que aprovechan esta función se ejecutan más rápido.

## <a name="examples"></a>Ejemplos

En el escenario siguiente se muestra cómo usar la función ReuseWhere:

1.  Emita la consulta siguiente:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  En el conjunto de filas devuelto, obtiene el [identificador Where](-search-sql-rowset-properties.md), *Query1WhereID*.

    Where ID es una propiedad de conjunto de filas con PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8 y el tipo UI4.

3.  Emita una segunda consulta con la función ReuseWhere y pase *query1WhereID* del paso 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

La segunda consulta es equivalente a la siguiente:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



La función ReuseWhere se puede usar en un lugar de la [cláusula WHERE.](-search-sql-where.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

[Propiedades del conjunto de filas](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



