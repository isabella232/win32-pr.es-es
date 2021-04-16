---
description: Lo genera el procesador de audio cuando se quita el dispositivo de audio. El representador de audio ahora no es válido.
ms.assetid: a65a3931-e0d6-47ac-b545-9d616e914109
title: Evento MEAudioSessionDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8153eca68d480f092a358c35bfcbad7cedffd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539947"
---
# <a name="meaudiosessiondeviceremoved-event"></a><span data-ttu-id="31abb-104">Evento MEAudioSessionDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="31abb-104">MEAudioSessionDeviceRemoved event</span></span>

<span data-ttu-id="31abb-105">Lo genera el procesador de audio cuando se quita el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="31abb-105">Raised by the audio renderer when the audio device is removed.</span></span> <span data-ttu-id="31abb-106">El representador de audio ahora no es válido.</span><span class="sxs-lookup"><span data-stu-id="31abb-106">The audio renderer is now invalid.</span></span>

<span data-ttu-id="31abb-107">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31abb-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="31abb-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="31abb-108">Event values</span></span>

<span data-ttu-id="31abb-109">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="31abb-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="31abb-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="31abb-110">VARTYPE</span></span>                | <span data-ttu-id="31abb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="31abb-111">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="31abb-112">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="31abb-112">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="31abb-113">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="31abb-113">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="31abb-114">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="31abb-114">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="31abb-115">Puntero a la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="31abb-115">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="31abb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31abb-116">Remarks</span></span>

<span data-ttu-id="31abb-117">El receptor de flujo del representador de audio envía este evento.</span><span class="sxs-lookup"><span data-stu-id="31abb-117">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="31abb-118">El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de la desconexión igual a **DisconnectReasonDeviceRemoval**.</span><span class="sxs-lookup"><span data-stu-id="31abb-118">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonDeviceRemoval**.</span></span>

<span data-ttu-id="31abb-119">El puntero [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , si está establecido, no es útil porque la secuencia de audio ya no es válida.</span><span class="sxs-lookup"><span data-stu-id="31abb-119">The [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) pointer, if set, is not useful, because the audio stream is no longer valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="31abb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31abb-120">Requirements</span></span>



| <span data-ttu-id="31abb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="31abb-121">Requirement</span></span> | <span data-ttu-id="31abb-122">Value</span><span class="sxs-lookup"><span data-stu-id="31abb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31abb-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31abb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="31abb-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="31abb-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="31abb-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31abb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="31abb-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="31abb-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31abb-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31abb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="31abb-128"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31abb-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31abb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="31abb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31abb-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31abb-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="31abb-131">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="31abb-131">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
