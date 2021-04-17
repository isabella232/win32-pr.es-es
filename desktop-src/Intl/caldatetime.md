---
description: Desusado. Representa un instante de tiempo, normalmente expresado como una fecha y hora del día y un calendario correspondiente.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Estructura CALDATETIME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689565"
---
# <a name="caldatetime-structure"></a>Estructura CALDATETIME

En desuso. Representa un instante de tiempo, normalmente expresado como una fecha y hora del día y un calendario correspondiente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CalId**
</dt> <dd>

[Identificador del calendario](calendar-identifiers.md) para el instante en el tiempo.

</dd> <dt>

**Período**
</dt> <dd>

Información de la era para el instante en el tiempo.

</dd> <dt>

**Anual**
</dt> <dd>

Año para el instante en el tiempo.

</dd> <dt>

**Mensuales**
</dt> <dd>

Mes para el instante en el tiempo.

</dd> <dt>

**Day**
</dt> <dd>

Día del instante en el tiempo.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

El día de la semana para el instante en el tiempo.

</dd> <dt>

**Hora**
</dt> <dd>

Hora del instante en el tiempo.

</dd> <dt>

**Minute**
</dt> <dd>

Minuto para el instante en el tiempo.

</dd> <dt>

**Segundo**
</dt> <dd>

Segundo para el instante en el tiempo.

</dd> <dt>

**Ticker**
</dt> <dd>

El paso del instante en el tiempo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de soporte de National Language](national-language-support-structures.md)
</dt> </dl>

 

 




