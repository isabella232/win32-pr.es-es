---
description: Enviado por un origen de captura de audio cuando el desconexión de audio está desconectado porque el usuario cerró sesión en una sesión de Windows Terminal Services (WTS).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Evento MECaptureAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154881"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a><span data-ttu-id="14a1d-103">Evento MECaptureAudioSessionDisconnected</span><span class="sxs-lookup"><span data-stu-id="14a1d-103">MECaptureAudioSessionDisconnected event</span></span>

<span data-ttu-id="14a1d-104">Enviado por un origen de captura de audio cuando el desconexión de audio está desconectado porque el usuario cerró sesión en una sesión de Windows Terminal Services (WTS).</span><span class="sxs-lookup"><span data-stu-id="14a1d-104">Sent by an audio capture source when the audio dession is disconnected because the user logged off from a Windows Terminal Services (WTS) session.</span></span>

## <a name="event-values"></a><span data-ttu-id="14a1d-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="14a1d-105">Event values</span></span>

<span data-ttu-id="14a1d-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="14a1d-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="14a1d-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="14a1d-107">VARTYPE</span></span>               | <span data-ttu-id="14a1d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="14a1d-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="14a1d-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="14a1d-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="14a1d-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="14a1d-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="14a1d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14a1d-111">Remarks</span></span>

<span data-ttu-id="14a1d-112">Este evento lo envía el flujo multimedia del origen de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="14a1d-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="14a1d-113">El origen de la captura envía este evento cuando recibe un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de la desconexión igual a **DisconnectReasonSessionDisconnected**.</span><span class="sxs-lookup"><span data-stu-id="14a1d-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonSessionDisconnected**.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a1d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a1d-114">Requirements</span></span>



| <span data-ttu-id="14a1d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a1d-115">Requirement</span></span> | <span data-ttu-id="14a1d-116">Value</span><span class="sxs-lookup"><span data-stu-id="14a1d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a1d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14a1d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14a1d-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="14a1d-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="14a1d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14a1d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14a1d-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="14a1d-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14a1d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14a1d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14a1d-122"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14a1d-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14a1d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="14a1d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a1d-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="14a1d-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
