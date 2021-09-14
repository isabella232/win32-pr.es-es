---
description: La estructura PERFINFO \_ DSHOW AUDIOBREAK contiene datos para un evento de seguimiento de tipo GUID \_ \_ AUDIOBREAK. El filtro Representador de Direct Sound registra este evento cuando hay una interrupción en la secuencia de audio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: PERFINFO_DSHOW_AUDIOBREAK estructura (Perfstruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886620"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>ESTRUCTURA PERFINFO \_ DSHOW \_ AUDIOBREAK

La `PERFINFO_DSHOW_AUDIOBREAK` estructura contiene datos para un evento de seguimiento de tipo GUID \_ AUDIOBREAK.

El [filtro Representador de Direct Sound](directsound-renderer-filter.md) registra este evento cuando hay una interrupción en la secuencia de audio.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>Members

<dl> <dt>

**cycleCounter**
</dt> <dd>

Recuento del ciclo de reloj más reciente (instrucción RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Posición de escritura actual en el búfer Direct Sound.

</dd> <dt>

**sampleTime**
</dt> <dd>

Inicio de la interrupción de audio en el búfer Direct Sound.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Duración de la interrupción, en milisegundos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para habilitar este evento, debe establecer la marca AUDIOBREAK BIT en el \_ *parámetro EnableFlag* al llamar a **EnableTrace**. Esta marca se define en el archivo de encabezado Dxmperf.h, que se incluye en las DirectShow base.

Para registrar este evento desde un filtro DirectShow, use la macro **PERFLOG \_ AUDIOBREAK,** que se define en Dxmperf.h.

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

 

 




