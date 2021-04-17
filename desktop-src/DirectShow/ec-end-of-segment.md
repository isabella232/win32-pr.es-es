---
description: Se alcanzó el final de un segmento.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679538"
---
# <a name="ec_end_of_segment"></a><span data-ttu-id="5a0e3-103">\_fin \_ del \_ segmento EC</span><span class="sxs-lookup"><span data-stu-id="5a0e3-103">EC\_END\_OF\_SEGMENT</span></span>

<span data-ttu-id="5a0e3-104">Se alcanzó el final de un segmento.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-104">The end of a segment was reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="5a0e3-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a0e3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a0e3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5a0e3-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5a0e3-107">(**const** **Reference \_ Time** \* ) puntero en un valor de **\_ tiempo de referencia** que especifica el tiempo de flujo acumulado desde el inicio del segmento, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="5a0e3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5a0e3-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5a0e3-109">(**DWORD**) Número de segmento (basado en cero).</span><span class="sxs-lookup"><span data-stu-id="5a0e3-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="5a0e3-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="5a0e3-110">Default Action</span></span>

<span data-ttu-id="5a0e3-111">El administrador de gráficos de filtros comprueba el número de eventos de **\_ fin \_ de \_ segmento de EC** con respecto al número de eventos de [**segmento de EC \_ \_ iniciado**](ec-segment-started.md) .</span><span class="sxs-lookup"><span data-stu-id="5a0e3-111">The filter graph manager checks the number of **EC\_END\_OF\_SEGMENT** events against the number of [**EC\_SEGMENT\_STARTED**](ec-segment-started.md) events.</span></span> <span data-ttu-id="5a0e3-112">Si coinciden, reenvía el **evento \_ \_ de fin de \_ segmento de EC** a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-112">If they match, it forwards the **EC\_END\_OF\_SEGMENT** event to the application.</span></span> <span data-ttu-id="5a0e3-113">Las aplicaciones no pueden invalidar la acción predeterminada para este evento.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a0e3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a0e3-114">Remarks</span></span>

<span data-ttu-id="5a0e3-115">Este código de evento admite el bucle sin problemas.</span><span class="sxs-lookup"><span data-stu-id="5a0e3-115">This event code supports seamless looping.</span></span> <span data-ttu-id="5a0e3-116">Cuando una llamada al método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) incluye la marca de \_ segmento de búsqueda de AM \_ , el filtro de origen envía este código de evento en lugar de llamar a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span><span class="sxs-lookup"><span data-stu-id="5a0e3-116">When a call to the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method includes the AM\_SEEKING\_Segment flag, the source filter sends this event code instead of calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a0e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a0e3-117">Requirements</span></span>



| <span data-ttu-id="5a0e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a0e3-118">Requirement</span></span> | <span data-ttu-id="5a0e3-119">Value</span><span class="sxs-lookup"><span data-stu-id="5a0e3-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a0e3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a0e3-120">Header</span></span><br/> | <dl> <span data-ttu-id="5a0e3-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a0e3-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a0e3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a0e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a0e3-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="5a0e3-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="5a0e3-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="5a0e3-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




