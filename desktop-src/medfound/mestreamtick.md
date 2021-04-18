---
description: Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715307"
---
# <a name="mestreamtick-event"></a><span data-ttu-id="4a52a-103">Evento MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="4a52a-103">MEStreamTick event</span></span>

<span data-ttu-id="4a52a-104">Indica que una secuencia multimedia no tiene datos disponibles en un momento especificado.</span><span class="sxs-lookup"><span data-stu-id="4a52a-104">Signals that a media stream does not have data available at a specified time.</span></span>

## <a name="event-values"></a><span data-ttu-id="4a52a-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="4a52a-105">Event values</span></span>

<span data-ttu-id="4a52a-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4a52a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4a52a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4a52a-107">VARTYPE</span></span>           | <span data-ttu-id="4a52a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a52a-108">Description</span></span>                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="4a52a-109">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="4a52a-109">VT\_I8</span></span><br/> | <span data-ttu-id="4a52a-110">Hora a la que se produce la brecha, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="4a52a-110">Time at which the gap occurs, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4a52a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a52a-111">Remarks</span></span>

<span data-ttu-id="4a52a-112">Este evento señala una brecha en los datos.</span><span class="sxs-lookup"><span data-stu-id="4a52a-112">This event signals a gap in the data.</span></span> <span data-ttu-id="4a52a-113">El evento notifica a los componentes de nivel inferior que no esperan ningún dato en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="4a52a-113">The event notifies downstream components not to expect any data at the specified time.</span></span>

<span data-ttu-id="4a52a-114">El evento debe ser enviado por cualquier objeto que genere las marcas de tiempo para los ejemplos de medios de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4a52a-114">The event should be sent by whichever object generates the time stamps for the media samples in the stream.</span></span> <span data-ttu-id="4a52a-115">Dependiendo del formato de los datos, se puede:</span><span class="sxs-lookup"><span data-stu-id="4a52a-115">Depending on the format of the data, this is either:</span></span>

-   <span data-ttu-id="4a52a-116">El flujo de medios en el origen de medios (interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ) o</span><span class="sxs-lookup"><span data-stu-id="4a52a-116">The media stream on the media source ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface), or</span></span>
-   <span data-ttu-id="4a52a-117">La transformación del descodificador (interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).</span><span class="sxs-lookup"><span data-stu-id="4a52a-117">The decoder transform ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface).</span></span>

<span data-ttu-id="4a52a-118">Durante el intervalo, el objeto debe enviar el evento con la frecuencia con la que generaría normalmente ejemplos.</span><span class="sxs-lookup"><span data-stu-id="4a52a-118">During the gap, the object should send the event about as often as it would normally produce samples.</span></span> <span data-ttu-id="4a52a-119">Para vídeo, envíe un evento por cada fotograma que falta.</span><span class="sxs-lookup"><span data-stu-id="4a52a-119">For video, send one event for each missing frame.</span></span> <span data-ttu-id="4a52a-120">En el caso de audio, envíe el evento al menos una vez por segundo durante el intervalo.</span><span class="sxs-lookup"><span data-stu-id="4a52a-120">For audio, send the event at least once per second during the gap.</span></span> <span data-ttu-id="4a52a-121">El valor del evento es la marca de tiempo del ejemplo que falta.</span><span class="sxs-lookup"><span data-stu-id="4a52a-121">The value of the event is the time stamp of the missing sample.</span></span> <span data-ttu-id="4a52a-122">Envíe tantos eventos MEStreamTick como sea necesario para completar la brecha en los datos.</span><span class="sxs-lookup"><span data-stu-id="4a52a-122">Send as many MEStreamTick events as needed to fill the gap in the data.</span></span>

<span data-ttu-id="4a52a-123">Si un origen multimedia tiene varios flujos y hay un hueco en más de un flujo, cada flujo debe enviar eventos MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="4a52a-123">If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events.</span></span> <span data-ttu-id="4a52a-124">Por ejemplo, si hay una brecha en los datos de audio y vídeo, ambos flujos envían el evento.</span><span class="sxs-lookup"><span data-stu-id="4a52a-124">For example, if there is a gap in both audio and video data, then both streams send the event.</span></span>

<span data-ttu-id="4a52a-125">El evento MEStreamTick no completa una solicitud [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="4a52a-125">The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) request.</span></span> <span data-ttu-id="4a52a-126">El origen multimedia todavía debe enviar un evento [MEMediaSample](memediasample.md) para cada llamada a **RequestSample**.</span><span class="sxs-lookup"><span data-stu-id="4a52a-126">The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.</span></span>

<span data-ttu-id="4a52a-127">Los receptores de medios no pueden consumir este evento directamente.</span><span class="sxs-lookup"><span data-stu-id="4a52a-127">Media sinks cannot consume this event directly.</span></span> <span data-ttu-id="4a52a-128">Para indicar una brecha en el flujo en un receptor de multimedia, llame a [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) con un marcador de **\_ \_ paso de marcador MFSTREAMSINK** .</span><span class="sxs-lookup"><span data-stu-id="4a52a-128">To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) with an **MFSTREAMSINK\_MARKER\_TICK** marker.</span></span> <span data-ttu-id="4a52a-129">La canalización Media Foundation convierte los eventos MEStreamTick en marcadores de **\_ \_ graduación del marcador MFSTREAMSINK** cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4a52a-129">The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.</span></span>

<span data-ttu-id="4a52a-130">No establezca el atributo [**\_ discontinuidad MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) en el siguiente ejemplo de medio después de un evento MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="4a52a-130">Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event.</span></span> <span data-ttu-id="4a52a-131">El **atributo \_ discontinuidad de MFSampleExtension** implica que la marca de tiempo es descontinuada con las marcas de tiempo anteriores, mientras que MEStreamTick implica que las marcas de tiempo son continuas pero faltan algunos datos.</span><span class="sxs-lookup"><span data-stu-id="4a52a-131">The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.</span></span>

> [!Note]  
> <span data-ttu-id="4a52a-132">Una versión anterior de la documentación indicó incorrectamente que el ejemplo después de un evento MEStreamTick debe tener el [**atributo \_ discontinuidad MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="4a52a-132">An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a52a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a52a-133">Requirements</span></span>



| <span data-ttu-id="4a52a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a52a-134">Requirement</span></span> | <span data-ttu-id="4a52a-135">Value</span><span class="sxs-lookup"><span data-stu-id="4a52a-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a52a-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a52a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4a52a-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4a52a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4a52a-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a52a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4a52a-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a52a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a52a-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a52a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a52a-141"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a52a-141"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a52a-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a52a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a52a-143">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a52a-143">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




