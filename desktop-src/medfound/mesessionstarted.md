---
description: 'Se genera cuando el método IMFMediaSession:: Start se completa de forma asincrónica.'
ms.assetid: 28ed32f0-9b23-4da1-9587-15f490da7bf9
title: Evento MESessionStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9510fb5f5dda3d14b916ed40dcba4ca05800b52b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082354"
---
# <a name="mesessionstarted-event"></a><span data-ttu-id="41db6-103">Evento MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="41db6-103">MESessionStarted event</span></span>

<span data-ttu-id="41db6-104">Se genera cuando el método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="41db6-104">Raised when the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="41db6-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="41db6-105">Event values</span></span>

<span data-ttu-id="41db6-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="41db6-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="41db6-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="41db6-107">VARTYPE</span></span>              | <span data-ttu-id="41db6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="41db6-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="41db6-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="41db6-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="41db6-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="41db6-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="41db6-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="41db6-111">Attributes</span></span>

<span data-ttu-id="41db6-112">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="41db6-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="41db6-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="41db6-113">Attribute</span></span>                                                                                               | <span data-ttu-id="41db6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="41db6-114">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41db6-115">**\_desplazamiento de \_ tiempo de presentación de evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41db6-115">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/> | <span data-ttu-id="41db6-116">Desplazamiento entre el tiempo de presentación y las marcas de tiempo del origen del medio.</span><span class="sxs-lookup"><span data-stu-id="41db6-116">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="41db6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41db6-117">Requirements</span></span>



| <span data-ttu-id="41db6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="41db6-118">Requirement</span></span> | <span data-ttu-id="41db6-119">Value</span><span class="sxs-lookup"><span data-stu-id="41db6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41db6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41db6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41db6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="41db6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41db6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41db6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41db6-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="41db6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41db6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41db6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="41db6-125"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41db6-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41db6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="41db6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41db6-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41db6-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




