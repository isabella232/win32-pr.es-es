---
description: Generado por el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento. Cuando se completa el segmento final, el origen del secuenciador genera un evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908476"
---
# <a name="meendofpresentationsegment-event"></a><span data-ttu-id="70ea0-104">Evento MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="70ea0-104">MEEndOfPresentationSegment event</span></span>

<span data-ttu-id="70ea0-105">Generado por el origen del secuenciador cuando se completa un segmento y va seguido de otro segmento.</span><span class="sxs-lookup"><span data-stu-id="70ea0-105">Raised by the sequencer source when a segment is completed and is followed by another segment.</span></span> <span data-ttu-id="70ea0-106">Cuando se completa el segmento final, el origen del secuenciador genera un evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="70ea0-106">When the final segment is completed, the sequencer source raises an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

<span data-ttu-id="70ea0-107">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="70ea0-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="70ea0-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="70ea0-108">Event values</span></span>

<span data-ttu-id="70ea0-109">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="70ea0-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="70ea0-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="70ea0-110">VARTYPE</span></span>              | <span data-ttu-id="70ea0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="70ea0-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="70ea0-112">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="70ea0-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="70ea0-113">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="70ea0-113">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="70ea0-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="70ea0-114">Attributes</span></span>

<span data-ttu-id="70ea0-115">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="70ea0-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="70ea0-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="70ea0-116">Attribute</span></span>                                                                                               | <span data-ttu-id="70ea0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="70ea0-117">Description</span></span>                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="70ea0-118">**\_topología de origen de eventos MF \_ \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="70ea0-118">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="70ea0-119">Especifica si el origen del secuenciador canceló este segmento.</span><span class="sxs-lookup"><span data-stu-id="70ea0-119">Specifies whether the sequencer source canceled this segment.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="70ea0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70ea0-120">Requirements</span></span>



| <span data-ttu-id="70ea0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ea0-121">Requirement</span></span> | <span data-ttu-id="70ea0-122">Value</span><span class="sxs-lookup"><span data-stu-id="70ea0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ea0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70ea0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70ea0-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70ea0-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="70ea0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70ea0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70ea0-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="70ea0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70ea0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70ea0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="70ea0-128"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70ea0-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ea0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="70ea0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ea0-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70ea0-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="70ea0-131">Acerca del origen del secuenciador</span><span class="sxs-lookup"><span data-stu-id="70ea0-131">About the Sequencer Source</span></span>](about-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="70ea0-132">Eventos de origen de Sequencer</span><span class="sxs-lookup"><span data-stu-id="70ea0-132">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




