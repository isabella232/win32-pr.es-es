---
description: Generado por un receptor de flujo cuando completa la transición al estado de pausa.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Evento MEStreamSinkPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706707"
---
# <a name="mestreamsinkpaused-event"></a><span data-ttu-id="04518-103">Evento MEStreamSinkPaused</span><span class="sxs-lookup"><span data-stu-id="04518-103">MEStreamSinkPaused event</span></span>

<span data-ttu-id="04518-104">Generado por un receptor de flujo cuando completa la transición al estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="04518-104">Raised by a stream sink when it completes the transition to the paused state.</span></span> <span data-ttu-id="04518-105">La transición a en pausa se produce cuando se llama al método [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) en el reloj de presentación del receptor.</span><span class="sxs-lookup"><span data-stu-id="04518-105">The transition to paused occurs when the [**IMFPresentationClock::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) method is called on the sink's presentation clock.</span></span>

## <a name="event-values"></a><span data-ttu-id="04518-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="04518-106">Event values</span></span>

<span data-ttu-id="04518-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="04518-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="04518-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="04518-108">VARTYPE</span></span>              | <span data-ttu-id="04518-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="04518-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="04518-110">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="04518-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="04518-111">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="04518-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="04518-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04518-112">Requirements</span></span>



| <span data-ttu-id="04518-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="04518-113">Requirement</span></span> | <span data-ttu-id="04518-114">Value</span><span class="sxs-lookup"><span data-stu-id="04518-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04518-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04518-115">Minimum supported client</span></span><br/> | <span data-ttu-id="04518-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="04518-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="04518-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04518-117">Minimum supported server</span></span><br/> | <span data-ttu-id="04518-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="04518-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04518-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04518-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="04518-120"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04518-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04518-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="04518-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04518-122">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04518-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="04518-123">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="04518-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




