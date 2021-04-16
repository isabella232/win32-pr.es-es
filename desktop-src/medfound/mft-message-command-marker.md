---
description: Marca un punto en la secuencia. Este mensaje se aplica solo a MFTs asincrónicos.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715791"
---
# <a name="mft_message_command_marker"></a><span data-ttu-id="957cb-104">\_marcador de \_ comando de mensaje de MFT \_</span><span class="sxs-lookup"><span data-stu-id="957cb-104">MFT\_MESSAGE\_COMMAND\_MARKER</span></span>

<span data-ttu-id="957cb-105">Marca un punto en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="957cb-105">Marks a point in the stream.</span></span> <span data-ttu-id="957cb-106">Este mensaje se aplica solo a [MFTs asincrónicos](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="957cb-106">This message applies only to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="957cb-107">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="957cb-107">Message Parameter</span></span>

<span data-ttu-id="957cb-108">Un valor arbitrario.</span><span class="sxs-lookup"><span data-stu-id="957cb-108">An arbitrary value.</span></span> <span data-ttu-id="957cb-109">La MFT devuelve el valor al cliente en el evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="957cb-109">The MFT returns the value to the client in the [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="remarks"></a><span data-ttu-id="957cb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="957cb-110">Remarks</span></span>

<span data-ttu-id="957cb-111">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="957cb-111">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="957cb-112">La MFT responde a este mensaje a continuación:</span><span class="sxs-lookup"><span data-stu-id="957cb-112">The MFT responds to this messageas follows:</span></span>

1.  <span data-ttu-id="957cb-113">La MFT genera tantos ejemplos de salida como los datos de entrada existentes, y envía un evento [METransformHaveOutput](metransformhaveoutput.md) para cada ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="957cb-113">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="957cb-114">Una vez generada la salida, el MFT envía un evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="957cb-114">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="957cb-115">Este evento se debe enviar después de todos los eventos [METransformHaveOutput](metransformhaveoutput.md) .</span><span class="sxs-lookup"><span data-stu-id="957cb-115">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="957cb-116">No es necesario que el cliente envíe este mensaje y debe enviar este mensaje solo a MFTs asincrónicos.</span><span class="sxs-lookup"><span data-stu-id="957cb-116">The client is not required to send this message, and should send this message only to asynchronous MFTs.</span></span> <span data-ttu-id="957cb-117">Un MFT sincrónico no enviará un evento [METransformMarker](metransformmarker.md) en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="957cb-117">A synchronous MFT will not send an [METransformMarker](metransformmarker.md) event in response to this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="957cb-118">Implementación</span><span class="sxs-lookup"><span data-stu-id="957cb-118">Implementation</span></span>

<span data-ttu-id="957cb-119">Los MFTs asincrónicos deben responder a este mensaje tal y como se describe.</span><span class="sxs-lookup"><span data-stu-id="957cb-119">Asynchronous MFTs must respond to this message as described.</span></span> <span data-ttu-id="957cb-120">Los MFTs sincrónicos deben omitir este mensaje.</span><span class="sxs-lookup"><span data-stu-id="957cb-120">Synchronous MFTs should ignore this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="957cb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="957cb-121">Requirements</span></span>



| <span data-ttu-id="957cb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="957cb-122">Requirement</span></span> | <span data-ttu-id="957cb-123">Value</span><span class="sxs-lookup"><span data-stu-id="957cb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="957cb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="957cb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="957cb-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="957cb-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="957cb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="957cb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="957cb-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="957cb-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="957cb-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="957cb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="957cb-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="957cb-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="957cb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="957cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957cb-131">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="957cb-131">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




