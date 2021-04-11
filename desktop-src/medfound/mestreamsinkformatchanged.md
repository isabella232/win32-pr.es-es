---
description: Generado por un receptor de flujo cuando el tipo de medio de los receptores ya no es válido.
ms.assetid: 9eeb4262-1593-4c5f-9341-ebd328b586e7
title: Evento MEStreamSinkFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e04c62072f69425079753ef4d0a56edcf8d65d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275964"
---
# <a name="mestreamsinkformatchanged-event"></a><span data-ttu-id="2a36a-103">Evento MEStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="2a36a-103">MEStreamSinkFormatChanged event</span></span>

<span data-ttu-id="2a36a-104">Generado por un receptor de flujo cuando el tipo de medio del receptor ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="2a36a-104">Raised by a stream sink when the sink's media type is no longer valid.</span></span>

## <a name="event-values"></a><span data-ttu-id="2a36a-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="2a36a-105">Event values</span></span>

<span data-ttu-id="2a36a-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="2a36a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2a36a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2a36a-107">VARTYPE</span></span>              | <span data-ttu-id="2a36a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a36a-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2a36a-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="2a36a-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2a36a-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="2a36a-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2a36a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a36a-111">Remarks</span></span>

<span data-ttu-id="2a36a-112">Un receptor de flujo puede producir esto incluso si ocurre algo que invalida el tipo de medio del receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2a36a-112">A stream sink can raise this even if something happens that invalidates the stream sink's media type.</span></span> <span data-ttu-id="2a36a-113">Por ejemplo, el representador de vídeo mejorado (EVR) envía este evento cuando cambia la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2a36a-113">For example, the enhanced video renderer (EVR) sends this event when the display changes.</span></span>

<span data-ttu-id="2a36a-114">El valor **HRESULT** recuperado por [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) podría indicar por qué el tipo de medio ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="2a36a-114">The **HRESULT** value retrieved by [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) might indicate why the media type is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a36a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a36a-115">Requirements</span></span>



| <span data-ttu-id="2a36a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a36a-116">Requirement</span></span> | <span data-ttu-id="2a36a-117">Value</span><span class="sxs-lookup"><span data-stu-id="2a36a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a36a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a36a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2a36a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a36a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a36a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a36a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2a36a-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a36a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a36a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a36a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a36a-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a36a-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a36a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a36a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a36a-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a36a-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="2a36a-126">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="2a36a-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




