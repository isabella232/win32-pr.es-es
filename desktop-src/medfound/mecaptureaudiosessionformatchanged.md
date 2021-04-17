---
description: Enviado por un origen de captura de audio cuando cambia el formato de audio.
ms.assetid: 8197BBAD-8102-43C3-BA61-8DC3BC13B7D6
title: Evento MECaptureAudioSessionFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfb260d186a9e4d8434669e6a8c3ef08078b93af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360436"
---
# <a name="mecaptureaudiosessionformatchanged-event"></a><span data-ttu-id="d0c92-103">Evento MECaptureAudioSessionFormatChanged</span><span class="sxs-lookup"><span data-stu-id="d0c92-103">MECaptureAudioSessionFormatChanged event</span></span>

<span data-ttu-id="d0c92-104">Enviado por un origen de captura de audio cuando cambia el formato de audio.</span><span class="sxs-lookup"><span data-stu-id="d0c92-104">Sent by an audio capture source when the audio format changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="d0c92-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="d0c92-105">Event values</span></span>

<span data-ttu-id="d0c92-106">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="d0c92-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d0c92-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d0c92-107">VARTYPE</span></span>               | <span data-ttu-id="d0c92-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0c92-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="d0c92-109">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="d0c92-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="d0c92-110">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="d0c92-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="d0c92-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0c92-111">Remarks</span></span>

<span data-ttu-id="d0c92-112">Este evento lo envía el flujo multimedia del origen de captura de audio.</span><span class="sxs-lookup"><span data-stu-id="d0c92-112">This event is sent by the media stream of the audio capture source.</span></span>

<span data-ttu-id="d0c92-113">El origen de la captura envía este evento cuando recibe un evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) de la sesión de audio con el motivo de la desconexión igual a **DisconnectReasonFormatChanged**.</span><span class="sxs-lookup"><span data-stu-id="d0c92-113">The capture source sends this event when it receives an [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) event from the audio session with the disconnection reason equal to **DisconnectReasonFormatChanged**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c92-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0c92-114">Requirements</span></span>



| <span data-ttu-id="d0c92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0c92-115">Requirement</span></span> | <span data-ttu-id="d0c92-116">Value</span><span class="sxs-lookup"><span data-stu-id="d0c92-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c92-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0c92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d0c92-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0c92-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d0c92-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0c92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d0c92-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0c92-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0c92-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0c92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0c92-122"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0c92-122"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c92-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0c92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c92-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0c92-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 
