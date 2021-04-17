---
description: 'Más información acerca de: estructura de JET_INDEXRANGE'
title: Estructura de JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716541"
---
# <a name="jet_indexrange-structure"></a>Estructura de JET_INDEXRANGE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_indexrange-structure"></a>Estructura de JET_INDEXRANGE

La estructura **JET_INDEXRANGE** identifica un intervalo de índice cuando se usa con la función [JetIntersectIndexes](./jetintersectindexes-function.md) .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño, en bytes, del **JET_INDEXRANGE**.

**TABLEID**

Un cursor que previamente tenía un intervalo de índice establecido con [JetSetIndexRange](./jetsetindexrange-function.md).

**grbit**

Máscara de código formada por exactamente uno de los siguientes elementos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRecordInIndex</p></td>
<td><p>Especifica que el intervalo de índice se debe tratar normalmente.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Reservado para uso futuro. No debe usarse.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Observaciones

Cada estructura de **JET_INDEXRANGE** que se pasa a [JetIntersectIndexes](./jetintersectindexes-function.md) representa un intervalo de índice, que se intersectará con la llamada a la API. El cursor que se proporciona en **JET_INDEXRANGE** debe tener un intervalo de índices válido establecido en él, con una llamada correcta a [JetSetIndexRange](./jetsetindexrange-function.md).

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
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
