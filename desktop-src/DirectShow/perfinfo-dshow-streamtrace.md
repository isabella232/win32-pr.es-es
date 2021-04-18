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
# <a name="perfinfo_dshow_streamtrace-structure"></a><span data-ttu-id="d541e-103">PERFINFO \_ STREAMTRACE, estructura de DSHOW \_</span><span class="sxs-lookup"><span data-stu-id="d541e-103">PERFINFO\_DSHOW\_STREAMTRACE structure</span></span>

<span data-ttu-id="d541e-104">La `PERFINFO_DSHOW_STREAMTRACE` estructura contiene datos para un evento de seguimiento de DirectShow de tipo GUID \_ STREAMTRACE.</span><span class="sxs-lookup"><span data-stu-id="d541e-104">The `PERFINFO_DSHOW_STREAMTRACE` structure contains data for a DirectShow trace event of type GUID\_STREAMTRACE.</span></span>

## <a name="syntax"></a><span data-ttu-id="d541e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d541e-105">Syntax</span></span>


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a><span data-ttu-id="d541e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d541e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d541e-107">**id**</span><span class="sxs-lookup"><span data-stu-id="d541e-107">**id**</span></span>
</dt> <dd>

<span data-ttu-id="d541e-108">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-108">Event identifier.</span></span> <span data-ttu-id="d541e-109">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d541e-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d541e-110">**sector**</span><span class="sxs-lookup"><span data-stu-id="d541e-110">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d541e-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d541e-111">Reserved.</span></span> <span data-ttu-id="d541e-112">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="d541e-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="d541e-113">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="d541e-113">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="d541e-114">Tiempo de secuencia para este evento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="d541e-114">Stream time for this event, in 100-nanosecond units.</span></span> <span data-ttu-id="d541e-115">Este valor es opcional y puede ser cero.</span><span class="sxs-lookup"><span data-stu-id="d541e-115">This value is optional and can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d541e-116">**data**</span><span class="sxs-lookup"><span data-stu-id="d541e-116">**data**</span></span>
</dt> <dd>

<span data-ttu-id="d541e-117">Datos de evento opcionales que se componen de cuatro valores de **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="d541e-117">Optional event data consisting of four **ULONGLONG** values.</span></span> <span data-ttu-id="d541e-118">El significado de estos datos depende del identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-118">The meaning of this data depends on the event identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d541e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d541e-119">Remarks</span></span>

<span data-ttu-id="d541e-120">Se definen los siguientes identificadores de eventos.</span><span class="sxs-lookup"><span data-stu-id="d541e-120">The following event identifiers are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d541e-121">Identificador de evento</span><span class="sxs-lookup"><span data-stu-id="d541e-121">Event identifier</span></span></th>
<th><span data-ttu-id="d541e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d541e-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d541e-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span><span class="sxs-lookup"><span data-stu-id="d541e-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span></span></td>
<td><span data-ttu-id="d541e-124">Se registra cuando el filtro <a href="mpeg-2-demultiplexer.md">de demultiplexador MPEG-2</a> convierte una marca de tiempo de presentación (PTS) en una hora de flujo.</span><span class="sxs-lookup"><span data-stu-id="d541e-124">Logged when the <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer</a> filter converts a presentation time stamp (PTS) to stream time.</span></span>
<ul>
<li><span data-ttu-id="d541e-125"><strong>data</strong>[0]: Converted start time.</span><span class="sxs-lookup"><span data-stu-id="d541e-125"><strong>data</strong>[0]: Converted start time.</span></span></li>
<li><span data-ttu-id="d541e-126"><strong>data</strong>[1]: Converted stop time.</span><span class="sxs-lookup"><span data-stu-id="d541e-126"><strong>data</strong>[1]: Converted stop time.</span></span></li>
<li><span data-ttu-id="d541e-127"><strong>datos</strong>[2].</span><span class="sxs-lookup"><span data-stu-id="d541e-127"><strong>data</strong>[2].</span></span> <span data-ttu-id="d541e-128">Identificador de flujo para el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d541e-128">Stream identifier for the input pin.</span></span></li>
<li><span data-ttu-id="d541e-129"><strong>data</strong>[3]: PTS that was converted.</span><span class="sxs-lookup"><span data-stu-id="d541e-129"><strong>data</strong>[3]: PTS that was converted.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d541e-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="d541e-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span></span></td>
<td><span data-ttu-id="d541e-131">Se registra cuando el demultiplexador MPEG-2 recibe un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d541e-131">Logged when MPEG-2 Demultiplexer receives a sample.</span></span>
<ul>
<li><span data-ttu-id="d541e-132"><strong>datos</strong> [0]: Current time returned by  de <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d541e-132"><strong>data</strong>[0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d541e-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span><span class="sxs-lookup"><span data-stu-id="d541e-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span></span></td>
<td><span data-ttu-id="d541e-134">Se registra cuando VMR programa un ejemplo para la representación, inmediatamente antes de que la VMR llame a <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock:: AdviseTime</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d541e-134">Logged when the VMR schedules a sample for rendering, immediately before the VMR calls <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.</span></span>
<ul>
<li><span data-ttu-id="d541e-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span><span class="sxs-lookup"><span data-stu-id="d541e-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d541e-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span><span class="sxs-lookup"><span data-stu-id="d541e-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span></span></td>
<td><span data-ttu-id="d541e-137">Se registra cuando VMR inicia una operación de descodificación, es decir, cuando el descodificador llama a <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator:: BeginFrame</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d541e-137">Logged when the VMR begins a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>.</span></span> <span data-ttu-id="d541e-138">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-138">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d541e-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="d541e-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span></span></td>
<td><span data-ttu-id="d541e-140">Se registra cuando VMR comienza una operación de desentrelazado o de composición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d541e-140">Logged when the VMR begins a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="d541e-141">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-141">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d541e-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span><span class="sxs-lookup"><span data-stu-id="d541e-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span></span></td>
<td><span data-ttu-id="d541e-143">Se registra cuando VMR quita un fotograma; por ejemplo, si una muestra estaba atrasada.</span><span class="sxs-lookup"><span data-stu-id="d541e-143">Logged when the VMR drops a frame; for example, if a sample was late.</span></span>
<ul>
<li><span data-ttu-id="d541e-144"><strong>data</strong>[0]: Sample start time.</span><span class="sxs-lookup"><span data-stu-id="d541e-144"><strong>data</strong>[0]: Sample start time.</span></span></li>
<li><span data-ttu-id="d541e-145"><strong>data</strong>[1]: Sample end time.</span><span class="sxs-lookup"><span data-stu-id="d541e-145"><strong>data</strong>[1]: Sample end time.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d541e-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span><span class="sxs-lookup"><span data-stu-id="d541e-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span></span></td>
<td><span data-ttu-id="d541e-147">Se registra cuando VMR recibe una notificación de aviso del reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="d541e-147">Logged when the VMR receives an advise notification from the reference clock.</span></span> <span data-ttu-id="d541e-148">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-148">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d541e-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span><span class="sxs-lookup"><span data-stu-id="d541e-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span></span></td>
<td><span data-ttu-id="d541e-150">Se registra cuando VMR finaliza una operación de descodificación, es decir, cuando el descodificador llama a <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator:: EndFrame</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d541e-150">Logged when the VMR ends a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>.</span></span> <span data-ttu-id="d541e-151">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-151">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d541e-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="d541e-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span></span></td>
<td><span data-ttu-id="d541e-153">Se registra cuando VMR completa una operación de desentrelazado o de composición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d541e-153">Logged when the VMR completes a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="d541e-154">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-154">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d541e-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="d541e-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span></span></td>
<td><span data-ttu-id="d541e-156">Se registra cuando VMR recibe un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d541e-156">Logged when the VMR receives a new sample.</span></span> <span data-ttu-id="d541e-157">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d541e-157">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d541e-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span><span class="sxs-lookup"><span data-stu-id="d541e-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span></span></td>
<td><span data-ttu-id="d541e-159">Se registra cuando VMR finaliza la representación de un fotograma.</span><span class="sxs-lookup"><span data-stu-id="d541e-159">Logged when the VMR finishes rendering a frame.</span></span>
<ul>
<li><span data-ttu-id="d541e-160"><strong>data</strong>[0]: Time that it took to render this frame.</span><span class="sxs-lookup"><span data-stu-id="d541e-160"><strong>data</strong>[0]: Time that it took to render this frame.</span></span></li>
<li><span data-ttu-id="d541e-161"><strong>data</strong>[1]: Running average of frame rendering times.</span><span class="sxs-lookup"><span data-stu-id="d541e-161"><strong>data</strong>[1]: Running average of frame rendering times.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d541e-162">Para registrar este evento desde un filtro de DirectShow, use la función **\_ STREAMTRACE** , que se define en el archivo de encabezado Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="d541e-162">To log this event from a DirectShow filter, use the **PERFLOG\_STREAMTRACE** function, which is defined in the header file Dxmperf.h.</span></span> <span data-ttu-id="d541e-163">Este encabezado se incluye en las clases base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d541e-163">This header is included in the DirectShow base classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="d541e-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d541e-164">Requirements</span></span>



| <span data-ttu-id="d541e-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d541e-165">Requirement</span></span> | <span data-ttu-id="d541e-166">Value</span><span class="sxs-lookup"><span data-stu-id="d541e-166">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d541e-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d541e-167">Header</span></span><br/> | <dl> <span data-ttu-id="d541e-168"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="d541e-168"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d541e-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="d541e-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d541e-170">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d541e-170">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="d541e-171">Seguimiento de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d541e-171">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d541e-172">GUID de eventos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="d541e-172">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 
