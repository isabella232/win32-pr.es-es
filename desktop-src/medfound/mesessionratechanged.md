---
description: 'La inicia la sesión de medios cuando cambia la velocidad de reproducción. Este evento se envía después de que el método IMFRateControl:: SetRate se complete de forma asincrónica.'
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Evento MESessionRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908472"
---
# <a name="mesessionratechanged-event"></a><span data-ttu-id="5474d-104">Evento MESessionRateChanged</span><span class="sxs-lookup"><span data-stu-id="5474d-104">MESessionRateChanged event</span></span>

<span data-ttu-id="5474d-105">La inicia la sesión de medios cuando cambia la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="5474d-105">Raised by the Media Session when the playback rate changes.</span></span> <span data-ttu-id="5474d-106">Este evento se envía después de que el método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) se complete de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="5474d-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="5474d-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="5474d-107">Event values</span></span>

<span data-ttu-id="5474d-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5474d-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5474d-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5474d-109">VARTYPE</span></span>           | <span data-ttu-id="5474d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5474d-110">Description</span></span>                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5474d-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="5474d-111">VT\_R4</span></span><br/> | <span data-ttu-id="5474d-112">La nueva velocidad de reproducción, expresada como proporción de la velocidad de reproducción normal.</span><span class="sxs-lookup"><span data-stu-id="5474d-112">The new playback rate, expressed as a ratio of the normal playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="5474d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5474d-113">Requirements</span></span>



| <span data-ttu-id="5474d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5474d-114">Requirement</span></span> | <span data-ttu-id="5474d-115">Value</span><span class="sxs-lookup"><span data-stu-id="5474d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5474d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5474d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5474d-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5474d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5474d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5474d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5474d-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5474d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5474d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5474d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5474d-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5474d-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5474d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="5474d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5474d-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5474d-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




