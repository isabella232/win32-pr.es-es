---
description: 'Más información acerca de: estructura de JET_LOGTIME'
title: Estructura de JET_LOGTIME
TOCTitle: JET_LOGTIME Structure
ms:assetid: cb7c0b74-db7a-4e48-80b8-37b3fdf6d088
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294089(v=EXCHG.10)
ms:contentKeyID: 32765704
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
ms.openlocfilehash: 9c99e2c1f77a01c33a75d3e5d16c4fe58c122a4e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821591"
---
# <a name="jet_logtime-structure"></a>Estructura de JET_LOGTIME


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_logtime-structure"></a>Estructura de JET_LOGTIME

La estructura **JET_LOGTIME** contiene elementos de la fecha y hora de un evento.

```cpp
typedef struct {
  char bSeconds;
  char bMinutes;
  char bHours;
  char bDay;
  char bMonth;
  char bYear;
  union {
    char bFiller1;
    struct {
        unsigned char fTimeIsUTC: 1;
        unsigned char fUnused: 7;
    };
  };
  char bFiller2;
} JET_LOGTIME;
```

### <a name="members"></a>Miembros

**bSeconds**

La hora del evento en segundos. Este valor puede ser de 0 a 59. se usa 0 cuando la estructura es NULL.

**bMinutes**

La hora del evento en minutos. Este valor puede ser de 0 a 59. se usa 0 cuando la estructura es NULL.

**bHours**

La hora del evento en horas. Este valor puede ser de 0 a 23. se usa 0 cuando la estructura es NULL.

**bDay**

Día del mes del evento. Este valor puede ser de 0 a 31. se usa 0 cuando la estructura es NULL.

**bMonth**

Mes del año del evento. Este valor puede ser de 0 a 12. se usa 0 cuando la estructura es NULL.

**bYear**

Año del evento (desplazamiento por 1900). Para lograr el año real, agregue 1900 a este valor. se usa 0 cuando la estructura es NULL.

**bFiller1**

Este campo debe omitirse.

**fTimeIsUTC**

La hora está en formato UTC.

**fUnused**

Este campo debe omitirse.

**bFiller2**

Este campo debe omitirse.

### <a name="remarks"></a>Observaciones

Esta estructura está pensada principalmente para el uso en la depuración.

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

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
