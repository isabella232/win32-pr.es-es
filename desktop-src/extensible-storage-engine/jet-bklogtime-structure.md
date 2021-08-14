---
description: 'Más información sobre: JET_BKLOGTIME estructura'
title: JET_BKLOGTIME estructura
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
ms.openlocfilehash: b34740d582e341cce3b2fd0b28203b7346a4de1d94a8586289be8ab252247943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118487727"
---
# <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_bklogtime-structure"></a>JET_BKLOGTIME estructura

La **JET_BKLOGTIME** contiene los elementos de fecha y hora de un evento. Es una extensión de [JET_LOGTIME](./jet-logtime-structure.md).

**Windows Vista: JET_BKLOGTIME** se presenta en Windows Vista.

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

Hora del evento en segundos. Puede ser de 0 (cero) a 60. Se usa 0 (cero) cuando la **JET_BKLOGTIME** es "null".

**bMinutes**

Hora del evento en minutos. Puede ser de 0 (cero) a 60. Se usa 0 (cero) cuando la **JET_BKLOGTIME** es "null".

**bHours**

Hora del evento en horas. Puede ser de 0 (cero) a 24. Se usa 0 (cero) cuando la **JET_BKLOGTIME** es "null".

**Cumpleaños**

Día del mes del evento. Puede ser de 0 (cero) a 31. Se usa 0 (cero) cuando la **JET_BKLOGTIME** es "null".

**bMonth**

Mes del año del evento. Puede ser de 0 (cero) a 12. Se usa 0 (cero) cuando la **JET_BKLOGTIME** es "null".

**bYear**

Año (desplazamiento por 1900) del evento. Para lograr el año real, agregue 1900 a este valor. Se usa 0 (cero) cuando la **JET_BKLOGTIME** es "null".

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
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>copia de seguridad de streaming</p></td>
<td><p>0 (cero)</p></td>
</tr>
<tr class="even">
<td><p>copia de seguridad de instantáneas</p></td>
<td><p>1</p></td>
</tr>
</tbody>
</table>


**fReserved**

Este campo debe omitirse.

### <a name="remarks"></a>Comentarios

Esta estructura se usa al depurar.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
