---
description: 'Generado por un origen de medios cuando cambia la velocidad de reproducción. Este evento se envía después de que el método IMFRateControl:: SetRate se complete de forma asincrónica.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Evento MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154656"
---
# <a name="mesourceratechanged-event"></a><span data-ttu-id="13822-104">Evento MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="13822-104">MESourceRateChanged event</span></span>

<span data-ttu-id="13822-105">Generado por un origen de medios cuando cambia la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="13822-105">Raised by a media source when the playback rate changes.</span></span> <span data-ttu-id="13822-106">Este evento se envía después de que el método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) se complete de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="13822-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="13822-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="13822-107">Event values</span></span>

<span data-ttu-id="13822-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="13822-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="13822-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="13822-109">VARTYPE</span></span>           | <span data-ttu-id="13822-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="13822-110">Description</span></span>                                   |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="13822-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="13822-111">VT\_R4</span></span><br/> | <span data-ttu-id="13822-112">La nueva velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="13822-112">The new playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="13822-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13822-113">Requirements</span></span>



| <span data-ttu-id="13822-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13822-114">Requirement</span></span> | <span data-ttu-id="13822-115">Value</span><span class="sxs-lookup"><span data-stu-id="13822-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13822-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13822-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13822-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="13822-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13822-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13822-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13822-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="13822-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13822-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13822-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="13822-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13822-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13822-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="13822-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13822-123">Control de tasa de implementación</span><span class="sxs-lookup"><span data-stu-id="13822-123">Implementing Rate Control</span></span>](implementing-rate-control.md)
</dt> <dt>

[<span data-ttu-id="13822-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="13822-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="13822-125">Control de tasa</span><span class="sxs-lookup"><span data-stu-id="13822-125">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="13822-126">**IMFRateControl::SetRate**</span><span class="sxs-lookup"><span data-stu-id="13822-126">**IMFRateControl::SetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




