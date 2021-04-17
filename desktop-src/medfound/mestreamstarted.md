---
description: Generado por un flujo multimedia cuando el origen comienza sin búsquedas. Un flujo multimedia genera este evento cuando el origen del medio genera el evento MESourceStarted.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Evento MEStreamStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705990"
---
# <a name="mestreamstarted-event"></a><span data-ttu-id="6858a-104">Evento MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="6858a-104">MEStreamStarted event</span></span>

<span data-ttu-id="6858a-105">Generado por un flujo multimedia cuando el origen comienza sin búsquedas.</span><span class="sxs-lookup"><span data-stu-id="6858a-105">Raised by a media stream when the source starts without seeking.</span></span> <span data-ttu-id="6858a-106">Un flujo multimedia genera este evento cuando el origen del medio genera el evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="6858a-106">A media stream raises this event when the media source raises the [MESourceStarted](mesourcestarted.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="6858a-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6858a-107">Event values</span></span>

<span data-ttu-id="6858a-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6858a-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6858a-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6858a-109">VARTYPE</span></span>              | <span data-ttu-id="6858a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6858a-110">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6858a-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="6858a-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6858a-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="6858a-112">No event data.</span></span><br/> <br/>                                                                          |
| <span data-ttu-id="6858a-113">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="6858a-113">VT\_I8</span></span><br/>    | <span data-ttu-id="6858a-114">La hora de inicio, en unidades de 100-nanosegundos, con respecto a las marcas de tiempo de los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="6858a-114">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="6858a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6858a-115">Requirements</span></span>



| <span data-ttu-id="6858a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6858a-116">Requirement</span></span> | <span data-ttu-id="6858a-117">Value</span><span class="sxs-lookup"><span data-stu-id="6858a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6858a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6858a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6858a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6858a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6858a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6858a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6858a-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6858a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6858a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6858a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6858a-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6858a-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6858a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6858a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6858a-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6858a-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




