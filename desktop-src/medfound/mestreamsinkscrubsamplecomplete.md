---
description: Generado por un receptor de flujo cuando completa una solicitud de limpieza.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678377"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a><span data-ttu-id="d8fcc-103">Evento MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="d8fcc-103">MEStreamSinkScrubSampleComplete event</span></span>

<span data-ttu-id="d8fcc-104">Generado por un receptor de flujo cuando completa una solicitud de limpieza.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-104">Raised by a stream sink when it completes a scrubbing request.</span></span>

<span data-ttu-id="d8fcc-105">La limpieza se produce cuando la velocidad de reproducción es cero y el reloj de la presentación se inicia con una hora de srubbing especificada.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-105">Scrubbing occurs when the playback rate is zero and the presentation clock is started with a specified srubbing time.</span></span> <span data-ttu-id="d8fcc-106">Si un receptor de medios admite la limpieza, cada secuencia del receptor genera este evento cada vez que se llama al método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) mientras que la velocidad de reproducción es cero.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-106">If a media sink supports scrubbing, every stream on the sink raises this event whenever the [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) method is called while the playback rate is zero.</span></span>

<span data-ttu-id="d8fcc-107">Si el flujo representa datos durante la limpieza, envía el evento en cuanto se representan los datos.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-107">If the stream renders data while scrubbing, it sends the event as soon as the data is rendered.</span></span> <span data-ttu-id="d8fcc-108">Si la secuencia no representa datos, envía el evento inmediatamente después de que se llame a [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .</span><span class="sxs-lookup"><span data-stu-id="d8fcc-108">If the stream does not render data, it sends the event immediately after [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="d8fcc-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="d8fcc-109">Event values</span></span>

<span data-ttu-id="d8fcc-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d8fcc-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d8fcc-111">VARTYPE</span></span>              | <span data-ttu-id="d8fcc-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8fcc-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d8fcc-113">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="d8fcc-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d8fcc-114">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="d8fcc-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8fcc-115">Attributes</span></span>

<span data-ttu-id="d8fcc-116">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="d8fcc-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="d8fcc-117">Attribute</span></span>                                                                              | <span data-ttu-id="d8fcc-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8fcc-118">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8fcc-119">**\_hora de \_ SCRUBSAMPLE de eventos de MF \_**</span><span class="sxs-lookup"><span data-stu-id="d8fcc-119">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)<br/> | <span data-ttu-id="d8fcc-120">Tiempo de presentación para el que se representan los datos.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-120">Presentation time for which data was rendered.</span></span> <span data-ttu-id="d8fcc-121">Si el receptor de medios no representa los datos durante la limpieza, no establece este atributo.</span><span class="sxs-lookup"><span data-stu-id="d8fcc-121">If the media sink does not render data while scrubbing, it does not set this attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d8fcc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8fcc-122">Requirements</span></span>



| <span data-ttu-id="d8fcc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8fcc-123">Requirement</span></span> | <span data-ttu-id="d8fcc-124">Value</span><span class="sxs-lookup"><span data-stu-id="d8fcc-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8fcc-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8fcc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d8fcc-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d8fcc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d8fcc-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8fcc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d8fcc-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8fcc-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d8fcc-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8fcc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8fcc-130"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8fcc-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8fcc-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8fcc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8fcc-132">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d8fcc-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="d8fcc-133">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="d8fcc-133">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="d8fcc-134">MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="d8fcc-134">MESessionScrubSampleComplete</span></span>](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




