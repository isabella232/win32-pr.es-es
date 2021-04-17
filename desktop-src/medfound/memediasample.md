---
description: 'Se envía cuando una transmisión por secuencias multimedia entrega un nuevo ejemplo en respuesta a una llamada a IMFMediaStream:: RequestSample.'
ms.assetid: 01610053-786f-44b5-90d6-2cb2668cd632
title: Evento MEMediaSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de0cfcdbf943e0526d61a0c63424f7add078b2c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717361"
---
# <a name="memediasample-event"></a><span data-ttu-id="f0606-103">Evento MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="f0606-103">MEMediaSample event</span></span>

<span data-ttu-id="f0606-104">Se envía cuando una transmisión por secuencias multimedia entrega un nuevo ejemplo en respuesta a una llamada a [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span><span class="sxs-lookup"><span data-stu-id="f0606-104">Sent when a media stream delivers a new sample in response to a call to [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span>

## <a name="event-values"></a><span data-ttu-id="f0606-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f0606-105">Event values</span></span>

<span data-ttu-id="f0606-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f0606-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f0606-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f0606-107">VARTYPE</span></span>                | <span data-ttu-id="f0606-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0606-108">Description</span></span>                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0606-109">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="f0606-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="f0606-110">Puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f0606-110">Pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of the sample.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f0606-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0606-111">Requirements</span></span>



| <span data-ttu-id="f0606-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0606-112">Requirement</span></span> | <span data-ttu-id="f0606-113">Value</span><span class="sxs-lookup"><span data-stu-id="f0606-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0606-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0606-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f0606-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0606-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0606-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0606-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f0606-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0606-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0606-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0606-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0606-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0606-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0606-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0606-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0606-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f0606-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f0606-122">Orígenes multimedia</span><span class="sxs-lookup"><span data-stu-id="f0606-122">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 




