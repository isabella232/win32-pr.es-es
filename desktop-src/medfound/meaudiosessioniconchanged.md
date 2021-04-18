---
description: Generado por el procesador de audio cuando cambia el icono de la sesión de audio.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Evento MEAudioSessionIconChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720406"
---
# <a name="meaudiosessioniconchanged-event"></a><span data-ttu-id="da323-103">Evento MEAudioSessionIconChanged</span><span class="sxs-lookup"><span data-stu-id="da323-103">MEAudioSessionIconChanged event</span></span>

<span data-ttu-id="da323-104">Generado por el procesador de audio cuando cambia el icono de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="da323-104">Raised by the audio renderer when the audio session icon changes.</span></span>

<span data-ttu-id="da323-105">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="da323-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="da323-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="da323-106">Event values</span></span>

<span data-ttu-id="da323-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="da323-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="da323-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="da323-108">VARTYPE</span></span>                | <span data-ttu-id="da323-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="da323-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="da323-110">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="da323-110">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="da323-111">Sin datos del evento.</span><span class="sxs-lookup"><span data-stu-id="da323-111">No event data.</span></span><br/> <br/>                                                     |
| <span data-ttu-id="da323-112">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="da323-112">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="da323-113">Puntero a la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="da323-113">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="da323-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da323-114">Remarks</span></span>

<span data-ttu-id="da323-115">El receptor de flujo del representador de audio envía este evento.</span><span class="sxs-lookup"><span data-stu-id="da323-115">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="da323-116">El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents:: OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="da323-116">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) event from the audio session.</span></span>

<span data-ttu-id="da323-117">Para obtener el nuevo icono, llame a [**IMFAudioPolicy:: GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span><span class="sxs-lookup"><span data-stu-id="da323-117">To get the new icon, call [**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).</span></span>

## <a name="requirements"></a><span data-ttu-id="da323-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da323-118">Requirements</span></span>



| <span data-ttu-id="da323-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da323-119">Requirement</span></span> | <span data-ttu-id="da323-120">Value</span><span class="sxs-lookup"><span data-stu-id="da323-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da323-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da323-121">Minimum supported client</span></span><br/> | <span data-ttu-id="da323-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da323-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da323-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da323-123">Minimum supported server</span></span><br/> | <span data-ttu-id="da323-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="da323-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da323-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da323-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="da323-126"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da323-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da323-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="da323-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da323-128">**IMFAudioPolicy::GetIconPath**</span><span class="sxs-lookup"><span data-stu-id="da323-128">**IMFAudioPolicy::GetIconPath**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[<span data-ttu-id="da323-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da323-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="da323-130">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="da323-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
