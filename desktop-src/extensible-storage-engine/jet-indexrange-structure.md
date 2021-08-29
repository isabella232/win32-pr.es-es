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
ms.openlocfilehash: 97a3447ae17d3d34f2df3afcd92c47ec49f7f97b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984238"
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

Cursor que anteriormente tenía un intervalo de índice establecido [con JetSetIndexRange.](./jetsetindexrange-function.md)

**grbit**

Máscara de bits compuesta de exactamente una de las siguientes.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRecordInIndex</p> | <p>Especifica que el intervalo de índice se debe tratar con normalidad.</p> | 
| <p>JET_bitRecordNotInIndex</p> | <p>Reservado para uso futuro. No debe usarse.</p> | 



### <a name="remarks"></a>Observaciones

Cada **JET_INDEXRANGE** estructura que se pasa a [JetIntersectIndexes](./jetintersectindexes-function.md) representa un intervalo de índice, que se intersecrá con la llamada API. El cursor que se da en **JET_INDEXRANGE** debe tener un intervalo de índice válido establecido en él ya, con una llamada correcta a [JetSetIndexRange](./jetsetindexrange-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
