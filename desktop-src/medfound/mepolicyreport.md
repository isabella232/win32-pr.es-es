---
description: Generado por una salida de confianza para enviar información de estado sobre el cumplimiento de la Directiva de salida.
ms.assetid: 4906f6c3-1570-421f-aef1-914bd338bb1f
title: Evento MEPolicyReport (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0053fb551a69b820beeb4237211cb9af446f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677597"
---
# <a name="mepolicyreport-event"></a><span data-ttu-id="123c1-103">Evento MEPolicyReport</span><span class="sxs-lookup"><span data-stu-id="123c1-103">MEPolicyReport event</span></span>

<span data-ttu-id="123c1-104">Generado por una salida de confianza para enviar información de estado sobre el cumplimiento de la Directiva de salida.</span><span class="sxs-lookup"><span data-stu-id="123c1-104">Raised by a trusted output to send status information about the enforcement of the output policy.</span></span>

## <a name="event-values"></a><span data-ttu-id="123c1-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="123c1-105">Event values</span></span>

<span data-ttu-id="123c1-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="123c1-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="123c1-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="123c1-107">VARTYPE</span></span>              | <span data-ttu-id="123c1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="123c1-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="123c1-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="123c1-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="123c1-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="123c1-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="123c1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="123c1-111">Remarks</span></span>

<span data-ttu-id="123c1-112">Los atributos y códigos de estado de este evento dependen del sistema de protección de contenido específico aplicado por la salida de confianza.</span><span class="sxs-lookup"><span data-stu-id="123c1-112">Attributes and status codes for this event depend on the specific content protection system enforced by the trusted output.</span></span>

## <a name="requirements"></a><span data-ttu-id="123c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="123c1-113">Requirements</span></span>



| <span data-ttu-id="123c1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="123c1-114">Requirement</span></span> | <span data-ttu-id="123c1-115">Value</span><span class="sxs-lookup"><span data-stu-id="123c1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="123c1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="123c1-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="123c1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="123c1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="123c1-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="123c1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="123c1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="123c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="123c1-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="123c1-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="123c1-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="123c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123c1-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="123c1-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




