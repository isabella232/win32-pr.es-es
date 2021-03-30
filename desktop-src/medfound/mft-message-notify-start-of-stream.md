---
description: Notifica a una transformación de Media Foundation (MFT) que la primera muestra está a punto de procesarse.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082299"
---
# <a name="mft_message_notify_start_of_stream"></a><span data-ttu-id="0807c-103">el \_ mensaje \_ de MFT notifica el \_ Inicio \_ de la \_ secuencia</span><span class="sxs-lookup"><span data-stu-id="0807c-103">MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM</span></span>

<span data-ttu-id="0807c-104">Notifica a una transformación de Media Foundation (MFT) que la primera muestra está a punto de procesarse.</span><span class="sxs-lookup"><span data-stu-id="0807c-104">Notifies a Media Foundation transform (MFT) that the first sample is about to be processed.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="0807c-105">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="0807c-105">Message Parameter</span></span>

<span data-ttu-id="0807c-106">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0807c-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0807c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0807c-107">Remarks</span></span>

<span data-ttu-id="0807c-108">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="0807c-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="0807c-109">En el caso de MFTs sincrónicos, es opcional enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0807c-109">For synchronous MFTs, it is optional to send this message.</span></span>

<span data-ttu-id="0807c-110">En el caso de MFTs asincrónico, el cliente debe enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0807c-110">For asynchronous MFTs, the client must send this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="0807c-111">Implementación</span><span class="sxs-lookup"><span data-stu-id="0807c-111">Implementation</span></span>

<span data-ttu-id="0807c-112">No es necesario un MFT sincrónico para responder al mensaje.</span><span class="sxs-lookup"><span data-stu-id="0807c-112">A synchronous MFT is not required to respond to the message.</span></span>

<span data-ttu-id="0807c-113">Un MFT asincrónico debe implementar este mensaje, tal y como se describe en [MFTs asincrónico](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="0807c-113">An asynchronous MFT must implement this message, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0807c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0807c-114">Requirements</span></span>



| <span data-ttu-id="0807c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0807c-115">Requirement</span></span> | <span data-ttu-id="0807c-116">Value</span><span class="sxs-lookup"><span data-stu-id="0807c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0807c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0807c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0807c-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0807c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0807c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0807c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0807c-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0807c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0807c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0807c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0807c-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="0807c-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0807c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0807c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0807c-124">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="0807c-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




