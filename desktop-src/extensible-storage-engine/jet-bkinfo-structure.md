---
description: 'Más información sobre: JET_BKINFO estructura'
title: JET_BKINFO estructura
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: 9f391d711c6d10c50cfdb26314be6ee709ff481bda0ce370faa28d514422444c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487870"
---
# <a name="jet_bkinfo-structure"></a>JET_BKINFO estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_bkinfo-structure"></a>JET_BKINFO estructura

La **JET_BKINFO** contiene una colección de datos sobre un evento de copia de seguridad específico.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Miembros

**lgposMark**

Identificador de esta copia de seguridad.

**logtimeMark**

Hora de este evento de copia de seguridad.

**bklogtimeMark**

Hora de este evento de copia de seguridad, con bits adicionales para indicar una copia de seguridad de instantáneas.

**Windows Vista: bklogtimeMark** se introdujo en Windows Vista.

**genLow**

Número de generación de registros bajo asociado a este evento de copia de seguridad.

**genHigh**

Número de generación de registros alto asociado a este evento de copia de seguridad.

### <a name="remarks"></a>Comentarios

Esta estructura se usa dentro de la estructura [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) para representar datos sobre el evento de copia de seguridad de la base de datos.

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
