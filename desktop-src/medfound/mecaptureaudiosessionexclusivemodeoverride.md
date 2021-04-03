---
description: Enviado por un origen de captura de audio cuando otro programa abre el dispositivo de audio en modo exclusivo.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Evento MECaptureAudioSessionExclusiveModeOverride (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809608"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a><span data-ttu-id="f716f-103">Evento MECaptureAudioSessionExclusiveModeOverride</span><span class="sxs-lookup"><span data-stu-id="f716f-103">MECaptureAudioSessionExclusiveModeOverride event</span></span>

<span data-ttu-id="f716f-104">Enviado por un origen de captura de audio cuando otro programa abre el dispositivo de audio en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f716f-104">Sent by an audio capture source when another program opens the audio device in exclusive mode.</span></span>

## <a name="event-values"></a><span data-ttu-id="f716f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f716f-105">Event values</span></span>

<span data-ttu-id="f716f-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f716f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f716f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f716f-107">VARTYPE</span></span>               | <span data-ttu-id="f716f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f716f-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="f716f-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="f716f-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="f716f-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="f716f-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f716f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f716f-111">Remarks</span></span>

<span data-ttu-id="f716f-112">Este evento lo envía el flujo multimedia del origen de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="f716f-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="f716f-113">El origen de la captura envía este evento cuando recibe un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de la desconexión igual a **DisconnectReasonExclusiveModeOverride**.</span><span class="sxs-lookup"><span data-stu-id="f716f-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonExclusiveModeOverride**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f716f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f716f-114">Requirements</span></span>



| <span data-ttu-id="f716f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f716f-115">Requirement</span></span> | <span data-ttu-id="f716f-116">Value</span><span class="sxs-lookup"><span data-stu-id="f716f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f716f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f716f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f716f-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f716f-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f716f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f716f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f716f-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f716f-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f716f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f716f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f716f-122"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f716f-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f716f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f716f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f716f-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f716f-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
