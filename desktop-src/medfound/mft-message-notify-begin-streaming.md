---
description: Notifica a una transformación de Media Foundation (MFT) que la transmisión por secuencias está a punto de comenzar.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275841"
---
# <a name="mft_message_notify_begin_streaming"></a><span data-ttu-id="44d89-103">la \_ notificación del mensaje de MFT \_ comienza el \_ \_ streaming</span><span class="sxs-lookup"><span data-stu-id="44d89-103">MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING</span></span>

<span data-ttu-id="44d89-104">Notifica a una transformación de Media Foundation (MFT) que la transmisión por secuencias está a punto de comenzar.</span><span class="sxs-lookup"><span data-stu-id="44d89-104">Notifies a Media Foundation transform (MFT) that streaming is about to begin.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="44d89-105">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="44d89-105">Message Parameter</span></span>

<span data-ttu-id="44d89-106">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44d89-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d89-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44d89-107">Remarks</span></span>

<span data-ttu-id="44d89-108">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="44d89-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="44d89-109">No es necesario que el cliente envíe este mensaje.</span><span class="sxs-lookup"><span data-stu-id="44d89-109">The client is not required to send this message.</span></span> <span data-ttu-id="44d89-110">Si el cliente envía este mensaje, debe hacerlo después de establecer todos los tipos de medios en la MFT y antes de llamar a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="44d89-110">If the client sends this message, it must do so after setting all of the media types on the MFT, and before calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="44d89-111">La MFT puede responder mediante la asignación de búferes u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="44d89-111">The MFT can respond by allocating buffers or other resources.</span></span> <span data-ttu-id="44d89-112">Si el cliente no envía este mensaje, la MFT asigna recursos en la primera llamada a **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="44d89-112">If the client does not send this message, the MFT allocates resources on the first call to **ProcessInput**.</span></span> <span data-ttu-id="44d89-113">Por lo tanto, el envío de este mensaje puede reducir la latencia inicial cuando se inicia la transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="44d89-113">Therefore, sending this message can reduce the initial latency when streaming begins.</span></span>

### <a name="implementation"></a><span data-ttu-id="44d89-114">Implementación</span><span class="sxs-lookup"><span data-stu-id="44d89-114">Implementation</span></span>

<span data-ttu-id="44d89-115">No se requiere una MFT para responder a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="44d89-115">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d89-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44d89-116">Requirements</span></span>



| <span data-ttu-id="44d89-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="44d89-117">Requirement</span></span> | <span data-ttu-id="44d89-118">Value</span><span class="sxs-lookup"><span data-stu-id="44d89-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44d89-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44d89-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44d89-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="44d89-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="44d89-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44d89-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44d89-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="44d89-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="44d89-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44d89-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44d89-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="44d89-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d89-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="44d89-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d89-126">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="44d89-126">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




