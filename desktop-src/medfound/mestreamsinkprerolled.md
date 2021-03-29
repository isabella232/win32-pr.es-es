---
description: Generado por un receptor de flujo cuando la secuencia ha recibido suficientes datos previos para comenzar la representación. Este evento es desencadenado por receptores de medios que admiten la interfaz IMFMediaSinkPreroll.
ms.assetid: 1ecb1805-73ce-4741-b969-6eb88982ee26
title: Evento MEStreamSinkPrerolled (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312daa90c995ccbbe8667cfa5acdf47975248474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811869"
---
# <a name="mestreamsinkprerolled-event"></a><span data-ttu-id="72b16-104">Evento MEStreamSinkPrerolled</span><span class="sxs-lookup"><span data-stu-id="72b16-104">MEStreamSinkPrerolled event</span></span>

<span data-ttu-id="72b16-105">Generado por un receptor de flujo cuando la secuencia ha recibido suficientes datos previos para comenzar la representación.</span><span class="sxs-lookup"><span data-stu-id="72b16-105">Raised by a stream sink when the stream has received enough pre-roll data to begin rendering.</span></span> <span data-ttu-id="72b16-106">Este evento es desencadenado por receptores de medios que admiten la interfaz [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="72b16-106">This event is raised by media sinks that support the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="72b16-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="72b16-107">Event values</span></span>

<span data-ttu-id="72b16-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="72b16-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="72b16-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="72b16-109">VARTYPE</span></span>              | <span data-ttu-id="72b16-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="72b16-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="72b16-111">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="72b16-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="72b16-112">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="72b16-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="72b16-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b16-113">Requirements</span></span>



| <span data-ttu-id="72b16-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b16-114">Requirement</span></span> | <span data-ttu-id="72b16-115">Value</span><span class="sxs-lookup"><span data-stu-id="72b16-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b16-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72b16-116">Minimum supported client</span></span><br/> | <span data-ttu-id="72b16-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="72b16-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="72b16-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72b16-118">Minimum supported server</span></span><br/> | <span data-ttu-id="72b16-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="72b16-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="72b16-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72b16-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b16-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72b16-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b16-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="72b16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b16-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72b16-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="72b16-124">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="72b16-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




