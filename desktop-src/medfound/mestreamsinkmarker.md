---
description: Generado por un receptor de secuencia después de llamar al método IMFStreamSink::P laceMarker.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Evento MEStreamSinkMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071d6e5b25873739c176d1c808929c26e1e338bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811870"
---
# <a name="mestreamsinkmarker-event"></a><span data-ttu-id="3995a-103">Evento MEStreamSinkMarker</span><span class="sxs-lookup"><span data-stu-id="3995a-103">MEStreamSinkMarker event</span></span>

<span data-ttu-id="3995a-104">Generado por un receptor de secuencia después de llamar al método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="3995a-104">Raised by a stream sink after the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="3995a-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="3995a-105">Event values</span></span>

<span data-ttu-id="3995a-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="3995a-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3995a-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3995a-107">VARTYPE</span></span>            | <span data-ttu-id="3995a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3995a-108">Description</span></span>                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3995a-109">>cualquier</span><span class="sxs-lookup"><span data-stu-id="3995a-109">>Any</span></span><br/> | <span data-ttu-id="3995a-110">El valor del evento es una copia del **PROPVARIANT** que el autor de la llamada especificó en el parámetro *PvarContextValue* del método [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="3995a-110">The event value is a copy of the **PROPVARIANT** that the caller specified in the *pvarContextValue* parameter of the [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="3995a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3995a-111">Requirements</span></span>



| <span data-ttu-id="3995a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3995a-112">Requirement</span></span> | <span data-ttu-id="3995a-113">Value</span><span class="sxs-lookup"><span data-stu-id="3995a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3995a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3995a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3995a-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3995a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3995a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3995a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3995a-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3995a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3995a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3995a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3995a-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3995a-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3995a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3995a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3995a-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3995a-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="3995a-122">Receptores de medios</span><span class="sxs-lookup"><span data-stu-id="3995a-122">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




