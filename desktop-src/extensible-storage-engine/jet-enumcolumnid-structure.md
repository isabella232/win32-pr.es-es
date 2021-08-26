---
description: 'Más información sobre: JET_ENUMCOLUMNID estructura'
title: JET_ENUMCOLUMNID estructura
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21f28e160f1c31dac909e02bf64acba0ae230305
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479648"
---
# <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID estructura

La **JET_ENUMCOLUMNID** enumera un conjunto específico de columnas y, opcionalmente, un conjunto específico de varios valores para esas columnas cuando se usa la [función JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de **JET_ENUMCOLUMNID** estructuras.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Miembros

**columnid**

Identificador de columna que se enumerará.

Si el identificador de columna es 0 (cero), se omite la enumeración [](./jet-enumcolumn-structure.md) de esta columna y se genera una ranura correspondiente en la matriz de salida de estructuras JET_ENUMCOLUMN con un estado de columna de JET_wrnColumnSkipped.

**ctagSequence**

Opcionalmente, identifica una matriz de valores de columna (por índice basado en uno) para enumerar para el identificador de columna especificado.

Si **ctagSequence** es 0 (cero), se omite **rgtagSequence** y se enumerarán todos los valores de columna para el identificador de columna especificado.

Si un elemento de **rgtagSequence** es 0 (cero), se omitirá la enumeración de ese valor de columna (por índice basado en uno). Se generará una ranura correspondiente en la matriz **de salida JET_ENUMCOLUMNID** estructura con un valor de estado de columna de JET_wrnColumnSkipped.

**rgtagSequence**

Matriz de índices basados en uno en la matriz de valores de columna para una columna determinada. Un único elemento es **una itagSequence** que se define en [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Una **itagSequence** de 0 (cero) significa "skip". Una **itagSequence de** 1 significa devolver el primer valor de columna de la columna, 2 significa la segunda, y así sucesivamente.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
