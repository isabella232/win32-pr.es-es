---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) para solicitar un nuevo ejemplo de entrada.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154652"
---
# <a name="metransformneedinput-event"></a><span data-ttu-id="469e6-103">Evento METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="469e6-103">METransformNeedInput event</span></span>

<span data-ttu-id="469e6-104">Enviado por una transformación de Media Foundation asincrónica (MFT) para solicitar un nuevo ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="469e6-104">Sent by an asynchronous Media Foundation transform (MFT) to request a new input sample.</span></span>

## <a name="event-values"></a><span data-ttu-id="469e6-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="469e6-105">Event values</span></span>

<span data-ttu-id="469e6-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="469e6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="469e6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="469e6-107">VARTYPE</span></span>              | <span data-ttu-id="469e6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="469e6-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="469e6-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="469e6-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="469e6-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="469e6-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="469e6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="469e6-111">Attributes</span></span>

<span data-ttu-id="469e6-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="469e6-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="469e6-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="469e6-113">Attribute</span></span>                                                                        | <span data-ttu-id="469e6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="469e6-114">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="469e6-115">\_identificador de \_ flujo de entrada de MFT de evento MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="469e6-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="469e6-116">Identificador de la secuencia que necesita datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="469e6-116">The identifier of the stream that needs input data.</span></span><br/><span data-ttu-id="469e6-117">*Desee*</span><span class="sxs-lookup"><span data-stu-id="469e6-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="469e6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="469e6-118">Remarks</span></span>

<span data-ttu-id="469e6-119">Los MFTs asincrónicos envían este evento a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="469e6-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="469e6-120">Los MFTs sincrónicos nunca envían este evento.</span><span class="sxs-lookup"><span data-stu-id="469e6-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="469e6-121">Cuando el cliente del MFT recibe este evento, debe llamar a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para ofrecer el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="469e6-121">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) to deliver the next sample.</span></span> <span data-ttu-id="469e6-122">El atributo de [identificador de flujo de entrada de \_ MFT del evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) del objeto de evento especifica qué flujo de entrada requiere datos.</span><span class="sxs-lookup"><span data-stu-id="469e6-122">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event object specifies which input stream requires data.</span></span>

## <a name="requirements"></a><span data-ttu-id="469e6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="469e6-123">Requirements</span></span>



| <span data-ttu-id="469e6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="469e6-124">Requirement</span></span> | <span data-ttu-id="469e6-125">Value</span><span class="sxs-lookup"><span data-stu-id="469e6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="469e6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="469e6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="469e6-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="469e6-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="469e6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="469e6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="469e6-129">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="469e6-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="469e6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="469e6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="469e6-131"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="469e6-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="469e6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="469e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469e6-133">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="469e6-133">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="469e6-134">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="469e6-134">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




