---
description: El predicado NULL indica si el documento tiene un valor para la columna indicada.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: Predicado NULL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd80ea6cba2009b398c8cdd0a2926240e3ce78309ca3f8511fb6ba286f44a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058125"
---
# <a name="null-predicate"></a>Predicado NULL

El **predicado NULL** indica si el documento tiene un valor para la columna indicada.

El **predicado NULL** tiene la sintaxis siguiente:


```
...WHERE <column> IS [NOT] NULL
```



La palabra clave NOT opcional nega el resultado. La columna puede ser un identificador normal o [delimitado.](-search-sql-identifiers.md)

> [!IMPORTANT]
> Para probar si una columna tiene el **valor NULL,** debe usar el predicado **NULL.** No es válido usar el valor **NULL** en un predicado de comparación. "WHERE column IS **NULL"** es correcto. "WHERE column = **NULL"** no es válido.

 

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se devuelven documentos que no tienen un valor System.Video.Director.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Predicado LIKE](-search-sql-like.md)
</dt> <dt>

[Comparación de valores literales](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Comparaciones multivalor (ARRAY)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Predicados de texto completo](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicados que no son de texto completo](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



