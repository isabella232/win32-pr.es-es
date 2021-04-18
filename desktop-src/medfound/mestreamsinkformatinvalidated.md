---
description: Enviado por un receptor de flujo cuando se ha invalidado el formato de bajada y se debe volver a negociar.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Evento MEStreamSinkFormatInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715308"
---
# <a name="mestreamsinkformatinvalidated-event"></a><span data-ttu-id="b161f-103">Evento MEStreamSinkFormatInvalidated</span><span class="sxs-lookup"><span data-stu-id="b161f-103">MEStreamSinkFormatInvalidated event</span></span>

<span data-ttu-id="b161f-104">Enviado por un receptor de flujo cuando se ha invalidado el formato de bajada y se debe volver a negociar.</span><span class="sxs-lookup"><span data-stu-id="b161f-104">Sent by a stream sink when the downstream format has become invalidated and it needs to be renegotiated.</span></span>

## <a name="event-values"></a><span data-ttu-id="b161f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="b161f-105">Event values</span></span>

<span data-ttu-id="b161f-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="b161f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b161f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b161f-107">VARTYPE</span></span>              | <span data-ttu-id="b161f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b161f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b161f-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="b161f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b161f-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="b161f-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b161f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b161f-111">Remarks</span></span>

<span data-ttu-id="b161f-112">Los datos que se han puesto en cola en el receptor, más allá de la posición de reproducción actual, deben reenviarse.</span><span class="sxs-lookup"><span data-stu-id="b161f-112">Data that was queued to the sink, past the current playback position, should be resent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b161f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b161f-113">Requirements</span></span>



| <span data-ttu-id="b161f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b161f-114">Requirement</span></span> | <span data-ttu-id="b161f-115">Value</span><span class="sxs-lookup"><span data-stu-id="b161f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b161f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b161f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b161f-117">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="b161f-117">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                                      |
| <span data-ttu-id="b161f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b161f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b161f-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b161f-119">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="b161f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b161f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b161f-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b161f-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b161f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b161f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b161f-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b161f-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




