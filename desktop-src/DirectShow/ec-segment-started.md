---
description: Se ha iniciado un nuevo segmento.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653375"
---
# <a name="ec_segment_started"></a><span data-ttu-id="04617-103">segmento de EC \_ \_ iniciado</span><span class="sxs-lookup"><span data-stu-id="04617-103">EC\_SEGMENT\_STARTED</span></span>

<span data-ttu-id="04617-104">Se ha iniciado un nuevo segmento.</span><span class="sxs-lookup"><span data-stu-id="04617-104">A new segment has started.</span></span>

## <a name="parameters"></a><span data-ttu-id="04617-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04617-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04617-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="04617-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="04617-107">(**const** **Reference \_ Time** \* ) puntero en un valor de **\_ tiempo de referencia** que especifica el tiempo de flujo acumulado desde el inicio del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="04617-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="04617-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="04617-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="04617-109">(**DWORD**) Número de segmento (basado en cero).</span><span class="sxs-lookup"><span data-stu-id="04617-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="04617-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="04617-110">Default Action</span></span>

<span data-ttu-id="04617-111">Este evento no se envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04617-111">This event is not sent to the application.</span></span> <span data-ttu-id="04617-112">Las aplicaciones no pueden invalidar la acción predeterminada para este evento.</span><span class="sxs-lookup"><span data-stu-id="04617-112">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="04617-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04617-113">Remarks</span></span>

<span data-ttu-id="04617-114">Si un filtro va a enviar [**un \_ final \_ de \_ segmento de EC**](ec-end-of-segment.md) al final de un segmento, envía este evento al principio del segmento.</span><span class="sxs-lookup"><span data-stu-id="04617-114">If a filter will send an [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) at the end of a segment, it sends this event at the start of the segment.</span></span> <span data-ttu-id="04617-115">Filter Graph Manager usa esta notificación de eventos para calcular el número \_ \_ de notificaciones de fin de segmento de EC \_ que debería esperar al final del segmento.</span><span class="sxs-lookup"><span data-stu-id="04617-115">The filter graph manager uses this event notification to compute how many EC\_END\_OF\_SEGMENT notifications it should expect at the end of the segment.</span></span>

<span data-ttu-id="04617-116">De forma predeterminada, los filtros no envían eventos [**\_ \_ de fin de \_ segmento de EC**](ec-end-of-segment.md) al final de los segmentos y, por tanto, no deben enviar este evento.</span><span class="sxs-lookup"><span data-stu-id="04617-116">By default, filters do not send [**EC\_END\_OF\_SEGMENT**](ec-end-of-segment.md) events at the end of segments, and therefore should not send this event.</span></span> <span data-ttu-id="04617-117">Para obtener más información, vea [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span><span class="sxs-lookup"><span data-stu-id="04617-117">For more information, see [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).</span></span>

## <a name="requirements"></a><span data-ttu-id="04617-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04617-118">Requirements</span></span>



| <span data-ttu-id="04617-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04617-119">Requirement</span></span> | <span data-ttu-id="04617-120">Value</span><span class="sxs-lookup"><span data-stu-id="04617-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04617-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04617-121">Header</span></span><br/> | <dl> <span data-ttu-id="04617-122"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="04617-122"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04617-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="04617-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04617-124">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="04617-124">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="04617-125">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="04617-125">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




