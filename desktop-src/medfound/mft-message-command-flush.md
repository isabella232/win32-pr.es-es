---
description: Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811612"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="b46e9-103">\_ \_ vaciado de comandos de mensajes de MFT \_</span><span class="sxs-lookup"><span data-stu-id="b46e9-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="b46e9-104">Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="b46e9-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="b46e9-105">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="b46e9-105">Message Parameter</span></span>

<span data-ttu-id="b46e9-106">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b46e9-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b46e9-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b46e9-107">Remarks</span></span>

<span data-ttu-id="b46e9-108">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="b46e9-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="b46e9-109">Después de enviar este mensaje, el MFT puede aceptar nuevos ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="b46e9-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="b46e9-110">Los tipos de medios actuales no se invalidan.</span><span class="sxs-lookup"><span data-stu-id="b46e9-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="b46e9-111">Implementación</span><span class="sxs-lookup"><span data-stu-id="b46e9-111">Implementation</span></span>

<span data-ttu-id="b46e9-112">Todos los MFTs deben implementar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b46e9-112">All MFTs must implement this message.</span></span> <span data-ttu-id="b46e9-113">Cuando recibe este mensaje, la MFT debe descartar los ejemplos de medios que contiene.</span><span class="sxs-lookup"><span data-stu-id="b46e9-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="b46e9-114">[Asincrónico MFTs](asynchronous-mfts.md): el MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje de [**MFT \_ para \_ notificar el \_ Inicio \_ del \_**](mft-message-notify-start-of-stream.md) mensaje de secuencia desde el cliente.</span><span class="sxs-lookup"><span data-stu-id="b46e9-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="b46e9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b46e9-115">Requirements</span></span>



| <span data-ttu-id="b46e9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b46e9-116">Requirement</span></span> | <span data-ttu-id="b46e9-117">Value</span><span class="sxs-lookup"><span data-stu-id="b46e9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b46e9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b46e9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b46e9-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b46e9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b46e9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b46e9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b46e9-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b46e9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b46e9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b46e9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b46e9-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b46e9-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b46e9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b46e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b46e9-125">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="b46e9-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




