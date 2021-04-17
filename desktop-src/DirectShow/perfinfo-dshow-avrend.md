---
description: La \_ estructura PERFINFO \_ de DSHOW AVREND contiene datos para un evento de seguimiento de tipo GUID \_ VIDEOREND. VMR registra este evento inmediatamente antes de representar un fotograma.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: PERFINFO_DSHOW_AVREND estructura (Perfstruct. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690861"
---
# <a name="perfinfo_dshow_avrend-structure"></a>PERFINFO \_ AVREND, estructura de DSHOW \_

La `PERFINFO_DSHOW_AVREND` estructura contiene datos para un evento de seguimiento de tipo GUID \_ VIDEOREND.

VMR registra este evento inmediatamente antes de representar un fotograma.

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

Recuento de ciclos de reloj más recientes (instrucción RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Tiempo de referencia actual, tal y como lo devuelve el método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

</dd> <dt>

**sampleTime**
</dt> <dd>

Hora de inicio del ejemplo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para habilitar este evento, debe establecer la marca DXMPERF \_ VIDEOREND en el parámetro *EnableFlag* cuando llame a **EnableTrace**. Esta marca se define en el archivo de encabezado Dxmperf. h, que se incluye en las clases base de DirectShow.

Para registrar este evento desde un filtro de DirectShow, use la macro **\_ VIDEOREND** , que se define en Dxmperf. h.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Perfstruct. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DirectShow](directshow-structures.md)
</dt> <dt>

[Seguimiento de eventos en DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[GUID de eventos de seguimiento](trace-guids.md)
</dt> </dl>

 

 




