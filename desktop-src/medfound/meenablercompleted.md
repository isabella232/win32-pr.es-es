---
description: Generado por un objeto de habilitador de contenido cuando se completa la acción de habilitación de objetos.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155592"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="a1c32-103">Evento MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="a1c32-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="a1c32-104">Lo genera un objeto de habilitador de contenido cuando se completa la acción de habilitación del objeto.</span><span class="sxs-lookup"><span data-stu-id="a1c32-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="a1c32-105">Los objetos que exponen la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pueden generar este evento.</span><span class="sxs-lookup"><span data-stu-id="a1c32-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="a1c32-106">El evento se desencadena si se produce alguno de los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="a1c32-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="a1c32-107">El método [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a1c32-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="a1c32-108">La aplicación llama a [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)y, a continuación, la aplicación completa la solicitud HTTP POST, como se describe en el método **MonitorEnable** .</span><span class="sxs-lookup"><span data-stu-id="a1c32-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="a1c32-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a1c32-109">Event values</span></span>

<span data-ttu-id="a1c32-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1c32-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a1c32-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a1c32-111">VARTYPE</span></span>              | <span data-ttu-id="a1c32-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1c32-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a1c32-113">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="a1c32-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a1c32-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="a1c32-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a1c32-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1c32-115">Remarks</span></span>

<span data-ttu-id="a1c32-116">El código de estado del evento puede contener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1c32-116">The status code from the event may contain one of the following values.</span></span>



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c32-117">**S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="a1c32-117">**S\_OK**</span></span>                            | <span data-ttu-id="a1c32-118">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a1c32-118">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="a1c32-119">**NOTACQUIRED de licencia de DRM de NS \_ E \_ DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a1c32-119">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="a1c32-120">No se adquirió la licencia DRM.</span><span class="sxs-lookup"><span data-stu-id="a1c32-120">The DRM license was not acquired.</span></span> <span data-ttu-id="a1c32-121">Si el intento anterior usaba [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), la aplicación debe intentar la adquisición no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="a1c32-121">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="a1c32-122">**MONITOR de DRM de NS \_ \_ \_ \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="a1c32-122">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="a1c32-123">Se canceló la operación [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) .</span><span class="sxs-lookup"><span data-stu-id="a1c32-123">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="a1c32-124">Para recibir este evento, consulte la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="a1c32-124">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="a1c32-125">Después, llame a [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), tal y como se describe en el tema [generadores de eventos multimedia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="a1c32-125">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1c32-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1c32-126">Requirements</span></span>



| <span data-ttu-id="a1c32-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1c32-127">Requirement</span></span> | <span data-ttu-id="a1c32-128">Value</span><span class="sxs-lookup"><span data-stu-id="a1c32-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c32-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1c32-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c32-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a1c32-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a1c32-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1c32-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c32-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1c32-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1c32-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1c32-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1c32-134"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1c32-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c32-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1c32-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c32-136">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="a1c32-136">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="a1c32-137">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="a1c32-137">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="a1c32-138">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a1c32-138">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




