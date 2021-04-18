---
description: Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa533cfddfda53fd8eb0ee512b0535aaf9ad8f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666871"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="91d5b-103">\_consumo de \_ comandos de mensajes de MFT \_</span><span class="sxs-lookup"><span data-stu-id="91d5b-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="91d5b-104">Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="91d5b-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="91d5b-105">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="91d5b-105">Message Parameter</span></span>

<span data-ttu-id="91d5b-106">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="91d5b-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d5b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91d5b-107">Remarks</span></span>

<span data-ttu-id="91d5b-108">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="91d5b-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="91d5b-109">Después de enviar este mensaje, el flujo de entrada especificado no acepta la entrada hasta que el MFT procesa todos los datos de llamadas anteriores a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="91d5b-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="91d5b-110">El proceso de purga varía ligeramente entre MFTs sincrónicos y MFTs asincrónicos:</span><span class="sxs-lookup"><span data-stu-id="91d5b-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="91d5b-111">**MFTs sincrónicos**</span><span class="sxs-lookup"><span data-stu-id="91d5b-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="91d5b-112">Una vez que el cliente envía este mensaje, llama a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en un bucle, hasta que **ProcessOutput** devuelve el código de error de la **\_ transformación MF E \_ \_ necesita \_ más \_ entrada**.</span><span class="sxs-lookup"><span data-stu-id="91d5b-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="91d5b-113">Siempre que la MFT siga teniendo datos para procesar, se producirá un error en otras llamadas a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) .</span><span class="sxs-lookup"><span data-stu-id="91d5b-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="91d5b-114">La MFT continúa generando resultados hasta que utiliza todos los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="91d5b-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="91d5b-115">La MFT descarta todos los datos que no se pueden procesar en un ejemplo de salida completo.</span><span class="sxs-lookup"><span data-stu-id="91d5b-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="91d5b-116">(Por ejemplo, debe quitar un fotograma de vídeo parcial).</span><span class="sxs-lookup"><span data-stu-id="91d5b-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="91d5b-117">**MFTs asincrónico**</span><span class="sxs-lookup"><span data-stu-id="91d5b-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="91d5b-118">La MFT sigue enviando eventos [METransformHaveOutput](metransformhaveoutput.md) hasta que no tiene más datos para procesar.</span><span class="sxs-lookup"><span data-stu-id="91d5b-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="91d5b-119">No envía eventos [METransformNeedInput](metransformneedinput.md) durante este tiempo.</span><span class="sxs-lookup"><span data-stu-id="91d5b-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="91d5b-120">Después de que el MFT envíe el último evento [METransformHaveOutput](metransformhaveoutput.md) , envía un evento [METransformDrainComplete](metransformdraincomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="91d5b-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="91d5b-121">Una vez completada la purga, el MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que reciba un [**mensaje de MFT para \_ \_ notificar el \_ Inicio \_ del \_**](mft-message-notify-start-of-stream.md) mensaje de secuencia desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="91d5b-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="91d5b-122">Una vez que el cliente ha purgado la MFT, el cliente puede enviar más datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="91d5b-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="91d5b-123">El primer ejemplo después de la operación de purga debe tener el atributo discontinuidad (atributo discontinuidad [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="91d5b-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="91d5b-124">En las versiones anteriores de esta documentación se indicó que el parámetro de evento *ulParam* es un miembro de la enumeración de [**\_ \_ \_ tipo Drain de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) .</span><span class="sxs-lookup"><span data-stu-id="91d5b-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="91d5b-125">No es correcto.</span><span class="sxs-lookup"><span data-stu-id="91d5b-125">That is not correct.</span></span> <span data-ttu-id="91d5b-126">*UlParam* contiene un identificador de flujo.</span><span class="sxs-lookup"><span data-stu-id="91d5b-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="91d5b-127">Implementación</span><span class="sxs-lookup"><span data-stu-id="91d5b-127">Implementation</span></span>

<span data-ttu-id="91d5b-128">Una MFT asincrónica siempre debe devolver [METransformDrainComplete](metransformdraincomplete.md) una vez que se ha purgado.</span><span class="sxs-lookup"><span data-stu-id="91d5b-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="91d5b-129">Los MFT sincrónicos pueden pasar por alto este mensaje y devolver S \_ correcto si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="91d5b-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="91d5b-130">La MFT nunca almacena más de una muestra de entrada a la vez.</span><span class="sxs-lookup"><span data-stu-id="91d5b-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="91d5b-131">Cada ejemplo de entrada genera un único ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="91d5b-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="91d5b-132">De lo contrario, un MFT sincrónico debe implementar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="91d5b-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d5b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91d5b-133">Requirements</span></span>



| <span data-ttu-id="91d5b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d5b-134">Requirement</span></span> | <span data-ttu-id="91d5b-135">Value</span><span class="sxs-lookup"><span data-stu-id="91d5b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d5b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91d5b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="91d5b-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="91d5b-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="91d5b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91d5b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="91d5b-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="91d5b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="91d5b-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91d5b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d5b-141"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d5b-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d5b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="91d5b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d5b-143">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="91d5b-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="91d5b-144">MFTs asincrónico</span><span class="sxs-lookup"><span data-stu-id="91d5b-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




