---
description: Lo genera un origen multimedia cuando se reinicia o busca una secuencia que ya está activa.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Evento MEUpdatedStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546163"
---
# <a name="meupdatedstream-event"></a><span data-ttu-id="1450a-103">Evento MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="1450a-103">MEUpdatedStream event</span></span>

<span data-ttu-id="1450a-104">Lo genera un origen multimedia cuando se reinicia o busca una secuencia que ya está activa.</span><span class="sxs-lookup"><span data-stu-id="1450a-104">Raised by a media source when it restarts or seeks a stream that is already active.</span></span>

<span data-ttu-id="1450a-105">Cuando se llama al método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en un origen multimedia, el origen multimedia envía un evento para cada flujo seleccionado:</span><span class="sxs-lookup"><span data-stu-id="1450a-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="1450a-106">El origen envía el evento [MENewStream](menewstream.md) si la secuencia no se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), o esta es la primera llamada a **Start** en este origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="1450a-106">The source sends the [MENewStream](menewstream.md) event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="1450a-107">El origen envía el evento MEUpdatedStream si la secuencia ya se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="1450a-107">The source sends the MEUpdatedStream event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="1450a-108">No se envía ningún evento para flujos no seleccionados.</span><span class="sxs-lookup"><span data-stu-id="1450a-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="1450a-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="1450a-109">Event values</span></span>

<span data-ttu-id="1450a-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="1450a-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="1450a-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1450a-111">VARTYPE</span></span>                | <span data-ttu-id="1450a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1450a-112">Description</span></span>                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1450a-113">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="1450a-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="1450a-114">Puntero a la interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1450a-114">Pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="1450a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1450a-115">Remarks</span></span>

<span data-ttu-id="1450a-116">En la primera llamada a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en la que se activa una secuencia, el origen multimedia envía un evento [MENewStream](menewstream.md) para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1450a-116">On the first call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) in which a stream becomes active, the media source sends an [MENewStream](menewstream.md) event for the stream.</span></span> <span data-ttu-id="1450a-117">En las llamadas posteriores a **Start**, el origen multimedia envía un evento MEUpdatedStream, hasta que se anule la selección de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1450a-117">On subsequent calls to **Start**, the media source sends an MEUpdatedStream event, until the stream is deselected.</span></span>

## <a name="requirements"></a><span data-ttu-id="1450a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1450a-118">Requirements</span></span>



| <span data-ttu-id="1450a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1450a-119">Requirement</span></span> | <span data-ttu-id="1450a-120">Value</span><span class="sxs-lookup"><span data-stu-id="1450a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1450a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1450a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1450a-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1450a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1450a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1450a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1450a-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1450a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1450a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1450a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1450a-126"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1450a-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1450a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1450a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1450a-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1450a-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




