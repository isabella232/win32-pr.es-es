---
description: La inicia la sesión multimedia cuando completa una solicitud de limpieza.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Evento MESessionScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908471"
---
# <a name="mesessionscrubsamplecomplete-event"></a><span data-ttu-id="b53f9-103">Evento MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="b53f9-103">MESessionScrubSampleComplete event</span></span>

<span data-ttu-id="b53f9-104">La inicia la sesión multimedia cuando completa una solicitud de limpieza.</span><span class="sxs-lookup"><span data-stu-id="b53f9-104">Raised by the Media Session when it completes a scrubbing request.</span></span>

<span data-ttu-id="b53f9-105">La limpieza se produce cuando la velocidad de reproducción es cero y la aplicación llama a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="b53f9-105">Scrubbing occurs when the playback rate is zero and the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="b53f9-106">Este evento se desencadena después de que cada receptor de flujo haya completado la solicitud de limpieza.</span><span class="sxs-lookup"><span data-stu-id="b53f9-106">This event is raised after every stream sink has completed the scrubbing request.</span></span>

## <a name="event-values"></a><span data-ttu-id="b53f9-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="b53f9-107">Event values</span></span>

<span data-ttu-id="b53f9-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="b53f9-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b53f9-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b53f9-109">VARTYPE</span></span>              | <span data-ttu-id="b53f9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b53f9-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b53f9-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="b53f9-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b53f9-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="b53f9-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b53f9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b53f9-113">Requirements</span></span>



| <span data-ttu-id="b53f9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b53f9-114">Requirement</span></span> | <span data-ttu-id="b53f9-115">Value</span><span class="sxs-lookup"><span data-stu-id="b53f9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b53f9-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b53f9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b53f9-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b53f9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b53f9-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b53f9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b53f9-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b53f9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b53f9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b53f9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b53f9-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b53f9-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b53f9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b53f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53f9-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b53f9-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b53f9-124">MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="b53f9-124">MEStreamSinkScrubSampleComplete</span></span>](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




