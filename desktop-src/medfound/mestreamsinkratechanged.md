---
description: Generado por un receptor de flujo cuando la tasa ha cambiado.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Evento MEStreamSinkRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716507"
---
# <a name="mestreamsinkratechanged-event"></a><span data-ttu-id="a14cf-103">Evento MEStreamSinkRateChanged</span><span class="sxs-lookup"><span data-stu-id="a14cf-103">MEStreamSinkRateChanged event</span></span>

<span data-ttu-id="a14cf-104">Generado por un receptor de flujo cuando la tasa ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a14cf-104">Raised by a stream sink when the rate has changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="a14cf-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a14cf-105">Event values</span></span>

<span data-ttu-id="a14cf-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a14cf-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a14cf-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a14cf-107">VARTYPE</span></span>              | <span data-ttu-id="a14cf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a14cf-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a14cf-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="a14cf-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a14cf-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="a14cf-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a14cf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a14cf-111">Remarks</span></span>

<span data-ttu-id="a14cf-112">Si un receptor de flujo admite cambios de velocidad, envía este evento una vez completado el cambio de tasa.</span><span class="sxs-lookup"><span data-stu-id="a14cf-112">If a stream sink supports rate changes, it sends this event after the rate change is complete.</span></span> <span data-ttu-id="a14cf-113">El evento se envía una vez por cada llamada al método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) del receptor.</span><span class="sxs-lookup"><span data-stu-id="a14cf-113">The event is sent once for each call to the sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span> <span data-ttu-id="a14cf-114">Si el cambio de frecuencia no se realiza correctamente, el valor de estado del evento es un código de error.</span><span class="sxs-lookup"><span data-stu-id="a14cf-114">If the rate change is not successful, the event status value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a14cf-115">Requirements</span></span>



| <span data-ttu-id="a14cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a14cf-116">Requirement</span></span> | <span data-ttu-id="a14cf-117">Value</span><span class="sxs-lookup"><span data-stu-id="a14cf-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a14cf-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a14cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a14cf-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a14cf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a14cf-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a14cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a14cf-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a14cf-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a14cf-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a14cf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a14cf-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a14cf-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a14cf-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a14cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a14cf-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a14cf-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="a14cf-126">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="a14cf-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




