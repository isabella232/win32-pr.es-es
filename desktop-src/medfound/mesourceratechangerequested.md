---
description: 'Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción. La aplicación debe llamar a IMFRateControl:: SetRate con la tasa solicitada. Un origen multimedia podría producir este evento si no puede continuar la reproducción a la velocidad actual.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275967"
---
# <a name="mesourceratechangerequested-event"></a><span data-ttu-id="bb104-105">Evento MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="bb104-105">MESourceRateChangeRequested event</span></span>

<span data-ttu-id="bb104-106">Lo genera un origen multimedia para solicitar una nueva velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="bb104-106">Raised by a media source to request a new playback rate.</span></span> <span data-ttu-id="bb104-107">La aplicación debe llamar a [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) con la tasa solicitada.</span><span class="sxs-lookup"><span data-stu-id="bb104-107">The application should call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) with the requested rate.</span></span> <span data-ttu-id="bb104-108">Un origen multimedia podría producir este evento si no puede continuar la reproducción a la velocidad actual.</span><span class="sxs-lookup"><span data-stu-id="bb104-108">A media source might raise this event if it cannot continue playback at the current rate.</span></span>

## <a name="event-values"></a><span data-ttu-id="bb104-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="bb104-109">Event values</span></span>

<span data-ttu-id="bb104-110">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="bb104-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bb104-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bb104-111">VARTYPE</span></span>           | <span data-ttu-id="bb104-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb104-112">Description</span></span>                                             |
|-------------------|---------------------------------------------------------|
| <span data-ttu-id="bb104-113">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="bb104-113">VT\_R4</span></span><br/> | <span data-ttu-id="bb104-114">La nueva velocidad de reproducción solicitada.</span><span class="sxs-lookup"><span data-stu-id="bb104-114">The requested new playback rate.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="bb104-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb104-115">Attributes</span></span>

<span data-ttu-id="bb104-116">Para este evento, se definen los atributos siguientes.</span><span class="sxs-lookup"><span data-stu-id="bb104-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="bb104-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="bb104-117">Attribute</span></span>                                                                    | <span data-ttu-id="bb104-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb104-118">Description</span></span>                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="bb104-119">**el \_ evento \_ MF \_ simplifica**</span><span class="sxs-lookup"><span data-stu-id="bb104-119">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)<br/> | <span data-ttu-id="bb104-120">Especifica si el origen multimedia también solicita el ligero.</span><span class="sxs-lookup"><span data-stu-id="bb104-120">Specifies whether the media source also requests thinning.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="bb104-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb104-121">Requirements</span></span>



| <span data-ttu-id="bb104-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb104-122">Requirement</span></span> | <span data-ttu-id="bb104-123">Value</span><span class="sxs-lookup"><span data-stu-id="bb104-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb104-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb104-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bb104-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb104-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb104-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb104-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bb104-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb104-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb104-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb104-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb104-129"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb104-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb104-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb104-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb104-131">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb104-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




