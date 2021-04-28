---
description: 'MFT_MESSAGE_COMMAND_FLUSH: solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.'
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092743"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="47c94-103">COMANDO DE MENSAJE DE MFT \_ \_ \_ FLUSH</span><span class="sxs-lookup"><span data-stu-id="47c94-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="47c94-104">Solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="47c94-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="47c94-105">Parámetro message</span><span class="sxs-lookup"><span data-stu-id="47c94-105">Message Parameter</span></span>

<span data-ttu-id="47c94-106">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="47c94-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c94-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="47c94-107">Remarks</span></span>

<span data-ttu-id="47c94-108">Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="47c94-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="47c94-109">Después de enviar este mensaje, MFT puede aceptar nuevos ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="47c94-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="47c94-110">Los tipos de medios actuales no se invalidan.</span><span class="sxs-lookup"><span data-stu-id="47c94-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="47c94-111">Implementación</span><span class="sxs-lookup"><span data-stu-id="47c94-111">Implementation</span></span>

<span data-ttu-id="47c94-112">Todas las MTA deben implementar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="47c94-112">All MFTs must implement this message.</span></span> <span data-ttu-id="47c94-113">Cuando recibe este mensaje, el MFT debe descartar las muestras de medios que esté manteniendo.</span><span class="sxs-lookup"><span data-stu-id="47c94-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="47c94-114">[MFT asincrónico:](asynchronous-mfts.md)MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) del cliente.</span><span class="sxs-lookup"><span data-stu-id="47c94-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c94-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c94-115">Requirements</span></span>



| <span data-ttu-id="47c94-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c94-116">Requirement</span></span> | <span data-ttu-id="47c94-117">Valor</span><span class="sxs-lookup"><span data-stu-id="47c94-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c94-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47c94-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47c94-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="47c94-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47c94-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47c94-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47c94-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="47c94-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="47c94-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47c94-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="47c94-123"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="47c94-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47c94-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47c94-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c94-125">**TIPO DE \_ MENSAJE \_ MFT**</span><span class="sxs-lookup"><span data-stu-id="47c94-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




