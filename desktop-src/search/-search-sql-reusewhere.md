---
description: La cláusula WHERE de una consulta especifica un conjunto de elementos con los que buscar coincidencias.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705477"
---
# <a name="reusewhere-function"></a>ReuseWhere función)

La cláusula [Where](-search-sql-where.md) de una consulta especifica un conjunto de elementos con los que buscar coincidencias. Las consultas posteriores pueden compartir el trabajo realizado para una consulta anterior mediante la función ReuseWhere en una nueva cláusula WHERE de consulta. Las consultas que aprovechan esta función se ejecutan más rápido.

## <a name="examples"></a>Ejemplos

En el escenario siguiente se muestra cómo usar la función ReuseWhere:

1.  Se emite la siguiente consulta:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  En el conjunto de filas devuelto, se obtiene un [identificador Where](-search-sql-rowset-properties.md), *Query1WhereID*.

    Donde ID es una propiedad de conjunto de filas con PROPSET {aa6ee6b0-e828-11d0-B2-3e-00-AA-00-47-FC-01}, PROPID 8 y Type UI4.

3.  Se emite una segunda consulta con la función ReuseWhere, pasando el *Query1WhereID* del paso 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

La segunda consulta es equivalente a la siguiente:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



Se puede usar la función ReuseWhere en la cláusula [Where](-search-sql-where.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Cláusula WHERE](-search-sql-where.md)
</dt> <dt>

[Propiedades del conjunto de filas](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



