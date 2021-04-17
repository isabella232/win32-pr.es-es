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
# <a name="perfinfo_dshow_avrend-structure"></a><span data-ttu-id="955dd-103">PERFINFO \_ AVREND, estructura de DSHOW \_</span><span class="sxs-lookup"><span data-stu-id="955dd-103">PERFINFO\_DSHOW\_AVREND structure</span></span>

<span data-ttu-id="955dd-104">La `PERFINFO_DSHOW_AVREND` estructura contiene datos para un evento de seguimiento de tipo GUID \_ VIDEOREND.</span><span class="sxs-lookup"><span data-stu-id="955dd-104">The `PERFINFO_DSHOW_AVREND` structure contains data for a trace event of type GUID\_VIDEOREND.</span></span>

<span data-ttu-id="955dd-105">VMR registra este evento inmediatamente antes de representar un fotograma.</span><span class="sxs-lookup"><span data-stu-id="955dd-105">The VMR logs this event immediately before rendering a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="955dd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="955dd-106">Syntax</span></span>


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a><span data-ttu-id="955dd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="955dd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="955dd-108">**cycleCounter**</span><span class="sxs-lookup"><span data-stu-id="955dd-108">**cycleCounter**</span></span>
</dt> <dd>

<span data-ttu-id="955dd-109">Recuento de ciclos de reloj más recientes (instrucción RDTSC).</span><span class="sxs-lookup"><span data-stu-id="955dd-109">Latest clock cycle count (RDTSC instruction).</span></span>

</dd> <dt>

<span data-ttu-id="955dd-110">**dshowClock**</span><span class="sxs-lookup"><span data-stu-id="955dd-110">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="955dd-111">Tiempo de referencia actual, tal y como lo devuelve el método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .</span><span class="sxs-lookup"><span data-stu-id="955dd-111">Current reference time, as returned by the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

</dd> <dt>

<span data-ttu-id="955dd-112">**sampleTime**</span><span class="sxs-lookup"><span data-stu-id="955dd-112">**sampleTime**</span></span>
</dt> <dd>

<span data-ttu-id="955dd-113">Hora de inicio del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="955dd-113">Start time of the sample.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="955dd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="955dd-114">Remarks</span></span>

<span data-ttu-id="955dd-115">Para habilitar este evento, debe establecer la marca DXMPERF \_ VIDEOREND en el parámetro *EnableFlag* cuando llame a **EnableTrace**.</span><span class="sxs-lookup"><span data-stu-id="955dd-115">To enable this event, you must set the DXMPERF\_VIDEOREND flag in the *EnableFlag* parameter when you call **EnableTrace**.</span></span> <span data-ttu-id="955dd-116">Esta marca se define en el archivo de encabezado Dxmperf. h, que se incluye en las clases base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="955dd-116">This flag is defined in the header file Dxmperf.h, which is included in the DirectShow base classes.</span></span>

<span data-ttu-id="955dd-117">Para registrar este evento desde un filtro de DirectShow, use la macro **\_ VIDEOREND** , que se define en Dxmperf. h.</span><span class="sxs-lookup"><span data-stu-id="955dd-117">To log this event from a DirectShow filter, use the **PERFLOG\_VIDEOREND** macro, which is defined in Dxmperf.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="955dd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="955dd-118">Requirements</span></span>



| <span data-ttu-id="955dd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="955dd-119">Requirement</span></span> | <span data-ttu-id="955dd-120">Value</span><span class="sxs-lookup"><span data-stu-id="955dd-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="955dd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="955dd-121">Header</span></span><br/> | <dl> <span data-ttu-id="955dd-122"><dt>Perfstruct. h</dt></span><span class="sxs-lookup"><span data-stu-id="955dd-122"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="955dd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="955dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955dd-124">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="955dd-124">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="955dd-125">Seguimiento de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="955dd-125">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="955dd-126">GUID de eventos de seguimiento</span><span class="sxs-lookup"><span data-stu-id="955dd-126">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 




