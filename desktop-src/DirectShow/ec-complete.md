---
description: Se han representado todos los datos de una secuencia determinada.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680257"
---
# <a name="ec_complete"></a><span data-ttu-id="fed49-103">EC \_ completado</span><span class="sxs-lookup"><span data-stu-id="fed49-103">EC\_COMPLETE</span></span>

<span data-ttu-id="fed49-104">Se han representado todos los datos de una secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="fed49-104">All data from a particular stream has been rendered.</span></span>

## <a name="parameters"></a><span data-ttu-id="fed49-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fed49-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed49-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="fed49-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="fed49-107">(**HRESULT**) Estado de la secuencia al finalizar.</span><span class="sxs-lookup"><span data-stu-id="fed49-107">(**HRESULT**) Status of the stream on completion.</span></span> <span data-ttu-id="fed49-108">Si no se produjo ningún error durante la reproducción, el valor es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fed49-108">If no errors occurred during playback, the value is S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="fed49-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fed49-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fed49-110">(**IUnknown** \* ) Cero o un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del representador.</span><span class="sxs-lookup"><span data-stu-id="fed49-110">(**IUnknown**\*) Zero, or a pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="fed49-111">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="fed49-111">Default Action</span></span>

<span data-ttu-id="fed49-112">De forma predeterminada, el administrador de gráficos de filtro no reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fed49-112">By default, the filter graph manager does not forward this event to the application.</span></span> <span data-ttu-id="fed49-113">Sin embargo, después de que se **\_ completen** todas las secuencias del informe de gráficos, el administrador de gráficos de filtros publica un evento de **EC \_ Complete** independiente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fed49-113">However, after all the streams in the graph report **EC\_COMPLETE**, the filter graph manager posts a separate **EC\_COMPLETE** event to the application.</span></span>

<span data-ttu-id="fed49-114">Si la acción predeterminada está deshabilitada para este evento, la aplicación recibe todos los eventos de **\_ finalización de EC** de los representadores.</span><span class="sxs-lookup"><span data-stu-id="fed49-114">If the default action is disabled for this event, the application receives all of the **EC\_COMPLETE** events from the renderers.</span></span>

## <a name="remarks"></a><span data-ttu-id="fed49-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fed49-115">Remarks</span></span>

<span data-ttu-id="fed49-116">Un filtro de representador envía este evento cuando recibe un aviso de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="fed49-116">A renderer filter sends this event when it receives an end-of-stream notice.</span></span> <span data-ttu-id="fed49-117">(El final de la secuencia se señaliza a través del método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ). El filtro envía exactamente un evento de **\_ finalización de EC** para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="fed49-117">(End-of-stream is signaled through the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.) The filter sends exactly one **EC\_COMPLETE** event for each stream.</span></span> <span data-ttu-id="fed49-118">El filtro debe procesar cualquier ejemplo pendiente antes de enviar el evento.</span><span class="sxs-lookup"><span data-stu-id="fed49-118">The filter must process any pending samples before it sends the event.</span></span> <span data-ttu-id="fed49-119">Al detener un representador, se restablece cualquier estado de final de secuencia que se almacenó en caché.</span><span class="sxs-lookup"><span data-stu-id="fed49-119">Stopping a renderer resets any end-of-stream state that was cached.</span></span>

<span data-ttu-id="fed49-120">Si el representador está en pausa, no envía la **\_ finalización de EC** hasta que se llama al método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) .</span><span class="sxs-lookup"><span data-stu-id="fed49-120">If the renderer is paused, it does not send **EC\_COMPLETE** until the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method is called.</span></span> <span data-ttu-id="fed49-121">Además, sigue enviando eventos de **\_ finalización de EC** para cada transición de la pausa a la ejecución hasta que el filtro se detenga o se vacíe.</span><span class="sxs-lookup"><span data-stu-id="fed49-121">Furthermore, it continues to send **EC\_COMPLETE** events for each transition from pause to run, until the filter is either stopped or flushed.</span></span>

<span data-ttu-id="fed49-122">Los filtros establecen el parámetro *lParam2* en un puntero [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="fed49-122">Filters set the *lParam2* parameter to an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="fed49-123">Si la acción predeterminada está habilitada, el administrador de gráficos de filtro establece este parámetro en cero.</span><span class="sxs-lookup"><span data-stu-id="fed49-123">If the default action is enabled, the filter graph manager sets this parameter to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed49-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fed49-124">Requirements</span></span>



| <span data-ttu-id="fed49-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed49-125">Requirement</span></span> | <span data-ttu-id="fed49-126">Value</span><span class="sxs-lookup"><span data-stu-id="fed49-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fed49-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fed49-127">Header</span></span><br/> | <dl> <span data-ttu-id="fed49-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="fed49-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed49-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fed49-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed49-130">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="fed49-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="fed49-131">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="fed49-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="fed49-132">Representadores de vídeo alternativos</span><span class="sxs-lookup"><span data-stu-id="fed49-132">Alternative Video Renderers</span></span>](alternative-video-renderers.md)
</dt> </dl>

 

 




