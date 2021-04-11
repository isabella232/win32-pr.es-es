---
description: 'Generado por un flujo multimedia después de una llamada a IMFMediaSource:: Start produce una búsqueda en la secuencia. Un flujo multimedia genera este evento cuando el origen del medio genera el evento MESourceSeeked.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Evento MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275965"
---
# <a name="mestreamseeked-event"></a><span data-ttu-id="1bdae-104">Evento MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="1bdae-104">MEStreamSeeked event</span></span>

<span data-ttu-id="1bdae-105">Generado por un flujo multimedia después de una llamada a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) produce una búsqueda en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1bdae-105">Raised by a media stream after a call to [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causes a seek in the stream.</span></span> <span data-ttu-id="1bdae-106">Un flujo multimedia genera este evento cuando el origen del medio genera el evento [MESourceSeeked](mesourceseeked.md) .</span><span class="sxs-lookup"><span data-stu-id="1bdae-106">A media stream raises this event when the media source raises the [MESourceSeeked](mesourceseeked.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="1bdae-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="1bdae-107">Event values</span></span>

<span data-ttu-id="1bdae-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="1bdae-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1bdae-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1bdae-109">VARTYPE</span></span>           | <span data-ttu-id="1bdae-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bdae-110">Description</span></span>                                                        |
|-------------------|--------------------------------------------------------------------|
| <span data-ttu-id="1bdae-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="1bdae-111">VT\_I8</span></span><br/> | <span data-ttu-id="1bdae-112">Nueva hora de inicio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="1bdae-112">New starting time, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="1bdae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bdae-113">Requirements</span></span>



| <span data-ttu-id="1bdae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bdae-114">Requirement</span></span> | <span data-ttu-id="1bdae-115">Value</span><span class="sxs-lookup"><span data-stu-id="1bdae-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdae-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bdae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1bdae-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1bdae-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1bdae-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bdae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1bdae-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1bdae-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1bdae-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1bdae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bdae-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bdae-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bdae-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bdae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bdae-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1bdae-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




