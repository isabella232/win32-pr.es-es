---
description: Desusado. Representa un instante en el tiempo, normalmente expresado como una fecha y hora del día y un calendario correspondiente.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: CALDATETIME (estructura)
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
ms.openlocfilehash: 700e11f27b673d9ff706483cc4abcf2f06cd7d8bb779ef8eaf9b51a6d81b4068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822835"
---
# <a name="caldatetime-structure"></a>CALDATETIME (estructura)

En desuso. Representa un instante en el tiempo, normalmente expresado como una fecha y hora del día y un calendario correspondiente.

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

Identificador [del calendario](calendar-identifiers.md) para el instante en el tiempo.

</dd> <dt>

**Era**
</dt> <dd>

Información de era del instante en el tiempo.

</dd> <dt>

**año**
</dt> <dd>

Año del instante en el tiempo.

</dd> <dt>

**Month (Mes)**
</dt> <dd>

Mes del instante en el tiempo.

</dd> <dt>

**Day**
</dt> <dd>

Día del instante en el tiempo.

</dd> <dt>

**DayOfWeek**
</dt> <dd>

Día de la semana del instante en el tiempo.

</dd> <dt>

**Hora**
</dt> <dd>

Hora del instante en el tiempo.

</dd> <dt>

**Minuto**
</dt> <dd>

Minuto del instante en el tiempo.

</dd> <dt>

**Segundo**
</dt> <dd>

Segundo para el instante en el tiempo.

</dd> <dt>

**Garrapata**
</dt> <dd>

Tic para el instante en el tiempo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de compatibilidad con idiomas nacionales](national-language-support-structures.md)
</dt> </dl>

 

 




