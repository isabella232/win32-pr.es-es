---
description: Generado por un receptor de flujo cuando completa la transición al estado detenido. La transición a Stopped se produce cuando se llama al método STOP IMFPresentationClock en el reloj de la presentación de receptores.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Evento MEStreamSinkStopped (Mfobjects. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082970"
---
# <a name="mestreamsinkstopped-event"></a><span data-ttu-id="3693e-104">Evento MEStreamSinkStopped</span><span class="sxs-lookup"><span data-stu-id="3693e-104">MEStreamSinkStopped event</span></span>

<span data-ttu-id="3693e-105">Generado por un receptor de flujo cuando completa la transición al estado detenido.</span><span class="sxs-lookup"><span data-stu-id="3693e-105">Raised by a stream sink when it completes the transition to the stopped state.</span></span> <span data-ttu-id="3693e-106">La transición a Stopped se produce cuando se llama al método [**IMFPresentationClock:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) en el reloj de presentación del receptor.</span><span class="sxs-lookup"><span data-stu-id="3693e-106">The transition to stopped occurs when the [**IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="3693e-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="3693e-107">Event values</span></span>

<span data-ttu-id="3693e-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="3693e-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3693e-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3693e-109">VARTYPE</span></span>              | <span data-ttu-id="3693e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3693e-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="3693e-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="3693e-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="3693e-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="3693e-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="3693e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3693e-113">Requirements</span></span>



| <span data-ttu-id="3693e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3693e-114">Requirement</span></span> | <span data-ttu-id="3693e-115">Value</span><span class="sxs-lookup"><span data-stu-id="3693e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3693e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3693e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3693e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3693e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3693e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3693e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3693e-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3693e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3693e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3693e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3693e-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3693e-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3693e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3693e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3693e-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3693e-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3693e-124">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="3693e-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




