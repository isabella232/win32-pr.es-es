---
description: Solicita que una transformación de Media Foundation (MFT) a ese streaming esté a punto de finalizar.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543910"
---
# <a name="mft_message_notify_end_streaming"></a><span data-ttu-id="dd3f1-103">\_fin de \_ notificación de mensaje \_ de MFT \_</span><span class="sxs-lookup"><span data-stu-id="dd3f1-103">MFT\_MESSAGE\_NOTIFY\_END\_STREAMING</span></span>

<span data-ttu-id="dd3f1-104">Solicita que una transformación de Media Foundation (MFT) a ese streaming esté a punto de finalizar.</span><span class="sxs-lookup"><span data-stu-id="dd3f1-104">Requests a Media Foundation transform (MFT) to that streaming is about to end.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="dd3f1-105">Parámetro de mensaje</span><span class="sxs-lookup"><span data-stu-id="dd3f1-105">Message Parameter</span></span>

<span data-ttu-id="dd3f1-106">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd3f1-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd3f1-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd3f1-107">Remarks</span></span>

<span data-ttu-id="dd3f1-108">Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="dd3f1-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="dd3f1-109">No es necesario que el cliente envíe este mensaje, incluso si el cliente envió anteriormente el **mensaje de MFT \_ \_ Notify \_ Begin \_ streaming** .</span><span class="sxs-lookup"><span data-stu-id="dd3f1-109">The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.</span></span>

### <a name="implementation"></a><span data-ttu-id="dd3f1-110">Implementación</span><span class="sxs-lookup"><span data-stu-id="dd3f1-110">Implementation</span></span>

<span data-ttu-id="dd3f1-111">La MFT puede responder a este mensaje liberando búferes y otros recursos.</span><span class="sxs-lookup"><span data-stu-id="dd3f1-111">The MFT can respond to this message by releasing buffers and other resources.</span></span> <span data-ttu-id="dd3f1-112">MFT no vacía los datos de entrada ni restablece los tipos de medios en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd3f1-112">The MFT does not flush input data or reset the media types in response to this message.</span></span> <span data-ttu-id="dd3f1-113">No se requiere una MFT para responder a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd3f1-113">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3f1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd3f1-114">Requirements</span></span>



| <span data-ttu-id="dd3f1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd3f1-115">Requirement</span></span> | <span data-ttu-id="dd3f1-116">Value</span><span class="sxs-lookup"><span data-stu-id="dd3f1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd3f1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd3f1-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3f1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dd3f1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd3f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dd3f1-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd3f1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dd3f1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd3f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd3f1-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd3f1-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd3f1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd3f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3f1-124">**\_tipo de mensaje de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="dd3f1-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




