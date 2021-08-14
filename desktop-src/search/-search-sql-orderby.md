---
description: 'Más información sobre: Cláusula ORDER BY'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: Cláusula ORDER BY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3815ddecc659a47d7cf2c8547b49e878c54ba6bf8537e2589eea4441d9d3f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227190"
---
# <a name="order-by-clause"></a>Cláusula ORDER BY

La cláusula ORDER BY ordena los resultados en función del valor de una o varias columnas que especifique. A continuación se muestra la sintaxis de la cláusula ORDER BY:


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



El especificador de columna debe ser una columna válida. Puede usar el especificador de columna para hacer referencia a las columnas según el orden en que aparecen en la consulta. La primera columna de la consulta tiene el número 1. Puede incluir más de una columna en la cláusula ORDER BY, separada por comas.

El especificador de dirección opcional puede ser "ASC" para ascendente (de baja a alta) o "DESC" para descendente (de alto a bajo). Si no proporciona un especificador de dirección, se usa el valor predeterminado, ascendente. Si especifica más de una columna, pero no especifica todas las direcciones, la dirección que especifique en último lugar se aplicará a cada columna hasta que cambie explícitamente la dirección.

Por ejemplo, en la siguiente cláusula ORDER BY, las columnas A, B, C y G se ordenan en orden ascendente, mientras que las columnas D, E y F se ordenan en orden descendente.


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[From (cláusula)](-search-sql-from.md)
</dt> <dt>

[RANK BY (cláusula)](-search-sql-rankby.md)
</dt> <dt>

[Instrucción SELECT](-search-sql-select.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



