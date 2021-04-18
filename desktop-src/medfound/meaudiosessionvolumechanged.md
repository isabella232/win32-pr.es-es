---
description: Lo envía el representador de audio de transmisión por secuencias (SAR) cuando cambia el estado del volumen o el silenciador de la sesión de audio.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720404"
---
# <a name="meaudiosessionvolumechanged-event"></a><span data-ttu-id="0ef26-103">Evento MEAudioSessionVolumeChanged</span><span class="sxs-lookup"><span data-stu-id="0ef26-103">MEAudioSessionVolumeChanged event</span></span>

<span data-ttu-id="0ef26-104">Lo envía el representador de audio de transmisión por secuencias (SAR) cuando cambia el estado del volumen o el silenciador de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="0ef26-104">Sent by the streaming audio renderer (SAR) when the volume or mute state of the audio session changes.</span></span>

<span data-ttu-id="0ef26-105">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0ef26-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="0ef26-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0ef26-106">Event values</span></span>

<span data-ttu-id="0ef26-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ef26-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0ef26-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0ef26-108">VARTYPE</span></span>                | <span data-ttu-id="0ef26-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ef26-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef26-110">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="0ef26-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="0ef26-111">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="0ef26-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="0ef26-112">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="0ef26-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="0ef26-113">Puntero a la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="0ef26-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0ef26-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ef26-114">Remarks</span></span>

<span data-ttu-id="0ef26-115">Este evento es desencadenado por el receptor de la secuencia de SAR.</span><span class="sxs-lookup"><span data-stu-id="0ef26-115">This event is raised by the stream sink of the SAR.</span></span> <span data-ttu-id="0ef26-116">El evento se desencadena cuando el SAR recibe un evento [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="0ef26-116">The event is triggered when the SAR receives an [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) event from the audio session.</span></span> <span data-ttu-id="0ef26-117">Para obtener el nuevo nivel de volumen y silenciar el estado, llame a [**IMFSimpleAudioVolume:: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) y [**IMFSimpleAudioVolume:: GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span><span class="sxs-lookup"><span data-stu-id="0ef26-117">To get the new volume level and mute state, call [**IMFSimpleAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) and [**IMFSimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).</span></span>

<span data-ttu-id="0ef26-118">El SAR envía este evento si una acción externa cambia el volumen; por ejemplo, si el usuario cambia el volumen a través del programa de control de volumen del sistema (SndVol).</span><span class="sxs-lookup"><span data-stu-id="0ef26-118">The SAR sends this event if an external action changes the volume—for example, if the user changes the volume through the system volume-control program (SndVol).</span></span> <span data-ttu-id="0ef26-119">El SAR no envía el evento si la aplicación cambia el volumen directamente en el SAR.</span><span class="sxs-lookup"><span data-stu-id="0ef26-119">The SAR does not send the event if the application changes the volume directly on the SAR.</span></span>

<span data-ttu-id="0ef26-120">Además, el SAR no envía este evento cuando cambia el volumen del canal ([**IAudioSessionEvents:: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span><span class="sxs-lookup"><span data-stu-id="0ef26-120">Also, the SAR does not send this event when the channel volume changes ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef26-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ef26-121">Requirements</span></span>



| <span data-ttu-id="0ef26-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef26-122">Requirement</span></span> | <span data-ttu-id="0ef26-123">Value</span><span class="sxs-lookup"><span data-stu-id="0ef26-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef26-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ef26-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef26-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0ef26-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0ef26-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ef26-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef26-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ef26-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0ef26-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ef26-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef26-129"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef26-129"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef26-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ef26-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef26-131">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0ef26-131">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0ef26-132">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="0ef26-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
