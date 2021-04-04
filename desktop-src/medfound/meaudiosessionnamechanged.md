---
description: Generado por el procesador de audio cuando cambia el nombre para mostrar de la sesión de audio.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Evento MEAudioSessionNameChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810808"
---
# <a name="meaudiosessionnamechanged-event"></a><span data-ttu-id="88c24-103">Evento MEAudioSessionNameChanged</span><span class="sxs-lookup"><span data-stu-id="88c24-103">MEAudioSessionNameChanged event</span></span>

<span data-ttu-id="88c24-104">Generado por el procesador de audio cuando cambia el nombre para mostrar de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="88c24-104">Raised by the audio renderer when the audio session display name changes.</span></span>

<span data-ttu-id="88c24-105">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="88c24-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="88c24-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="88c24-106">Event values</span></span>

<span data-ttu-id="88c24-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="88c24-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="88c24-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="88c24-108">VARTYPE</span></span>                | <span data-ttu-id="88c24-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="88c24-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c24-110">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="88c24-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="88c24-111">Puntero a la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="88c24-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="88c24-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88c24-112">Remarks</span></span>

<span data-ttu-id="88c24-113">El receptor de flujo del representador de audio envía este evento.</span><span class="sxs-lookup"><span data-stu-id="88c24-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="88c24-114">El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents:: OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="88c24-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) event from the audio session.</span></span>

<span data-ttu-id="88c24-115">Para obtener el nuevo nombre para mostrar, llame a [**IMFAudioPolicy:: getDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span><span class="sxs-lookup"><span data-stu-id="88c24-115">To get the new display name, call [**IMFAudioPolicy::GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).</span></span>

## <a name="requirements"></a><span data-ttu-id="88c24-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88c24-116">Requirements</span></span>



| <span data-ttu-id="88c24-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c24-117">Requirement</span></span> | <span data-ttu-id="88c24-118">Value</span><span class="sxs-lookup"><span data-stu-id="88c24-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c24-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88c24-119">Minimum supported client</span></span><br/> | <span data-ttu-id="88c24-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88c24-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="88c24-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88c24-121">Minimum supported server</span></span><br/> | <span data-ttu-id="88c24-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88c24-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88c24-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88c24-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="88c24-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88c24-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c24-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="88c24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c24-126">**IMFAudioPolicy:: GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="88c24-126">**IMFAudioPolicy::GetDisplayName**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[<span data-ttu-id="88c24-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="88c24-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="88c24-128">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="88c24-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
