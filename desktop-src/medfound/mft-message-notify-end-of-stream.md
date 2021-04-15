---
description: Notifica a una transformación de Media Foundation (MFT) que un flujo de entrada ha finalizado.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715790"
---
# <a name="mft_message_notify_end_of_stream"></a><span data-ttu-id="522b3-103">\_ \_ \_ final \_ de notificación de mensaje de \_ MFT</span><span class="sxs-lookup"><span data-stu-id="522b3-103">MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM</span></span>

<span data-ttu-id="522b3-104">Notifica a una transformación de Media Foundation (MFT) que un flujo de entrada ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="522b3-104">Notifies a Media Foundation transform (MFT) that an input stream has ended.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="522b3-105">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="522b3-105">Message Parameter</span></span>

<span data-ttu-id="522b3-106">El parámetro *ulParam* contiene el identificador del flujo de entrada, especificado como un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="522b3-106">The *ulParam* parameter contains the identifier of the input stream, specified as a **DWORD** value.</span></span> <span data-ttu-id="522b3-107">En las aplicaciones de 64 bits, coloque este valor en los 32 bits inferiores de **ULong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="522b3-107">In 64-bit applications, place this value in the lower 32-bits of the **ULONG\_PTR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="522b3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="522b3-108">Remarks</span></span>

<span data-ttu-id="522b3-109">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="522b3-109">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="522b3-110">No es necesario que el cliente envíe este mensaje.</span><span class="sxs-lookup"><span data-stu-id="522b3-110">The client is not required to send this message.</span></span>

<span data-ttu-id="522b3-111">Una vez finalizada una secuencia, el cliente puede volver a llamar a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para enviar datos nuevos para esa secuencia.</span><span class="sxs-lookup"><span data-stu-id="522b3-111">After a stream ends, the client may call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) again to send new data for that stream.</span></span> <span data-ttu-id="522b3-112">En ese caso, el cliente debe establecer el atributo discontinuidad (atributo discontinuidad [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) ) en el primer ejemplo de entrada después de que finalice la secuencia.</span><span class="sxs-lookup"><span data-stu-id="522b3-112">If so, the client must set the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute) on the first input sample after the stream ends.</span></span> <span data-ttu-id="522b3-113">(El cliente siempre debe establecer este atributo en el primer ejemplo nuevo una vez finalizada una secuencia, independientemente de si el cliente envió el **\_ mensaje \_ de MFT notifica el \_ final del mensaje de la \_ \_ secuencia** .</span><span class="sxs-lookup"><span data-stu-id="522b3-113">(The client should always set this attribute on the first new sample after a stream ends, regardless of whether the client sent the **MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM** message.</span></span> <span data-ttu-id="522b3-114">Para obtener más información sobre cómo controlar las discontinuidades, vea [modelo de procesamiento de MFT básico](basic-mft-processing-model.md)).</span><span class="sxs-lookup"><span data-stu-id="522b3-114">For more information about handling discontinuities, see [Basic MFT Processing Model](basic-mft-processing-model.md).)</span></span>

<span data-ttu-id="522b3-115">Después de enviar este mensaje para cada flujo de entrada, el cliente normalmente envía un comando de purga de comando de mensaje de MFT y, a continuación, recopila el resultado restante. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="522b3-115">After sending this message for every input stream, the client typically sends an **MFT\_MESSAGE\_COMMAND\_DRAIN** command and then collects the remaining output.</span></span> <span data-ttu-id="522b3-116">Sin embargo, no es necesario que el cliente vacíe la MFT.</span><span class="sxs-lookup"><span data-stu-id="522b3-116">However, the client is not required to drain the MFT.</span></span> <span data-ttu-id="522b3-117">Si el cliente no purga la MFT, normalmente descartará todos los datos sin procesar en la siguiente llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), cuando detecte la discontinuidad de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="522b3-117">If the client does not drain the MFT, the MFT will typically discard any unprocessed data on the next call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), when it detects the stream discontinuity.</span></span> <span data-ttu-id="522b3-118">Como alternativa, el cliente puede vaciar el MFT antes de llamar a **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="522b3-118">Alternatively, the client might flush the MFT before calling **ProcessInput**.</span></span>

<span data-ttu-id="522b3-119">Este mensaje no quita el flujo de entrada ni restablece el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="522b3-119">This message does not remove the input stream or reset the media type.</span></span>

### <a name="implementation"></a><span data-ttu-id="522b3-120">Implementación</span><span class="sxs-lookup"><span data-stu-id="522b3-120">Implementation</span></span>

<span data-ttu-id="522b3-121">No se requiere una MFT para responder a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="522b3-121">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="522b3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="522b3-122">Requirements</span></span>



| <span data-ttu-id="522b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="522b3-123">Requirement</span></span> | <span data-ttu-id="522b3-124">Value</span><span class="sxs-lookup"><span data-stu-id="522b3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="522b3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="522b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="522b3-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="522b3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="522b3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="522b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="522b3-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="522b3-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="522b3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="522b3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="522b3-130"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="522b3-130"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522b3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="522b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522b3-132">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="522b3-132">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




