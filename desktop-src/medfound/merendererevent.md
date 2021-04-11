---
description: Señala un evento de un receptor de medios que representa los datos multimedia.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275972"
---
# <a name="merendererevent-event"></a><span data-ttu-id="f6503-103">Evento MERendererEvent</span><span class="sxs-lookup"><span data-stu-id="f6503-103">MERendererEvent event</span></span>

<span data-ttu-id="f6503-104">Señala un evento de un receptor de medios que representa los datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="f6503-104">Signals an event from a media sink that renders media data.</span></span>

<span data-ttu-id="f6503-105">El [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) envía este evento cuando recibe un evento de usuario del presentador de EVR.</span><span class="sxs-lookup"><span data-stu-id="f6503-105">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) sends this event when it receives a user event from the EVR presenter.</span></span>

## <a name="event-values"></a><span data-ttu-id="f6503-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f6503-106">Event values</span></span>

<span data-ttu-id="f6503-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f6503-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f6503-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f6503-108">VARTYPE</span></span>           | <span data-ttu-id="f6503-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6503-109">Description</span></span>                        |
|-------------------|------------------------------------|
| <span data-ttu-id="f6503-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="f6503-110">VT\_I4</span></span><br/> | <span data-ttu-id="f6503-111">Código de evento.</span><span class="sxs-lookup"><span data-stu-id="f6503-111">Event code.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f6503-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6503-112">Remarks</span></span>

<span data-ttu-id="f6503-113">Si el presentador llama al método **IMediaEventSink:: Notify** de EVR con un código de evento en el usuario del intervalo de EC \_ o superior, el EVR envía este evento.</span><span class="sxs-lookup"><span data-stu-id="f6503-113">If the presenter calls the EVR's **IMediaEventSink::Notify** method with an event code in the range EC\_USER or higher, the EVR sends this event.</span></span> <span data-ttu-id="f6503-114">Los datos del evento son el código de evento que se pasó al método **Notify** .</span><span class="sxs-lookup"><span data-stu-id="f6503-114">The event data is the event code that was passed to the **Notify** method.</span></span>

<span data-ttu-id="f6503-115">Los parámetros de evento originales (*EventParam1* y *EventParam2* en el método **IMediaEventSink:: Notify** ) se omiten, por lo que el presentador debe establecer estos valores en **null**.</span><span class="sxs-lookup"><span data-stu-id="f6503-115">The original event parameters (*EventParam1* and *EventParam2* in the **IMediaEventSink::Notify** method) are ignored, so the presenter should set these values to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6503-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6503-116">Requirements</span></span>



| <span data-ttu-id="f6503-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6503-117">Requirement</span></span> | <span data-ttu-id="f6503-118">Value</span><span class="sxs-lookup"><span data-stu-id="f6503-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6503-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6503-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6503-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f6503-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6503-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6503-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6503-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6503-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f6503-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6503-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6503-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6503-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6503-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6503-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6503-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6503-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




