---
description: Generado por un origen multimedia cuando el método IMFMediaSource::P ause se completa de forma asincrónica.
ms.assetid: cca03d60-47ae-4a11-b29d-81d749e24df9
title: Evento MESourcePaused (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac346e679eb3a82ca707a14f772f1a79e2a1e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908468"
---
# <a name="mesourcepaused-event"></a><span data-ttu-id="6eeeb-103">Evento MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="6eeeb-103">MESourcePaused event</span></span>

<span data-ttu-id="6eeeb-104">Generado por un origen multimedia cuando el método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="6eeeb-104">Raised by a media source when the [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="6eeeb-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="6eeeb-105">Event values</span></span>

<span data-ttu-id="6eeeb-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6eeeb-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="6eeeb-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="6eeeb-107">VARTYPE</span></span>              | <span data-ttu-id="6eeeb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6eeeb-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="6eeeb-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="6eeeb-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="6eeeb-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="6eeeb-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="6eeeb-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eeeb-111">Requirements</span></span>



| <span data-ttu-id="6eeeb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eeeb-112">Requirement</span></span> | <span data-ttu-id="6eeeb-113">Value</span><span class="sxs-lookup"><span data-stu-id="6eeeb-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eeeb-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eeeb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6eeeb-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6eeeb-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6eeeb-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eeeb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6eeeb-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6eeeb-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6eeeb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6eeeb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eeeb-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6eeeb-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eeeb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6eeeb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eeeb-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6eeeb-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




