---
description: Un representador de vídeo requiere volver a pintar.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689955"
---
# <a name="ec_repaint"></a><span data-ttu-id="0fced-103">repintar EC \_</span><span class="sxs-lookup"><span data-stu-id="0fced-103">EC\_REPAINT</span></span>

<span data-ttu-id="0fced-104">Un representador de vídeo requiere volver a pintar.</span><span class="sxs-lookup"><span data-stu-id="0fced-104">A video renderer requires a repaint.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fced-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0fced-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fced-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0fced-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0fced-107">(**IUnknown** \* ) Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada del representador de vídeo, o **null**.</span><span class="sxs-lookup"><span data-stu-id="0fced-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the video renderer's input pin, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0fced-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0fced-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0fced-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="0fced-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0fced-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="0fced-110">Default Action</span></span>

<span data-ttu-id="0fced-111">El parámetro *lParam1* podría especificar el PIN de entrada del representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0fced-111">The *lParam1* parameter might specify the video renderer's input pin.</span></span> <span data-ttu-id="0fced-112">Si es así, el administrador de gráficos de filtro busca el PIN de salida conectado a ese pin y lo consulta para la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="0fced-112">If so, the filter graph manager finds the output pin connected to that pin and queries it for the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="0fced-113">Si el PIN de salida admite **IMediaEventSink**, el administrador de gráficos de filtros llama a [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) con el \_ código de evento de Repaint de EC.</span><span class="sxs-lookup"><span data-stu-id="0fced-113">If the output pin supports **IMediaEventSink**, the filter graph manager calls [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) with the EC\_REPAINT event code.</span></span> <span data-ttu-id="0fced-114">Esto proporciona al filtro de nivel superior la oportunidad de volver a enviar el último ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0fced-114">This gives the upstream filter the opportunity to re-send the last sample.</span></span>

<span data-ttu-id="0fced-115">Si *lParam1* es **null**, o si el PIN no admite [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), o si se produce un error en el método [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) , el administrador de gráficos de filtro controla el \_ evento re Repaint por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="0fced-115">If *lParam1* is **NULL**, or if the pin does not support [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), or if the [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method fails, the filter graph manager handles the EC\_REPAINT event by itself.</span></span> <span data-ttu-id="0fced-116">Su comportamiento depende del estado del gráfico:</span><span class="sxs-lookup"><span data-stu-id="0fced-116">Its behavior depends on the state of the graph:</span></span>

-   <span data-ttu-id="0fced-117">Running: omite el evento.</span><span class="sxs-lookup"><span data-stu-id="0fced-117">Running: Ignores the event.</span></span> <span data-ttu-id="0fced-118">(El representador recibirá el siguiente ejemplo en el flujo).</span><span class="sxs-lookup"><span data-stu-id="0fced-118">(The renderer will receive the next sample in the stream.)</span></span>
-   <span data-ttu-id="0fced-119">En pausa: busca el gráfico en su ubicación actual, con lo que se vacía el filtro y se vuelven a poner en cola los datos.</span><span class="sxs-lookup"><span data-stu-id="0fced-119">Paused: Seeks the graph to its current location, thereby flushing the filter and re-queuing the data.</span></span>
-   <span data-ttu-id="0fced-120">Stopped: pausa y detiene el gráfico, con lo que se vuelven a poner en cola los datos.</span><span class="sxs-lookup"><span data-stu-id="0fced-120">Stopped: Pauses and stops the graph, thereby re-queuing the data.</span></span>

<span data-ttu-id="0fced-121">De forma predeterminada, el administrador de gráficos de filtro no pasa este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0fced-121">By default, the filter graph manager does not pass this event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fced-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fced-122">Remarks</span></span>

<span data-ttu-id="0fced-123">Los representadores de vídeo envían este mensaje cuando reciben un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) y no tienen datos para mostrar.</span><span class="sxs-lookup"><span data-stu-id="0fced-123">Video renderers send this message when they receive a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message and have no data to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fced-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fced-124">Requirements</span></span>



| <span data-ttu-id="0fced-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fced-125">Requirement</span></span> | <span data-ttu-id="0fced-126">Value</span><span class="sxs-lookup"><span data-stu-id="0fced-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fced-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fced-127">Header</span></span><br/> | <dl> <span data-ttu-id="0fced-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fced-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fced-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fced-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fced-130">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="0fced-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0fced-131">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="0fced-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

