---
description: Lo genera un origen multimedia cuando inicia una nueva secuencia.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Evento MENewStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696768"
---
# <a name="menewstream-event"></a><span data-ttu-id="67cf7-103">Evento MENewStream</span><span class="sxs-lookup"><span data-stu-id="67cf7-103">MENewStream event</span></span>

<span data-ttu-id="67cf7-104">Lo genera un origen multimedia cuando inicia una nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="67cf7-104">Raised by a media source when it starts a new stream.</span></span>

<span data-ttu-id="67cf7-105">Cuando se llama al método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) en un origen multimedia, el origen multimedia envía un evento para cada flujo seleccionado:</span><span class="sxs-lookup"><span data-stu-id="67cf7-105">When the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called on a media source, the media source sends one event for each selected stream:</span></span>

-   <span data-ttu-id="67cf7-106">El origen envía el evento MENewStream si la secuencia no se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), o esta es la primera llamada a **Start** en este origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="67cf7-106">The source sends the MENewStream event if the stream was not selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), or this is the very first call to **Start** on this media source.</span></span>

-   <span data-ttu-id="67cf7-107">El origen envía el evento [MEUpdatedStream](meupdatedstream.md) si la secuencia ya se seleccionó en la llamada anterior a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="67cf7-107">The source sends the [MEUpdatedStream](meupdatedstream.md) event if the stream was already selected in the previous call to [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>

<span data-ttu-id="67cf7-108">No se envía ningún evento para flujos no seleccionados.</span><span class="sxs-lookup"><span data-stu-id="67cf7-108">No events are sent for unselected streams.</span></span>

## <a name="event-values"></a><span data-ttu-id="67cf7-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="67cf7-109">Event values</span></span>

<span data-ttu-id="67cf7-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="67cf7-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="67cf7-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="67cf7-111">VARTYPE</span></span>                | <span data-ttu-id="67cf7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="67cf7-112">Description</span></span>                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67cf7-113">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="67cf7-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="67cf7-114">Contiene un puntero a la interfaz [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="67cf7-114">Contains a pointer to the stream's [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="67cf7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67cf7-115">Requirements</span></span>



| <span data-ttu-id="67cf7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67cf7-116">Requirement</span></span> | <span data-ttu-id="67cf7-117">Value</span><span class="sxs-lookup"><span data-stu-id="67cf7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67cf7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67cf7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67cf7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="67cf7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="67cf7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67cf7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67cf7-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="67cf7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67cf7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67cf7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67cf7-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67cf7-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67cf7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="67cf7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cf7-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67cf7-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




