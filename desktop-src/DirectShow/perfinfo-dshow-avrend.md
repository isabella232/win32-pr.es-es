---
description: La estructura PERFINFO DSHOW AVREND contiene datos para un evento \_ de seguimiento de tipo GUID \_ \_ VIDEOREND. VmR registra este evento inmediatamente antes de representar un fotograma.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: PERFINFO_DSHOW_AVREND estructura (Perfstruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 49cc76f4db1a5fae76678ee2d81f3e2fff0a6c5ca3d5c5532adebaec23f48215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050715"
---
# <a name="perfinfo_dshow_avrend-structure"></a>PERFINFO \_ DSHOW \_ (estructura AVREND)

La `PERFINFO_DSHOW_AVREND` estructura contiene datos para un evento de seguimiento de tipo GUID \_ VIDEOREND.

VmR registra este evento inmediatamente antes de representar un fotograma.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cycleCounter**
</dt> <dd>

Recuento del ciclo de reloj más reciente (instrucción RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Hora de referencia actual, tal como la devuelve [**el método IReferenceClock::GetTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime)

</dd> <dt>

**sampleTime**
</dt> <dd>

Hora de inicio del ejemplo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para habilitar este evento, debe establecer la marca DXMPERF VIDEOREND en el parámetro \_ *EnableFlag* al llamar a **EnableTrace**. Esta marca se define en el archivo de encabezado Dxmperf.h, que se incluye en las DirectShow base.

Para registrar este evento desde un filtro DirectShow, use la macro **PERFLOG \_ VIDEOREND,** que se define en Dxmperf.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Perfstruct.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[Seguimiento de eventos en DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID de eventos de seguimiento](trace-guids.md)
</dt> </dl>

 

 




