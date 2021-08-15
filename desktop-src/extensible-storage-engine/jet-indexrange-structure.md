---
description: 'Más información sobre: JET_INDEXRANGE estructura'
title: JET_INDEXRANGE estructura
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
ms.openlocfilehash: b5b68e7ebf6df39757ab39947201b945e35a3ece85518a3cb202525033cdd214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485603"
---
# <a name="jet_indexrange-structure"></a>JET_INDEXRANGE estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_indexrange-structure"></a>JET_INDEXRANGE estructura

La **JET_INDEXRANGE** identifica un intervalo de índice cuando se usa con la [función JetIntersectIndexes.](./jetintersectindexes-function.md)

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

**tableid**

Cursor que anteriormente tenía un intervalo de índice establecido [con JetSetIndexRange](./jetsetindexrange-function.md).

**grbit**

Máscara de bits formada exactamente por una de las siguientes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRecordInIndex</p></td>
<td><p>Especifica que el intervalo de índice se debe tratar con normalidad.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>Reservado para uso futuro. No debe usarse.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Comentarios

Cada **JET_INDEXRANGE** estructura que se pasa a [JetIntersectIndexes](./jetintersectindexes-function.md) representa un intervalo de índice, que se intersecrá con la llamada API. El cursor que se da en **JET_INDEXRANGE** debe tener un intervalo de índice válido establecido en él, con una llamada correcta a [JetSetIndexRange](./jetsetindexrange-function.md).

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
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
