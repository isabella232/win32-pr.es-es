---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) en respuesta a un \_ mensaje de marcador de comando de mensaje MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677593"
---
# <a name="metransformmarker-event"></a><span data-ttu-id="72058-103">Evento METransformMarker</span><span class="sxs-lookup"><span data-stu-id="72058-103">METransformMarker event</span></span>

<span data-ttu-id="72058-104">Enviado por una transformación de Media Foundation asincrónica (MFT) en respuesta a un mensaje de **\_ marcador de \_ comando \_ de mensaje MFT** .</span><span class="sxs-lookup"><span data-stu-id="72058-104">Sent by an asynchronous Media Foundation transform (MFT) in response to an **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span>

## <a name="event-values"></a><span data-ttu-id="72058-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="72058-105">Event values</span></span>

<span data-ttu-id="72058-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="72058-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="72058-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="72058-107">VARTYPE</span></span>              | <span data-ttu-id="72058-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="72058-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="72058-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="72058-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="72058-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="72058-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="72058-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="72058-111">Attributes</span></span>

<span data-ttu-id="72058-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="72058-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="72058-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="72058-113">Attribute</span></span>                                                      | <span data-ttu-id="72058-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="72058-114">Description</span></span>                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72058-115">\_ \_ contexto MFT del evento MF \_</span><span class="sxs-lookup"><span data-stu-id="72058-115">MF\_EVENT\_MFT\_CONTEXT</span></span>](mf-event-mft-context.md)<br/> | <span data-ttu-id="72058-116">El valor del parámetro *ulParam* del mensaje del **\_ marcador de \_ comando \_ del mensaje de MFT** .</span><span class="sxs-lookup"><span data-stu-id="72058-116">The value of the *ulParam* parameter from the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span><br/><span data-ttu-id="72058-117">*Desee*</span><span class="sxs-lookup"><span data-stu-id="72058-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="72058-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72058-118">Remarks</span></span>

<span data-ttu-id="72058-119">Los MFTs asincrónicos envían este evento a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="72058-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="72058-120">Los MFTs sincrónicos nunca envían este evento.</span><span class="sxs-lookup"><span data-stu-id="72058-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="72058-121">El cliente de un MFT asincrónico puede colocar un marcador en la secuencia mediante una llamada a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje del marcador de comando del mensaje de **MFT \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="72058-121">The client of an asynchronous MFT can place a marker in the stream by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span> <span data-ttu-id="72058-122">El parámetro *ulParam* contiene datos definidos por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72058-122">The *ulParam* parameter contains application-defined data.</span></span>

<span data-ttu-id="72058-123">Cuando el MFT finaliza el procesamiento de todos los datos de entrada que estaban disponibles en el momento de la llamada a [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , el MFT pone en cola un evento METransformMarker.</span><span class="sxs-lookup"><span data-stu-id="72058-123">When the MFT finishes processing all of the input data that was available at the time of the [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) call, the MFT queues an METransformMarker event.</span></span> <span data-ttu-id="72058-124">El atributo de [ \_ \_ \_ contexto MFT del evento MF](mf-event-mft-context.md) del evento contiene el valor del parámetro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="72058-124">The [MF\_EVENT\_MFT\_CONTEXT](mf-event-mft-context.md) attribute of the event contains the value of the *ulParam* parameter.</span></span> <span data-ttu-id="72058-125">Para obtener más información, consulte [MFTs asincrónico](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="72058-125">For more information, see [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72058-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72058-126">Requirements</span></span>



| <span data-ttu-id="72058-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="72058-127">Requirement</span></span> | <span data-ttu-id="72058-128">Value</span><span class="sxs-lookup"><span data-stu-id="72058-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72058-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72058-129">Minimum supported client</span></span><br/> | <span data-ttu-id="72058-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="72058-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="72058-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72058-131">Minimum supported server</span></span><br/> | <span data-ttu-id="72058-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="72058-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="72058-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72058-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="72058-134"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72058-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72058-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="72058-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72058-136">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72058-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="72058-137">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="72058-137">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




