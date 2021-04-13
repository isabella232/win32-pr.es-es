---
description: Se genera cuando un origen multimedia comienza sin búsquedas.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Evento MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544374"
---
# <a name="mesourcestarted-event"></a><span data-ttu-id="6679f-103">Evento MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="6679f-103">MESourceStarted event</span></span>

<span data-ttu-id="6679f-104">Se genera cuando un origen multimedia comienza sin búsquedas.</span><span class="sxs-lookup"><span data-stu-id="6679f-104">Raised when a media source starts without seeking.</span></span>

## <a name="event-values"></a><span data-ttu-id="6679f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6679f-105">Event values</span></span>

<span data-ttu-id="6679f-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6679f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6679f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6679f-107">VARTYPE</span></span>              | <span data-ttu-id="6679f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6679f-108">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6679f-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="6679f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6679f-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="6679f-110">No event data.</span></span> <span data-ttu-id="6679f-111">La hora de inicio era desde la posición actual.</span><span class="sxs-lookup"><span data-stu-id="6679f-111">The start time was from the current position.</span></span><br/> <br/>                            |
| <span data-ttu-id="6679f-112">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="6679f-112">VT\_I8</span></span><br/>    | <span data-ttu-id="6679f-113">La hora de inicio, en unidades de 100-nanosegundos, con respecto a las marcas de tiempo de los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="6679f-113">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="6679f-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="6679f-114">Attributes</span></span>

<span data-ttu-id="6679f-115">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="6679f-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="6679f-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="6679f-116">Attribute</span></span>                                                                                     | <span data-ttu-id="6679f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6679f-117">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6679f-118">**\_ \_ Inicio real del origen de eventos MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6679f-118">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)<br/> | <span data-ttu-id="6679f-119">Hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="6679f-119">Start time.</span></span> <span data-ttu-id="6679f-120">El origen de medios establece este atributo si se reinicia desde su posición actual.</span><span class="sxs-lookup"><span data-stu-id="6679f-120">The media source sets this attribute if it restarts from its current position.</span></span><br/> <br/>                     |
| [<span data-ttu-id="6679f-121">**\_ \_ Inicio falso de origen de evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6679f-121">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)<br/>     | <span data-ttu-id="6679f-122">Especifica si la topología de segmento actual está vacía.</span><span class="sxs-lookup"><span data-stu-id="6679f-122">Specifies whether the current segment topology is empty.</span></span> <span data-ttu-id="6679f-123">El origen del secuenciador establece este atributo.</span><span class="sxs-lookup"><span data-stu-id="6679f-123">The sequencer source sets this attribute.</span></span><br/> <br/>             |
| [<span data-ttu-id="6679f-124">**\_origen de evento MF \_ \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="6679f-124">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)<br/>  | <span data-ttu-id="6679f-125">Hora de inicio de un segmento, con respecto al inicio de la presentación.</span><span class="sxs-lookup"><span data-stu-id="6679f-125">Start time for a segment, relative to the start of the presentation.</span></span> <span data-ttu-id="6679f-126">El origen del secuenciador establece este atributo.</span><span class="sxs-lookup"><span data-stu-id="6679f-126">The sequencer source sets this attribute.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="6679f-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6679f-127">Remarks</span></span>

<span data-ttu-id="6679f-128">Un origen multimedia genera este evento cuando se inicia desde un estado detenido o se inicia a partir de un estado de pausa en la misma posición del origen.</span><span class="sxs-lookup"><span data-stu-id="6679f-128">A media source raises this event when it starts from a stopped state, or starts from a paused state at the same position in the source.</span></span> <span data-ttu-id="6679f-129">El evento se desencadena si el método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="6679f-129">The event is raised if the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method returns S\_OK.</span></span>

<span data-ttu-id="6679f-130">Si el origen multimedia se inicia desde la posición actual y el estado anterior del origen se estaba ejecutando o en pausa, los datos del evento pueden estar vacíos (VT \_ vacío).</span><span class="sxs-lookup"><span data-stu-id="6679f-130">If the media source starts from the current position and the source's previous state was running or paused, the event data can empty (VT\_EMPTY).</span></span> <span data-ttu-id="6679f-131">Si los datos de evento están \_ vacíos en VT, el origen de medios podría establecer el atributo de [**\_ \_ \_ \_ Inicio real del origen de eventos MF**](mf-event-source-actual-start-attribute.md) con la hora de inicio real.</span><span class="sxs-lookup"><span data-stu-id="6679f-131">If the event data is VT\_EMPTY, the media source might set the [**MF\_EVENT\_SOURCE\_ACTUAL\_START**](mf-event-source-actual-start-attribute.md) attribute with the actual starting time.</span></span>

<span data-ttu-id="6679f-132">Si el origen multimedia se inicia desde una nueva posición o se detuvo el estado anterior del origen, los datos del evento deben ser la hora de inicio (VT \_ i8).</span><span class="sxs-lookup"><span data-stu-id="6679f-132">If the media source starts from a new position, or the source's previous state was stopped, the event data must be the starting time (VT\_I8).</span></span>

<span data-ttu-id="6679f-133">Si el método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produce una búsqueda, el origen multimedia envía el evento [MESourceSeeked](mesourceseeked.md) en lugar de MESourceStarted.</span><span class="sxs-lookup"><span data-stu-id="6679f-133">If the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method causes a seek, the media source sends the [MESourceSeeked](mesourceseeked.md) event instead of MESourceStarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6679f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6679f-134">Requirements</span></span>



| <span data-ttu-id="6679f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6679f-135">Requirement</span></span> | <span data-ttu-id="6679f-136">Value</span><span class="sxs-lookup"><span data-stu-id="6679f-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6679f-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6679f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6679f-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6679f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6679f-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6679f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6679f-140">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6679f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6679f-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6679f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6679f-142"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6679f-142"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6679f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6679f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6679f-144">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6679f-144">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




