---
description: 'Más información sobre: JET_LGPOS estructura'
title: JET_LGPOS estructura
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: abf3ca2996e75d2abfe6fc766ec6f5bbd30054eeb9dd8406fe2747307a00c4a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119109262"
---
# <a name="jet_lgpos-structure"></a>JET_LGPOS estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_lgpos-structure"></a>JET_LGPOS estructura

La **JET_LGPOS** contiene datos que son internos del mecanismo de registro del motor de base de datos. Esta estructura se considera interna.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Miembros

**Ib**

Admite la infraestructura ese y no se puede usar desde el código.

**Isec**

Admite la infraestructura ese y no se puede usar desde el código.

**lGeneration**

Admite la infraestructura ese y no se puede usar desde el código.

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

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
