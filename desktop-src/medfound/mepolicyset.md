---
description: 'Generado por una autoridad de confianza de salida (OTA) cuando el método IMFOutputTrustAuthority:: SetPolicy se completa de forma asincrónica.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Evento MEPolicySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715664"
---
# <a name="mepolicyset-event"></a><span data-ttu-id="37d19-103">Evento MEPolicySet</span><span class="sxs-lookup"><span data-stu-id="37d19-103">MEPolicySet event</span></span>

<span data-ttu-id="37d19-104">Generado por una autoridad de confianza de salida (OTA) cuando el método [**IMFOutputTrustAuthority:: SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="37d19-104">Raised by an output trust authority (OTA) when the [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="37d19-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="37d19-105">Event values</span></span>

<span data-ttu-id="37d19-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="37d19-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="37d19-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="37d19-107">VARTYPE</span></span>              | <span data-ttu-id="37d19-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="37d19-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="37d19-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="37d19-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="37d19-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="37d19-110">No event data.</span></span><br/> <br/> |
| <span data-ttu-id="37d19-111">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="37d19-111">VT\_UI4</span></span><br/> | <span data-ttu-id="37d19-112">Identificador que se puede establecer en un [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) a través del atributo [MF_POLICY_ID](mf-policy-id.md) .</span><span class="sxs-lookup"><span data-stu-id="37d19-112">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) through the [MF_POLICY_ID](mf-policy-id.md) attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="37d19-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37d19-113">Requirements</span></span>



| <span data-ttu-id="37d19-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="37d19-114">Requirement</span></span> | <span data-ttu-id="37d19-115">Value</span><span class="sxs-lookup"><span data-stu-id="37d19-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d19-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37d19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37d19-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="37d19-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="37d19-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37d19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37d19-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="37d19-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37d19-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37d19-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d19-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37d19-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37d19-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="37d19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d19-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37d19-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




