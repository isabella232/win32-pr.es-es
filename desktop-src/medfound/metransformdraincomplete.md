---
description: Lo envía una transformación de Media Foundation asincrónica (MFT) cuando se completa una operación de purga.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361348"
---
# <a name="metransformdraincomplete-event"></a><span data-ttu-id="08b0a-103">Evento METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="08b0a-103">METransformDrainComplete event</span></span>

<span data-ttu-id="08b0a-104">Lo envía una transformación de Media Foundation asincrónica (MFT) cuando se completa una operación de purga.</span><span class="sxs-lookup"><span data-stu-id="08b0a-104">Sent by an asynchronous Media Foundation transform (MFT) when a drain operation is complete.</span></span>

## <a name="event-values"></a><span data-ttu-id="08b0a-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="08b0a-105">Event values</span></span>

<span data-ttu-id="08b0a-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="08b0a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="08b0a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="08b0a-107">VARTYPE</span></span>              | <span data-ttu-id="08b0a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="08b0a-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="08b0a-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="08b0a-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="08b0a-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="08b0a-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="08b0a-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="08b0a-111">Attributes</span></span>

<span data-ttu-id="08b0a-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="08b0a-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="08b0a-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="08b0a-113">Attribute</span></span>                                                                        | <span data-ttu-id="08b0a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="08b0a-114">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="08b0a-115">\_identificador de \_ flujo de entrada de MFT de evento MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="08b0a-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="08b0a-116">Identificador de la secuencia que se ha purgado.</span><span class="sxs-lookup"><span data-stu-id="08b0a-116">The identifier of the stream that was drained.</span></span><br/><span data-ttu-id="08b0a-117">*Desee*</span><span class="sxs-lookup"><span data-stu-id="08b0a-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="08b0a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08b0a-118">Remarks</span></span>

<span data-ttu-id="08b0a-119">Los MFTs asincrónicos envían este evento a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="08b0a-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="08b0a-120">Los MFTs sincrónicos nunca envían este evento.</span><span class="sxs-lookup"><span data-stu-id="08b0a-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="08b0a-121">Para purgar un MFT, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) con el mensaje de **agotamiento del comando de mensaje de MFT \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="08b0a-121">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_DRAIN** message.</span></span> <span data-ttu-id="08b0a-122">Especifique el flujo de entrada que se va a purgar en el parámetro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="08b0a-122">Specify the input stream to drain in the *ulParam* parameter.</span></span> <span data-ttu-id="08b0a-123">Cuando se completa la operación de purga, un MFT asincrónico envía el evento METransformDrainComplete.</span><span class="sxs-lookup"><span data-stu-id="08b0a-123">When the drain operation is completed, an asynchronous MFT sends the METransformDrainComplete event.</span></span> <span data-ttu-id="08b0a-124">El atributo de [identificador de flujo de entrada de \_ MFT del evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) del evento contiene el identificador de flujo proporcionado en el parámetro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="08b0a-124">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event contains the stream identifier given in the *ulParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="08b0a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08b0a-125">Requirements</span></span>



| <span data-ttu-id="08b0a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b0a-126">Requirement</span></span> | <span data-ttu-id="08b0a-127">Value</span><span class="sxs-lookup"><span data-stu-id="08b0a-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b0a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08b0a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="08b0a-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="08b0a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="08b0a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08b0a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="08b0a-131">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="08b0a-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="08b0a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08b0a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="08b0a-133"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08b0a-133"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b0a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="08b0a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b0a-135">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08b0a-135">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="08b0a-136">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="08b0a-136">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




