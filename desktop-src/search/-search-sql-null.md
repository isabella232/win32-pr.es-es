---
description: El predicado NULL indica si el documento tiene un valor para la columna indicada.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicado NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705480"
---
# <a name="null-predicate"></a>Predicado NULL

El predicado **null** indica si el documento tiene un valor para la columna indicada.

El predicado **null** tiene la siguiente sintaxis:


```
...WHERE <column> IS [NOT] NULL
```



La palabra clave NOT opcional niega el resultado. La columna puede ser un [identificador](-search-sql-identifiers.md)normal o delimitado.

> [!IMPORTANT]
> Para comprobar si una columna tiene el valor **null** , debe usar el predicado **null** . No es válido usar el valor **null** en un predicado de comparación. "Donde la columna es **null**" es correcta. "WHERE Column = **null**" no es válido.

 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se devuelven documentos que no tienen un valor System. video. Director.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[LIKE (predicado)](-search-sql-like.md)
</dt> <dt>

[Comparación de valores literales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparaciones de varios valores (matriz)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



