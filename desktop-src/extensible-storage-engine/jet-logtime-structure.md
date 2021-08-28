---
description: 'Más información sobre: JET_LOGTIME estructura'
title: JET_LOGTIME estructura
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
ms.openlocfilehash: 4cb99f2a64877ec76afda993a76be4aeaa14c895
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987047"
---
# <a name="jet_logtime-structure"></a>JET_LOGTIME estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_logtime-structure"></a>JET_LOGTIME estructura

La **JET_LOGTIME** contiene elementos de la fecha y hora de un evento.

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

Hora del evento en segundos. Este valor puede ser de 0 a 59. Se usa 0 cuando la estructura es null.

**bMinutes**

Hora del evento en minutos. Este valor puede ser de 0 a 59. Se usa 0 cuando la estructura es null.

**bHours**

Hora del evento en horas. Este valor puede ser de 0 a 23. Se usa 0 cuando la estructura es null.

**Cumpleaños**

Día del mes del evento. Este valor puede ser de 0 a 31. Se usa 0 cuando la estructura es null.

**bMonth**

Mes del año del evento. Este valor puede ser de 0 a 12. Se usa 0 cuando la estructura es null.

**bYear**

Año del evento (desplazamiento por 1900). Para lograr el año real, agregue 1900 a este valor. Se usa 0 cuando la estructura es null.

**bFiller1**

Este campo debe omitirse.

**fTimeIsUTC**

La hora está en formato UTC.

**fUnused**

Este campo debe omitirse.

**bFiller2**

Este campo debe omitirse.

### <a name="remarks"></a>Observaciones

Esta estructura está pensada principalmente para su uso en la depuración.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
