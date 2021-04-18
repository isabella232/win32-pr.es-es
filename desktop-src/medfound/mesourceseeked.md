---
description: 'Se genera cuando un origen multimedia busca una nueva posición. Un origen multimedia genera este evento si el origen se está ejecutando o está en pausa y la aplicación llama a IMFMediaSource:: Start con una hora de inicio que no es igual a la posición actual.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715316"
---
# <a name="mesourceseeked-event"></a><span data-ttu-id="fea33-104">Evento MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="fea33-104">MESourceSeeked event</span></span>

<span data-ttu-id="fea33-105">Se genera cuando un origen multimedia busca una nueva posición.</span><span class="sxs-lookup"><span data-stu-id="fea33-105">Raised when a media source seeks to a new position.</span></span> <span data-ttu-id="fea33-106">Un origen multimedia genera este evento si el origen se está ejecutando o está en pausa y la aplicación llama a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con una hora de inicio que no es igual a la posición actual.</span><span class="sxs-lookup"><span data-stu-id="fea33-106">A media source raises this event if the source is running or paused and the application calls [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) with a start time that does not equal the current position.</span></span>

## <a name="event-values"></a><span data-ttu-id="fea33-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="fea33-107">Event values</span></span>

<span data-ttu-id="fea33-108">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="fea33-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fea33-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fea33-109">VARTYPE</span></span>           | <span data-ttu-id="fea33-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fea33-110">Description</span></span>                                                                |
|-------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="fea33-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="fea33-111">VT\_I8</span></span><br/> | <span data-ttu-id="fea33-112">La nueva posición inicial, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="fea33-112">The new starting position, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="fea33-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fea33-113">Requirements</span></span>



| <span data-ttu-id="fea33-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fea33-114">Requirement</span></span> | <span data-ttu-id="fea33-115">Value</span><span class="sxs-lookup"><span data-stu-id="fea33-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fea33-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fea33-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fea33-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fea33-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fea33-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fea33-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fea33-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fea33-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fea33-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fea33-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea33-121"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fea33-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea33-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fea33-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea33-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fea33-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




