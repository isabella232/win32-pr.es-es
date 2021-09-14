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
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886625"
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



## <a name="members"></a>Members

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

## <a name="remarks"></a>Observaciones

Para habilitar este evento, debe establecer la marca DXMPERF VIDEOREND en el parámetro \_ *EnableFlag* al llamar a **EnableTrace**. Esta marca se define en el archivo de encabezado Dxmperf.h, que se incluye en las DirectShow base.

Para registrar este evento desde un filtro DirectShow, use la macro **PERFLOG \_ VIDEOREND,** que se define en Dxmperf.h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Perfstruct.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[Seguimiento de eventos en DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID de eventos de seguimiento](trace-guids.md)
</dt> </dl>

 

 




