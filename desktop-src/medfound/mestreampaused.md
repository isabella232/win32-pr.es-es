---
description: Generado por un flujo multimedia cuando el método IMFMediaSource::P ause se completa de forma asincrónica.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Evento MEStreamPaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715309"
---
# <a name="mestreampaused-event"></a><span data-ttu-id="43d03-103">Evento MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="43d03-103">MEStreamPaused event</span></span>

<span data-ttu-id="43d03-104">Generado por un flujo multimedia cuando el método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="43d03-104">Raised by a media stream when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="43d03-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="43d03-105">Event values</span></span>

<span data-ttu-id="43d03-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="43d03-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="43d03-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="43d03-107">VARTYPE</span></span>              | <span data-ttu-id="43d03-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="43d03-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="43d03-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="43d03-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="43d03-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="43d03-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="43d03-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43d03-111">Remarks</span></span>

<span data-ttu-id="43d03-112">Cada flujo activo de la presentación envía este evento.</span><span class="sxs-lookup"><span data-stu-id="43d03-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="43d03-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43d03-113">Requirements</span></span>



| <span data-ttu-id="43d03-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="43d03-114">Requirement</span></span> | <span data-ttu-id="43d03-115">Value</span><span class="sxs-lookup"><span data-stu-id="43d03-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d03-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43d03-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43d03-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="43d03-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="43d03-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43d03-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43d03-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="43d03-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="43d03-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43d03-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d03-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43d03-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d03-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="43d03-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d03-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="43d03-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




