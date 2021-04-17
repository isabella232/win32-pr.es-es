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
# <a name="perfinfo_dshow_audiobreak-structure"></a><span data-ttu-id="c5f78-103">PERFINFO \_ AUDIOBREAK, estructura de DSHOW \_</span><span class="sxs-lookup"><span data-stu-id="c5f78-103">PERFINFO\_DSHOW\_AUDIOBREAK structure</span></span>

<span data-ttu-id="c5f78-104">La `PERFINFO_DSHOW_AUDIOBREAK` estructura contiene datos para un evento de seguimiento de tipo GUID \_ AUDIOBREAK.</span><span class="sxs-lookup"><span data-stu-id="c5f78-104">The `PERFINFO_DSHOW_AUDIOBREAK` structure contains data for a trace event of type GUID\_AUDIOBREAK.</span></span>

<span data-ttu-id="c5f78-105">El filtro de [representador de DirectSound](directsound-renderer-filter.md) registra este evento cuando se produce una interrupción en la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="c5f78-105">The [DirectSound Renderer](directsound-renderer-filter.md) filter logs this event when there is a break in the audio stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f78-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5f78-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a><span data-ttu-id="c5f78-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5f78-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5f78-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="c5f78-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="c5f78-109">Recuento de ciclos de reloj más recientes (instrucción RDTSC).</span><span class="sxs-lookup"><span data-stu-id="c5f78-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="c5f78-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="c5f78-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="c5f78-111">Posición de escritura actual en el búfer de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="c5f78-111">Current write position in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c5f78-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="c5f78-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="c5f78-113">Inicio de la interrupción de audio en el búfer de DirectSound.</span><span class="sxs-lookup"><span data-stu-id="c5f78-113">Start of the audio break in the DirectSound buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c5f78-114">**sampleDuration**</span><span class="sxs-lookup"><span data-stu-id="c5f78-114">**sampleDuration**</span></span>
</dt> <dd>

<span data-ttu-id="c5f78-115">Duración de la interrupción, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="c5f78-115">Duration of the break, in milliseconds.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5f78-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5f78-116">Remarks</span></span>

<span data-ttu-id="c5f78-117">Para habilitar este evento, debe establecer la \_ marca de bits AUDIOBREAK en el parámetro *EnableFlag* cuando llame a **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="c5f78-117">To enable this event, you must set the AUDIOBREAK\_BIT flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="c5f78-118">Esta marca se define en el archivo de encabezado Dxmperf. h, que se incluye en las clases base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c5f78-118">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="c5f78-119">Para registrar este evento desde un filtro de DirectShow, use la macro **\_ AUDIOBREAK** , que se define en Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="c5f78-119">To log this event from a DirectShow filter, use the **PERFLOG\_AUDIOBREAK** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f78-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5f78-120">Requirements</span></span>



| <span data-ttu-id="c5f78-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f78-121">Requirement</span></span> | <span data-ttu-id="c5f78-122">Value</span><span class="sxs-lookup"><span data-stu-id="c5f78-122">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f78-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5f78-123">Header</span></span><br/> | <dl> <span data-ttu-id="c5f78-124"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f78-124"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5f78-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5f78-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f78-126">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c5f78-126">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="c5f78-127">Seguimiento de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="c5f78-127">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="c5f78-128">GUID de eventos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="c5f78-128">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




