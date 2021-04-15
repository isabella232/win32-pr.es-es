---
description: Generado por un receptor de flujo cuando completa la transición al estado en ejecución.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Evento MEStreamSinkStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715657"
---
# <a name="mestreamsinkstarted-event"></a><span data-ttu-id="25693-103">Evento MEStreamSinkStarted</span><span class="sxs-lookup"><span data-stu-id="25693-103">MEStreamSinkStarted event</span></span>

<span data-ttu-id="25693-104">Generado por un receptor de flujo cuando completa la transición al estado en ejecución.</span><span class="sxs-lookup"><span data-stu-id="25693-104">Raised by a stream sink when it completes the transition to the running state.</span></span> <span data-ttu-id="25693-105">La transición a Running se produce cuando se llama al método [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) en el reloj de presentación del receptor.</span><span class="sxs-lookup"><span data-stu-id="25693-105">The transition to running occurs when the [**IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) method is called on the sink's presentation clock.</span></span> <span data-ttu-id="25693-106">El receptor de medios recibe la notificación a través de su método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) o [**IMFClockStateSink:: OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) .</span><span class="sxs-lookup"><span data-stu-id="25693-106">The media sink receives the notification through its [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) or [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="25693-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="25693-107">Event values</span></span>

<span data-ttu-id="25693-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="25693-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="25693-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="25693-109">VARTYPE</span></span>              | <span data-ttu-id="25693-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="25693-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="25693-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="25693-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="25693-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="25693-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="25693-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25693-113">Requirements</span></span>



| <span data-ttu-id="25693-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="25693-114">Requirement</span></span> | <span data-ttu-id="25693-115">Value</span><span class="sxs-lookup"><span data-stu-id="25693-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25693-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25693-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25693-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="25693-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25693-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25693-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25693-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="25693-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25693-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25693-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25693-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25693-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25693-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="25693-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25693-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="25693-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="25693-124">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="25693-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




