---
description: Generado por una secuencia de medios cuando finaliza la secuencia.
ms.assetid: e793131a-f737-411f-a9fc-03b5b3d09aea
title: Evento MEEndOfStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb70af021c1a35af829df9b3c80c0c2b71aa120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908475"
---
# <a name="meendofstream-event"></a><span data-ttu-id="b35ea-103">Evento MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="b35ea-103">MEEndOfStream event</span></span>

<span data-ttu-id="b35ea-104">Generado por una secuencia de medios cuando finaliza la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b35ea-104">Raised by a media stream when the stream ends.</span></span>

## <a name="event-values"></a><span data-ttu-id="b35ea-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="b35ea-105">Event values</span></span>

<span data-ttu-id="b35ea-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="b35ea-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="b35ea-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="b35ea-107">VARTYPE</span></span>              | <span data-ttu-id="b35ea-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b35ea-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="b35ea-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="b35ea-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="b35ea-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="b35ea-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b35ea-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b35ea-111">Remarks</span></span>

<span data-ttu-id="b35ea-112">Cuando la [sesión multimedia](media-session.md) recibe el evento MEEndOfStream, llama a [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) en el receptor multimedia correspondiente, con el tipo de marcador **\_ \_ ENDOFSEGMENT de marcador de MFSTREAMSINK** .</span><span class="sxs-lookup"><span data-stu-id="b35ea-112">When the [Media Session](media-session.md) receives the MEEndOfStream event, it calls [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) on the corresponding media sink, with the **MFSTREAMSINK\_MARKER\_ENDOFSEGMENT** marker type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b35ea-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b35ea-113">Requirements</span></span>



| <span data-ttu-id="b35ea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b35ea-114">Requirement</span></span> | <span data-ttu-id="b35ea-115">Value</span><span class="sxs-lookup"><span data-stu-id="b35ea-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b35ea-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b35ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b35ea-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b35ea-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b35ea-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b35ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b35ea-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b35ea-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b35ea-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b35ea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b35ea-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b35ea-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b35ea-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b35ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35ea-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b35ea-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




