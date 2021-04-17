---
description: La \_ estructura PERFINFO \_ de DSHOW AUDIOBREAK contiene datos para un evento de seguimiento de tipo GUID \_ AUDIOBREAK. El filtro de representador de DirectSound registra este evento cuando se produce una interrupción en la secuencia de audio.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: PERFINFO_DSHOW_AUDIOBREAK estructura (Perfstruct. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690863"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>PERFINFO \_ AUDIOBREAK, estructura de DSHOW \_

La `PERFINFO_DSHOW_AUDIOBREAK` estructura contiene datos para un evento de seguimiento de tipo GUID \_ AUDIOBREAK.

El filtro de [representador de DirectSound](directsound-renderer-filter.md) registra este evento cuando se produce una interrupción en la secuencia de audio.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cycleCounter**
</dt> <dd>

Recuento de ciclos de reloj más recientes (instrucción RDTSC).

</dd> <dt>

**dshowClock**
</dt> <dd>

Posición de escritura actual en el búfer de DirectSound.

</dd> <dt>

**sampleTime**
</dt> <dd>

Inicio de la interrupción de audio en el búfer de DirectSound.

</dd> <dt>

**sampleDuration**
</dt> <dd>

Duración de la interrupción, en milisegundos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para habilitar este evento, debe establecer la \_ marca de bits AUDIOBREAK en el parámetro *EnableFlag* cuando llame a **EnableTrace**. Esta marca se define en el archivo de encabezado Dxmperf. h, que se incluye en las clases base de DirectShow.

Para registrar este evento desde un filtro de DirectShow, use la macro **\_ AUDIOBREAK** , que se define en Dxmperf. h.

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

 

 




