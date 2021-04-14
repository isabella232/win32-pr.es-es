---
description: 'Más información acerca de: estructura de JET_ENUMCOLUMNID'
title: Estructura de JET_ENUMCOLUMNID
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541470"
---
# <a name="jet_enumcolumnid-structure"></a>Estructura de JET_ENUMCOLUMNID


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_enumcolumnid-structure"></a>Estructura de JET_ENUMCOLUMNID

La estructura **JET_ENUMCOLUMNID** enumera un conjunto específico de columnas y, opcionalmente, un conjunto específico de varios valores para esas columnas cuando se usa la función [JetEnumerateColumns](./jetenumeratecolumns-function.md) . [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de estructuras **JET_ENUMCOLUMNID** .

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>Miembros

**columnid**

IDENTIFICADOR de columna que se va a enumerar.

Si el ID. de columna es 0 (cero), la enumeración de esta columna se omite y se generará una ranura correspondiente en la matriz de salida de [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) estructuras con un estado de columna de JET_wrnColumnSkipped.

**ctagSequence**

Opcionalmente, identifica una matriz de valores de columna (por índice de base uno) que se va a enumerar para el ID. de columna especificado.

Si **ctagSequence** es 0 (cero), se omite **rgtagSequence** y se enumeran todos los valores de columna para el ID. de columna especificado.

Si un elemento de **rgtagSequence** es 0 (cero), se omitirá la enumeración de ese valor de columna (por índice basado en uno). Se generará una ranura correspondiente en la matriz de salida de la estructura **JET_ENUMCOLUMNID** con un valor de estado de columna de JET_wrnColumnSkipped.

**rgtagSequence**

Matriz de índices basados en uno en la matriz de valores de columna de una columna determinada. Un único elemento es un **itagSequence** que se define en [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md). Un valor de **itagSequence** de 0 (cero) significa "SKIP". Un **itagSequence** de 1 significa devolver el valor de la primera columna de la columna, 2 significa el segundo, etc.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
