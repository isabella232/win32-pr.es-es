---
description: 'MFT_MESSAGE_COMMAND_DRAIN: solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092753"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="db28e-103">PURGA DE COMANDOS \_ DE \_ MENSAJES DE \_ MFT</span><span class="sxs-lookup"><span data-stu-id="db28e-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="db28e-104">Solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="db28e-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="db28e-105">Parámetro message</span><span class="sxs-lookup"><span data-stu-id="db28e-105">Message Parameter</span></span>

<span data-ttu-id="db28e-106">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="db28e-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="db28e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db28e-107">Remarks</span></span>

<span data-ttu-id="db28e-108">Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="db28e-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="db28e-109">Después de enviar este mensaje, el flujo de entrada especificado no acepta la entrada hasta que MFT procesa todos los datos de las llamadas anteriores a [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="db28e-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="db28e-110">El proceso de purga varía ligeramente entre los MTA sincrónicos y los MTA asincrónicos:</span><span class="sxs-lookup"><span data-stu-id="db28e-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="db28e-111">**MFT sincrónicos**</span><span class="sxs-lookup"><span data-stu-id="db28e-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="db28e-112">Una vez que el cliente envía este mensaje, llama a [**MFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en un bucle, hasta que **ProcessOutput** devuelve el código de error **MF E TRANSFORM NEED MORE \_ \_ \_ \_ \_ INPUT**.</span><span class="sxs-lookup"><span data-stu-id="db28e-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="db28e-113">Siempre y cuando MFT todavía tenga datos que procesar, se producirá un error en las llamadas a [**ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)</span><span class="sxs-lookup"><span data-stu-id="db28e-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="db28e-114">MFT continúa generando resultados hasta que usa todos los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="db28e-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="db28e-115">El MFT descarta los datos que no se pueden procesar en un ejemplo de salida completo.</span><span class="sxs-lookup"><span data-stu-id="db28e-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="db28e-116">(Por ejemplo, debería quitar un fotograma de vídeo parcial).</span><span class="sxs-lookup"><span data-stu-id="db28e-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="db28e-117">**MFT asincrónicos**</span><span class="sxs-lookup"><span data-stu-id="db28e-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="db28e-118">El MFT continúa con el envío [de eventos METransformTransformTransformOutput](metransformhaveoutput.md) hasta que no tiene más datos para procesar.</span><span class="sxs-lookup"><span data-stu-id="db28e-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="db28e-119">No envía eventos [METransformNeedInput](metransformneedinput.md) durante este tiempo.</span><span class="sxs-lookup"><span data-stu-id="db28e-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="db28e-120">Una vez que MFT envía el último [evento METransformTransformTransformOutput,](metransformhaveoutput.md) envía un [evento METransformDrainComplete.](metransformdraincomplete.md)</span><span class="sxs-lookup"><span data-stu-id="db28e-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="db28e-121">Una vez completada la purga, MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje [**MFT \_ MESSAGE NOTIFY START \_ OF \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) del cliente.</span><span class="sxs-lookup"><span data-stu-id="db28e-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="db28e-122">Una vez que el cliente ha purgado el MFT, el cliente puede enviar más datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="db28e-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="db28e-123">El primer ejemplo después de la operación de purga debe tener el atributo de discontinuidad [**(atributo MFSampleExtension \_ Discontinuity).**](mfsampleextension-discontinuity-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="db28e-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="db28e-124">En versiones anteriores de esta documentación se indicaba que el parámetro de evento *ulParam* es miembro de la [**\_ enumeración \_ MFT DRAIN \_ TYPE.**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type)</span><span class="sxs-lookup"><span data-stu-id="db28e-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="db28e-125">No es correcto.</span><span class="sxs-lookup"><span data-stu-id="db28e-125">That is not correct.</span></span> <span data-ttu-id="db28e-126">*UlParam contiene* un identificador de secuencia.</span><span class="sxs-lookup"><span data-stu-id="db28e-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="db28e-127">Implementación</span><span class="sxs-lookup"><span data-stu-id="db28e-127">Implementation</span></span>

<span data-ttu-id="db28e-128">Un MFT asincrónico siempre debe devolver [METransformDrainComplete después](metransformdraincomplete.md) de que se haya purgado.</span><span class="sxs-lookup"><span data-stu-id="db28e-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="db28e-129">Un MFT sincrónico puede omitir este mensaje y devolver S \_ OK si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="db28e-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="db28e-130">MFT nunca almacena más de un ejemplo de entrada a la vez.</span><span class="sxs-lookup"><span data-stu-id="db28e-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="db28e-131">Cada ejemplo de entrada genera un único ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="db28e-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="db28e-132">De lo contrario, un MFT sincrónico debe implementar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="db28e-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="db28e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db28e-133">Requirements</span></span>



| <span data-ttu-id="db28e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="db28e-134">Requirement</span></span> | <span data-ttu-id="db28e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="db28e-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db28e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db28e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="db28e-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db28e-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="db28e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db28e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="db28e-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="db28e-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db28e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db28e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="db28e-141"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="db28e-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db28e-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="db28e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db28e-143">**TIPO DE MENSAJE \_ \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="db28e-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="db28e-144">MFT asincrónicas</span><span class="sxs-lookup"><span data-stu-id="db28e-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




