---
description: Enviado por una transformación de Media Foundation asincrónica (MFT) cuando los datos de salida nuevos están disponibles desde la MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Evento METransformHaveOutput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677437"
---
# <a name="metransformhaveoutput-event"></a><span data-ttu-id="ade6f-103">Evento METransformHaveOutput</span><span class="sxs-lookup"><span data-stu-id="ade6f-103">METransformHaveOutput event</span></span>

<span data-ttu-id="ade6f-104">Enviado por una transformación de Media Foundation asincrónica (MFT) cuando los datos de salida nuevos están disponibles desde la MFT.</span><span class="sxs-lookup"><span data-stu-id="ade6f-104">Sent by an asynchronous Media Foundation transform (MFT) when new output data is available from the MFT.</span></span>

## <a name="event-values"></a><span data-ttu-id="ade6f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="ade6f-105">Event values</span></span>

<span data-ttu-id="ade6f-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="ade6f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ade6f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ade6f-107">VARTYPE</span></span>              | <span data-ttu-id="ade6f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ade6f-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="ade6f-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="ade6f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ade6f-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="ade6f-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="ade6f-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ade6f-111">Attributes</span></span>

<span data-ttu-id="ade6f-112">No hay atributos definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="ade6f-112">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade6f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ade6f-113">Remarks</span></span>

<span data-ttu-id="ade6f-114">Los MFTs asincrónicos envían este evento a través de la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="ade6f-114">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="ade6f-115">Los MFTs sincrónicos nunca envían este evento.</span><span class="sxs-lookup"><span data-stu-id="ade6f-115">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="ade6f-116">Cuando el cliente del MFT recibe este evento, debe llamar a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obtener la salida.</span><span class="sxs-lookup"><span data-stu-id="ade6f-116">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get the output.</span></span>

## <a name="requirements"></a><span data-ttu-id="ade6f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ade6f-117">Requirements</span></span>



| <span data-ttu-id="ade6f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade6f-118">Requirement</span></span> | <span data-ttu-id="ade6f-119">Value</span><span class="sxs-lookup"><span data-stu-id="ade6f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ade6f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ade6f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ade6f-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ade6f-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="ade6f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ade6f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ade6f-123">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ade6f-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="ade6f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ade6f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ade6f-125"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ade6f-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ade6f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ade6f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade6f-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ade6f-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ade6f-128">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="ade6f-128">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




