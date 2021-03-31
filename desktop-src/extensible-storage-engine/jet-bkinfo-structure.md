---
description: 'Más información acerca de: estructura de JET_BKINFO'
title: Estructura de JET_BKINFO
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
ms.openlocfilehash: 6c4849c23e742657d8f5eaba8a030426f7a2a440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278676"
---
# <a name="jet_bkinfo-structure"></a>Estructura de JET_BKINFO


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_bkinfo-structure"></a>Estructura de JET_BKINFO

La estructura **JET_BKINFO** contiene una colección de datos acerca de un evento de copia de seguridad específico.

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

El ID. de esta copia de seguridad.

**logtimeMark**

Hora de este evento de copia de seguridad.

**bklogtimeMark**

Hora de este evento de copia de seguridad, con bits adicionales para indicar una copia de seguridad de instantánea.

**Windows Vista: bklogtimeMark** se presentó en Windows Vista.

**genLow**

Número de generación de registro bajo asociado a este evento de copia de seguridad.

**genHigh**

Número de generación de registro alto asociado a este evento de copia de seguridad.

### <a name="remarks"></a>Observaciones

Esta estructura se utiliza dentro de la estructura [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) para representar datos sobre el evento de copia de seguridad de base de datos.

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

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
