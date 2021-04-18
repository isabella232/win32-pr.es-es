---
description: La \_ estructura PERFINFO \_ de DSHOW STREAMTRACE contiene datos para un evento de seguimiento de DirectShow de tipo GUID \_ STREAMTRACE.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: PERFINFO_DSHOW_STREAMTRACE estructura (Perfstruct. h)
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
ms.openlocfilehash: 2bee4f3c11cf8462c8292cc412a6da5d9f9bfa78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690143"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>PERFINFO \_ STREAMTRACE, estructura de DSHOW \_

La `PERFINFO_DSHOW_STREAMTRACE` estructura contiene datos para un evento de seguimiento de DirectShow de tipo GUID \_ STREAMTRACE.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**id**
</dt> <dd>

Identificador del evento. Vea la sección Comentarios.

</dd> <dt>

**sector**
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

**dshowClock**
</dt> <dd>

Tiempo de secuencia para este evento, en unidades de 100-nanosegundos. Este valor es opcional y puede ser cero.

</dd> <dt>

**data**
</dt> <dd>

Datos de evento opcionales que se componen de cuatro valores de **ULONGLONG** . El significado de estos datos depende del identificador de evento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se definen los siguientes identificadores de eventos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificador de evento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</td>
<td>Se registra cuando el filtro <a href="mpeg-2-demultiplexer.md">de demultiplexador MPEG-2</a> convierte una marca de tiempo de presentación (PTS) en una hora de flujo.
<ul>
<li><strong>data</strong>[0]: Converted start time.</li>
<li><strong>data</strong>[1]: Converted stop time.</li>
<li><strong>datos</strong>[2]. Identificador de flujo para el PIN de entrada.</li>
<li><strong>data</strong>[3]: PTS that was converted.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</td>
<td>Se registra cuando el demultiplexador MPEG-2 recibe un ejemplo.
<ul>
<li><strong>datos</strong> [0]: Current time returned by  de <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</td>
<td>Se registra cuando VMR programa un ejemplo para la representación, inmediatamente antes de que la VMR llame a <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: AdviseTime</strong></a>.
<ul>
<li><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</td>
<td>Se registra cuando VMR inicia una operación de descodificación, es decir, cuando el descodificador llama a <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator:: BeginFrame</strong></a>. Sin datos del evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</td>
<td>Se registra cuando VMR comienza una operación de desentrelazado o de composición de vídeo. Sin datos del evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</td>
<td>Se registra cuando VMR quita un fotograma; por ejemplo, si una muestra estaba atrasada.
<ul>
<li><strong>data</strong>[0]: Sample start time.</li>
<li><strong>data</strong>[1]: Sample end time.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_ADVISE</td>
<td>Se registra cuando VMR recibe una notificación de aviso del reloj de referencia. Sin datos del evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_END_DECODE</td>
<td>Se registra cuando VMR finaliza una operación de descodificación, es decir, cuando el descodificador llama a <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator:: EndFrame</strong></a>. Sin datos del evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</td>
<td>Se registra cuando VMR completa una operación de desentrelazado o de composición de vídeo. Sin datos del evento.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_RECEIVE</td>
<td>Se registra cuando VMR recibe un nuevo ejemplo. Sin datos del evento.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_RENDER_TIME</td>
<td>Se registra cuando VMR finaliza la representación de un fotograma.
<ul>
<li><strong>data</strong>[0]: Time that it took to render this frame.</li>
<li><strong>data</strong>[1]: Running average of frame rendering times.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Para registrar este evento desde un filtro de DirectShow, use la función **\_ STREAMTRACE** , que se define en el archivo de encabezado Dxmperf. h. Este encabezado se incluye en las clases base de DirectShow.

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

 

 
