---
description: 'Más información acerca de: estructura de JET_BKLOGTIME'
title: Estructura de JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME Structure
ms:assetid: 31460079-7c5b-4145-837d-b112ba0117d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269219(v=EXCHG.10)
ms:contentKeyID: 32765522
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
ms.openlocfilehash: 0b3ebfd1c0b807a491695ba18d6735e0230a16fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697532"
---
# <a name="jet_bklogtime-structure"></a>Estructura de JET_BKLOGTIME


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_bklogtime-structure"></a>Estructura de JET_BKLOGTIME

La estructura **JET_BKLOGTIME** contiene los elementos de fecha y hora de un evento. Es una extensión de [JET_LOGTIME](./jet-logtime-structure.md).

**Windows Vista: JET_BKLOGTIME** se incorpora en Windows Vista.

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
      union {
        char bFiller2;
        struct {
          unsigned char fOSSnapshot  :1;
          unsigned char fReserved  :7;
        };
      };
    } JET_BKLOGTIME;
```

### <a name="members"></a>Miembros

**bSeconds**

La hora del evento en segundos. Puede ser 0 (cero) a 60. se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".

**bMinutes**

La hora del evento en minutos. Puede ser 0 (cero) a 60. se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".

**bHours**

La hora del evento en horas. Puede ser 0 (cero) a 24. se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".

**bDay**

Día del mes del evento. Puede ser 0 (cero) a 31. se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".

**bMonth**

Mes del año del evento. Puede ser 0 (cero) a 12. se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".

**bYear**

Año (desplazamiento por 1900) del evento. Para lograr el año real, agregue 1900 a este valor. se usa 0 (cero) cuando la estructura **JET_BKLOGTIME** es "null".

**bFiller1**

Este campo debe omitirse.

**fTimeIsUTC**

La hora está en formato UTC.

**fUnused**

Este campo debe omitirse.

**bFiller2**

Este campo debe omitirse.

**fOSSnapshot**

Si este evento es una copia de seguridad, esta marca contiene uno de los siguientes valores posibles:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Value</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>copia de seguridad de streaming</p></td>
<td><p>0 (cero)</p></td>
</tr>
<tr class="even">
<td><p>copia de seguridad de instantánea</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**fReserved**

Este campo debe omitirse.

### <a name="remarks"></a>Observaciones

Esta estructura se utiliza al depurar.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
