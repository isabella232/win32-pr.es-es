---
description: Lo genera un objeto habilitador de contenido cuando se completa la acción de habilitación de objetos.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119450"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="c34d3-103">Evento MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="c34d3-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="c34d3-104">Lo genera un objeto habilitador de contenido cuando se completa la acción de habilitación del objeto.</span><span class="sxs-lookup"><span data-stu-id="c34d3-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="c34d3-105">Los objetos que exponen [**la interfaz IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pueden generar este evento.</span><span class="sxs-lookup"><span data-stu-id="c34d3-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="c34d3-106">El evento se genera si se produce alguna de las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="c34d3-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="c34d3-107">El [**método IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="c34d3-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="c34d3-108">La aplicación llama [**a IMFContentEnabler::MonitorEnable y,**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)a continuación, la aplicación completa la solicitud HTTP POST, como se describe en el **método MonitorEnable.**</span><span class="sxs-lookup"><span data-stu-id="c34d3-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="c34d3-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="c34d3-109">Event values</span></span>

<span data-ttu-id="c34d3-110">Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c34d3-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c34d3-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c34d3-111">VARTYPE</span></span>              | <span data-ttu-id="c34d3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c34d3-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c34d3-113">VT \_ EMPTY</span><span class="sxs-lookup"><span data-stu-id="c34d3-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c34d3-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="c34d3-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="c34d3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c34d3-115">Remarks</span></span>

<span data-ttu-id="c34d3-116">El código de estado del evento puede contener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c34d3-116">The status code from the event may contain one of the following values.</span></span>



| <span data-ttu-id="c34d3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c34d3-117">Value</span></span>                                     | <span data-ttu-id="c34d3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c34d3-118">Description</span></span>                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c34d3-119">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="c34d3-119">**S\_OK**</span></span>                            | <span data-ttu-id="c34d3-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c34d3-120">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="c34d3-121">**NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED**</span><span class="sxs-lookup"><span data-stu-id="c34d3-121">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="c34d3-122">No se adquirió la licencia DRM.</span><span class="sxs-lookup"><span data-stu-id="c34d3-122">The DRM license was not acquired.</span></span> <span data-ttu-id="c34d3-123">Si el intento anterior [**usó AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), la aplicación debe intentar la adquisición no silenciosa.</span><span class="sxs-lookup"><span data-stu-id="c34d3-123">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="c34d3-124">**MONITOR DRM DE NS \_ \_ \_ \_ CANCELADO**</span><span class="sxs-lookup"><span data-stu-id="c34d3-124">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="c34d3-125">Se canceló la operación [**MonitorEnable.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)</span><span class="sxs-lookup"><span data-stu-id="c34d3-125">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="c34d3-126">Para recibir este evento, consulte la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para la [**interfaz IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)</span><span class="sxs-lookup"><span data-stu-id="c34d3-126">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="c34d3-127">A [**continuación, llame a IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), como se describe en el tema [Generadores de eventos multimedia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="c34d3-127">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c34d3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c34d3-128">Requirements</span></span>



| <span data-ttu-id="c34d3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c34d3-129">Requirement</span></span> | <span data-ttu-id="c34d3-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c34d3-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c34d3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c34d3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c34d3-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c34d3-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c34d3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c34d3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c34d3-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c34d3-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c34d3-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c34d3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c34d3-136"><dt>Mfobjects.h (incluir Mfidl.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c34d3-136"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34d3-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c34d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34d3-138">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="c34d3-138">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="c34d3-139">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="c34d3-139">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="c34d3-140">Media Foundation eventos</span><span class="sxs-lookup"><span data-stu-id="c34d3-140">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




