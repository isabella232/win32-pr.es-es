---
description: La estructura PERFINFO DSHOW STREAMTRACE contiene datos para \_ un DirectShow de seguimiento de tipo GUID \_ \_ STREAMTRACE.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: PERFINFO_DSHOW_STREAMTRACE estructura (Perfstruct.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_STREAMTRACE
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: e17d013d90b133f9c6819b8d9ddf4b5970582cae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063189"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>PERFINFO \_ DSHOW \_ STREAMTRACE (estructura)

La `PERFINFO_DSHOW_STREAMTRACE` estructura contiene datos para un evento DirectShow de seguimiento de tipo GUID \_ STREAMTRACE.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>Members

<dl> <dt>

**id**
</dt> <dd>

Identificador de evento. Vea la sección Comentarios.

</dd> <dt>

**reserved**
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

**dshowClock**
</dt> <dd>

Tiempo de transmisión para este evento, en unidades de 100 nanosegundos. Este valor es opcional y puede ser cero.

</dd> <dt>

**data**
</dt> <dd>

Datos de eventos opcionales que constan de cuatro **valores ULONGLONG.** El significado de estos datos depende del identificador de evento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se definen los siguientes identificadores de evento.




| Identificador de evento | Descripción | 
|------------------|-------------|
| PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION | Se registra cuando <a href="mpeg-2-demultiplexer.md">el filtro Demultiplexer MPEG-2</a> convierte una marca de tiempo de presentación (PTS) en tiempo de transmisión.<ul><li><strong>datos</strong>[0]: hora de inicio convertida.</li><li><strong>datos</strong>[1]: tiempo de detenerse convertido.</li><li><strong>datos</strong>[2]. Identificador de flujo para el pin de entrada.</li><li><strong>datos</strong>[3]: PTS que se ha convertido.</li></ul> | 
| PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE | Se registra cuando Demultiplexer MPEG-2 recibe un ejemplo.<ul><li><strong>data</strong>[0]: hora actual devuelta por <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE | Se registra cuando vmr programa un ejemplo para su representación, inmediatamente antes de que el VMR llame a <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.<ul><li><strong>data</strong>[0]: hora de referencia cuando se inició el streaming, que corresponde al tiempo de flujo cero.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE | Se registra cuando vmr comienza una operación de descodificación, es decir, cuando el descodificador llama a <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>. Sin datos del evento. | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE | Se registra cuando vmr comienza una operación de desenlazado o composición de vídeo. Sin datos del evento. | 
| PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME | Se registra cuando vmr quita un fotograma; por ejemplo, si una muestra se ha retrasado.<ul><li><strong>datos</strong>[0]: hora de inicio de ejemplo.</li><li><strong>datos</strong>[1]: hora de finalización del ejemplo.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_END_ADVISE | Se registra cuando el VMR recibe una notificación de aviso del reloj de referencia. Sin datos del evento. | 
| PERFINFO_STREAMTRACE_VMR_END_DECODE | Se registra cuando vmr finaliza una operación de descodificación, es decir, cuando el descodificador llama a <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>. Sin datos del evento. | 
| PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE | Se registra cuando VMR completa una operación de desenlazado o composición de vídeo. Sin datos del evento. | 
| PERFINFO_STREAMTRACE_VMR_RECEIVE | Se registra cuando vmr recibe un nuevo ejemplo. Sin datos del evento. | 
| PERFINFO_STREAMTRACE_VMR_RENDER_TIME | Se registra cuando vmr termina de representar un fotograma.<ul><li><strong>data</strong>[0]: tiempo que se tardó en representar este marco.</li><li><strong>datos</strong>[1]: promedio de ejecución de los tiempos de representación de fotogramas.</li></ul> | 




 

Para registrar este evento desde un filtro DirectShow, use la función **\_ PERFLOG STREAMTRACE,** que se define en el archivo de encabezado Dxmperf.h. Este encabezado se incluye en las clases DirectShow base.

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

 

 
