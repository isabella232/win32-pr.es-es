---
description: Lo genera la sesión multimedia cuando ha terminado de reproducir la última presentación en la cola de reproducción.
ms.assetid: e593e51f-c239-49e9-bba8-c6d8238eff24
title: Evento MESessionEnded (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447b222be48dccc0f190329ab0bb6d56d09b266e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720474"
---
# <a name="mesessionended-event"></a><span data-ttu-id="a8eb5-103">Evento MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="a8eb5-103">MESessionEnded event</span></span>

<span data-ttu-id="a8eb5-104">Lo genera la sesión multimedia cuando ha terminado de reproducir la última presentación en la cola de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-104">Raised by the Media Session when it has finished playing the last presentation in the playback queue.</span></span>

## <a name="event-values"></a><span data-ttu-id="a8eb5-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a8eb5-105">Event values</span></span>

<span data-ttu-id="a8eb5-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a8eb5-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a8eb5-107">VARTYPE</span></span>              | <span data-ttu-id="a8eb5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8eb5-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a8eb5-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="a8eb5-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a8eb5-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="a8eb5-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="a8eb5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8eb5-111">Requirements</span></span>



| <span data-ttu-id="a8eb5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8eb5-112">Requirement</span></span> | <span data-ttu-id="a8eb5-113">Value</span><span class="sxs-lookup"><span data-stu-id="a8eb5-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8eb5-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8eb5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a8eb5-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a8eb5-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8eb5-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8eb5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a8eb5-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8eb5-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8eb5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8eb5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8eb5-119"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8eb5-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8eb5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8eb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8eb5-121">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8eb5-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




