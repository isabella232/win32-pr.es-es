---
description: Generado por un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Evento MEStreamSinkRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c5afbfa9f0cfe4b320b451e699612a4729c23a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677594"
---
# <a name="mestreamsinkrequestsample-event"></a><span data-ttu-id="b10ca-103">Evento MEStreamSinkRequestSample</span><span class="sxs-lookup"><span data-stu-id="b10ca-103">MEStreamSinkRequestSample event</span></span>

<span data-ttu-id="b10ca-104">Generado por un receptor de flujo para solicitar un nuevo ejemplo multimedia de la canalización.</span><span class="sxs-lookup"><span data-stu-id="b10ca-104">Raised by a stream sink to request a new media sample from the pipeline.</span></span> <span data-ttu-id="b10ca-105">Para cada evento MEStreamSinkRequestSample, la canalización solicita datos del siguiente componente de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b10ca-105">For each MEStreamSinkRequestSample event, the pipeline requests data from the next upstream component.</span></span>

## <a name="event-values"></a><span data-ttu-id="b10ca-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="b10ca-106">Event values</span></span>

<span data-ttu-id="b10ca-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="b10ca-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b10ca-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b10ca-108">VARTYPE</span></span>              | <span data-ttu-id="b10ca-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b10ca-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b10ca-110">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="b10ca-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b10ca-111">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="b10ca-111">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="b10ca-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b10ca-112">Requirements</span></span>



| <span data-ttu-id="b10ca-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b10ca-113">Requirement</span></span> | <span data-ttu-id="b10ca-114">Value</span><span class="sxs-lookup"><span data-stu-id="b10ca-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b10ca-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b10ca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b10ca-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b10ca-116">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b10ca-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b10ca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b10ca-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b10ca-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b10ca-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b10ca-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b10ca-120"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b10ca-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b10ca-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b10ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b10ca-122">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b10ca-122">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="b10ca-123">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="b10ca-123">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




