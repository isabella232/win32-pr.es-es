---
description: 'La inicia la sesión de medios cuando el método IMFMediaSession:: ClearTopologies se completa de forma asincrónica.'
ms.assetid: 2017d13b-8dc2-48f9-a21e-7b826e174edf
title: Evento MESessionTopologiesCleared (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551e98607a8d23d9333527337bbd7d038ed0b340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155580"
---
# <a name="mesessiontopologiescleared-event"></a><span data-ttu-id="e3529-103">Evento MESessionTopologiesCleared</span><span class="sxs-lookup"><span data-stu-id="e3529-103">MESessionTopologiesCleared event</span></span>

<span data-ttu-id="e3529-104">La inicia la sesión de medios cuando el método [**IMFMediaSession:: ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) se completa de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e3529-104">Raised by the Media Session when the [**IMFMediaSession::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="e3529-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e3529-105">Event values</span></span>

<span data-ttu-id="e3529-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e3529-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e3529-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e3529-107">VARTYPE</span></span>              | <span data-ttu-id="e3529-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3529-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e3529-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="e3529-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e3529-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="e3529-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="e3529-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3529-111">Requirements</span></span>



| <span data-ttu-id="e3529-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3529-112">Requirement</span></span> | <span data-ttu-id="e3529-113">Value</span><span class="sxs-lookup"><span data-stu-id="e3529-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3529-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3529-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e3529-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e3529-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e3529-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3529-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e3529-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3529-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e3529-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3529-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3529-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3529-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3529-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3529-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3529-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3529-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




