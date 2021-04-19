---
description: Enviado por un origen de captura de audio cuando cambia el volumen.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Evento MECaptureAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720417"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a><span data-ttu-id="fa751-103">Evento MECaptureAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="fa751-103">MECaptureAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="fa751-104">Enviado por un origen de captura de audio cuando cambia el volumen.</span><span class="sxs-lookup"><span data-stu-id="fa751-104">Sent by an audio capture source when the volume changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="fa751-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="fa751-105">Event values</span></span>

<span data-ttu-id="fa751-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="fa751-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fa751-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fa751-107">VARTYPE</span></span>               | <span data-ttu-id="fa751-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa751-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="fa751-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="fa751-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="fa751-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="fa751-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fa751-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa751-111">Remarks</span></span>

<span data-ttu-id="fa751-112">Este evento lo envía el flujo multimedia del origen de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="fa751-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="fa751-113">El origen de captura de audio envía este evento si una acción externa cambia el volumen; por ejemplo, si el usuario cambia el volumen a través del panel de control.</span><span class="sxs-lookup"><span data-stu-id="fa751-113">The audio capture source sends this event if an external action changes the volume—for example, if the user changes the volume through the Control Panel.</span></span> <span data-ttu-id="fa751-114">El origen de captura no envía el evento si la aplicación cambia el volumen directamente en el origen.</span><span class="sxs-lookup"><span data-stu-id="fa751-114">The capture source does not send the event if the application changes the volume directly on the source.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa751-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa751-115">Requirements</span></span>



| <span data-ttu-id="fa751-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa751-116">Requirement</span></span> | <span data-ttu-id="fa751-117">Value</span><span class="sxs-lookup"><span data-stu-id="fa751-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa751-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa751-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fa751-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa751-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="fa751-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa751-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fa751-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa751-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa751-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa751-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa751-123"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa751-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa751-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa751-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa751-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fa751-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




