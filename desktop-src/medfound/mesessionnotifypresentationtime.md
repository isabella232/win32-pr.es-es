---
description: La inicia la sesión multimedia cuando se inicia una nueva presentación. Este evento indica cuándo se iniciará la presentación y el desplazamiento entre el tiempo de presentación y la hora de origen.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648265"
---
# <a name="mesessionnotifypresentationtime-event"></a><span data-ttu-id="66a35-104">Evento MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="66a35-104">MESessionNotifyPresentationTime event</span></span>

<span data-ttu-id="66a35-105">La inicia la sesión multimedia cuando se inicia una nueva presentación.</span><span class="sxs-lookup"><span data-stu-id="66a35-105">Raised by the Media Session when a new presentation starts.</span></span> <span data-ttu-id="66a35-106">Este evento indica cuándo se iniciará la presentación y el desplazamiento entre el tiempo de presentación y la hora de origen.</span><span class="sxs-lookup"><span data-stu-id="66a35-106">This event indicates when the presentation will start and the offset between the presentation time and the source time.</span></span>

## <a name="event-values"></a><span data-ttu-id="66a35-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="66a35-107">Event values</span></span>

<span data-ttu-id="66a35-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="66a35-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="66a35-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="66a35-109">VARTYPE</span></span>              | <span data-ttu-id="66a35-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="66a35-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="66a35-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="66a35-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="66a35-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="66a35-112">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="66a35-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="66a35-113">Attributes</span></span>

<span data-ttu-id="66a35-114">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="66a35-114">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="66a35-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="66a35-115">Attribute</span></span>                                                                                                                   | <span data-ttu-id="66a35-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="66a35-116">Description</span></span>                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66a35-117">**\_tiempo de \_ presentación de inicio de evento de MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="66a35-117">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)<br/>                       | <span data-ttu-id="66a35-118">Hora de inicio de la presentación.</span><span class="sxs-lookup"><span data-stu-id="66a35-118">Starting time for the presentation.</span></span><br/> <br/>                                                      |
| [<span data-ttu-id="66a35-119">**\_desplazamiento de \_ tiempo de presentación de evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="66a35-119">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/>                     | <span data-ttu-id="66a35-120">Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="66a35-120">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/>                 |
| [<span data-ttu-id="66a35-121">**\_ \_ \_ \_ tiempo de presentación de inicio \_ de evento MF en la \_ salida**</span><span class="sxs-lookup"><span data-stu-id="66a35-121">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md)<br/> | <span data-ttu-id="66a35-122">Tiempo de presentación cuando los receptores de medios van a representar el primer ejemplo de la nueva topología.</span><span class="sxs-lookup"><span data-stu-id="66a35-122">Presentation time when the media sinks will render the first sample of the new topology.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="66a35-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a35-123">Requirements</span></span>



| <span data-ttu-id="66a35-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a35-124">Requirement</span></span> | <span data-ttu-id="66a35-125">Value</span><span class="sxs-lookup"><span data-stu-id="66a35-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a35-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66a35-126">Minimum supported client</span></span><br/> | <span data-ttu-id="66a35-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66a35-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="66a35-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66a35-128">Minimum supported server</span></span><br/> | <span data-ttu-id="66a35-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="66a35-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66a35-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66a35-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="66a35-131"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66a35-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a35-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="66a35-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a35-133">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="66a35-133">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="66a35-134">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66a35-134">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




