---
description: Se genera cuando un receptor de medios deja de ser válido.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Evento MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275584"
---
# <a name="mesinkinvalidated-event"></a><span data-ttu-id="12822-103">Evento MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="12822-103">MESinkInvalidated event</span></span>

<span data-ttu-id="12822-104">Se genera cuando un receptor de medios deja de ser válido.</span><span class="sxs-lookup"><span data-stu-id="12822-104">Raised when a media sink becomes invalid.</span></span>

## <a name="event-values"></a><span data-ttu-id="12822-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="12822-105">Event values</span></span>

<span data-ttu-id="12822-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="12822-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="12822-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="12822-107">VARTYPE</span></span>              | <span data-ttu-id="12822-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="12822-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="12822-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="12822-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="12822-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="12822-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="12822-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="12822-111">Attributes</span></span>

<span data-ttu-id="12822-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="12822-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="12822-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="12822-113">Attribute</span></span>                                                                    | <span data-ttu-id="12822-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="12822-114">Description</span></span>                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="12822-115">**\_nodo de \_ salida de evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="12822-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="12822-116">Identifica el nodo de la topología para este receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="12822-116">Identifies the topology node for this media sink.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="12822-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12822-117">Remarks</span></span>

<span data-ttu-id="12822-118">La sesión multimedia genera este evento si recibe alguno de los siguientes eventos del receptor de medios:</span><span class="sxs-lookup"><span data-stu-id="12822-118">The Media Session raises this event if it receives any of the following events from the media sink:</span></span>

-   [<span data-ttu-id="12822-119">MEAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="12822-119">MEAudioSessionDeviceRemoved</span></span>](meaudiosessiondeviceremoved.md)

-   [<span data-ttu-id="12822-120">MEAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="12822-120">MEAudioSessionDisconnected</span></span>](meaudiosessiondisconnected.md)

-   [<span data-ttu-id="12822-121">MEAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="12822-121">MEAudioSessionExclusiveModeOverride</span></span>](meaudiosessionexclusivemodeoverride.md)

-   [<span data-ttu-id="12822-122">MEAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="12822-122">MEAudioSessionFormatChanged</span></span>](meaudiosessionformatchanged.md)

-   [<span data-ttu-id="12822-123">MEAudioSessionServerShutdown</span><span class="sxs-lookup"><span data-stu-id="12822-123">MEAudioSessionServerShutdown</span></span>](meaudiosessionservershutdown.md)

<span data-ttu-id="12822-124">Un receptor de medios también puede generar este evento, en cuyo caso la sesión multimedia establece el atributo de [**\_ nodo de \_ salida \_ de evento MF**](mf-event-output-node-attribute.md) en el evento y reenvía el evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="12822-124">A media sink can also raise this event, in which case the Media Session sets the [**MF\_EVENT\_OUTPUT\_NODE**](mf-event-output-node-attribute.md) attribute on the event and forwards the event to the application.</span></span>

<span data-ttu-id="12822-125">Si la aplicación recibe este evento, debe volver a crear el receptor de medios y poner en cola la topología de nuevo.</span><span class="sxs-lookup"><span data-stu-id="12822-125">If the application receives this event, it needs to recreate the media sink and queue the topology again.</span></span>

## <a name="requirements"></a><span data-ttu-id="12822-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12822-126">Requirements</span></span>



| <span data-ttu-id="12822-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="12822-127">Requirement</span></span> | <span data-ttu-id="12822-128">Value</span><span class="sxs-lookup"><span data-stu-id="12822-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12822-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12822-129">Minimum supported client</span></span><br/> | <span data-ttu-id="12822-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="12822-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12822-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12822-131">Minimum supported server</span></span><br/> | <span data-ttu-id="12822-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12822-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12822-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12822-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="12822-134"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12822-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12822-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="12822-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12822-136">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12822-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




