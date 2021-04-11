---
description: Indica el progreso de un objeto de habilitador de contenido. Los objetos que exponen la interfaz IMFContentEnabler pueden generar este evento para notificar a la aplicación el progreso de las acciones de habilitación del contenido.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Evento MEEnablerProgress (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275977"
---
# <a name="meenablerprogress-event"></a><span data-ttu-id="d953a-104">Evento MEEnablerProgress</span><span class="sxs-lookup"><span data-stu-id="d953a-104">MEEnablerProgress event</span></span>

<span data-ttu-id="d953a-105">Indica el progreso de un objeto de habilitador de contenido.</span><span class="sxs-lookup"><span data-stu-id="d953a-105">Signals the progress of a content enabler object.</span></span> <span data-ttu-id="d953a-106">Los objetos que exponen la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) pueden generar este evento para notificar a la aplicación el progreso de las acciones del habilitador de contenido.</span><span class="sxs-lookup"><span data-stu-id="d953a-106">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event to notify the application about the progress of the content enabler's actions.</span></span>

## <a name="event-values"></a><span data-ttu-id="d953a-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="d953a-107">Event values</span></span>

<span data-ttu-id="d953a-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="d953a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d953a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d953a-109">VARTYPE</span></span>               | <span data-ttu-id="d953a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d953a-110">Description</span></span>                                                               |
|-----------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="d953a-111">VT \_ LPWStr</span><span class="sxs-lookup"><span data-stu-id="d953a-111">VT\_LPWSTR</span></span><br/> | <span data-ttu-id="d953a-112">Cadena de caracteres anchos que describe el progreso.</span><span class="sxs-lookup"><span data-stu-id="d953a-112">Wide-character string that describes the progress.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d953a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d953a-113">Remarks</span></span>

<span data-ttu-id="d953a-114">Para recibir este evento, consulte la interfaz [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="d953a-114">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="d953a-115">Después, llame a [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), tal y como se describe en el tema [generadores de eventos multimedia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="d953a-115">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d953a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d953a-116">Requirements</span></span>



| <span data-ttu-id="d953a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d953a-117">Requirement</span></span> | <span data-ttu-id="d953a-118">Value</span><span class="sxs-lookup"><span data-stu-id="d953a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d953a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d953a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d953a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d953a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d953a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d953a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d953a-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d953a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d953a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d953a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d953a-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d953a-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d953a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d953a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d953a-126">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="d953a-126">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="d953a-127">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="d953a-127">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="d953a-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d953a-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




