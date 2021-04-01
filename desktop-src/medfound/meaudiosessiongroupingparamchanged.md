---
description: Lo genera el representador de audio cuando cambian los parámetros de agrupación para la sesión de audio.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Evento MEAudioSessionGroupingParamChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac115bb30a4c01247da537f3255e9bc40099e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275646"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a><span data-ttu-id="714c5-103">Evento MEAudioSessionGroupingParamChanged</span><span class="sxs-lookup"><span data-stu-id="714c5-103">MEAudioSessionGroupingParamChanged event</span></span>

<span data-ttu-id="714c5-104">Lo genera el representador de audio cuando cambian los parámetros de agrupación para la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="714c5-104">Raised by the audio renderer when the grouping parameters change for the audio session.</span></span>

<span data-ttu-id="714c5-105">La sesión multimedia reenvía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="714c5-105">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="714c5-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="714c5-106">Event values</span></span>

<span data-ttu-id="714c5-107">Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="714c5-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="714c5-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="714c5-108">VARTYPE</span></span>                | <span data-ttu-id="714c5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="714c5-109">Description</span></span>                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="714c5-110">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="714c5-110">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="714c5-111">Puntero a la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .</span><span class="sxs-lookup"><span data-stu-id="714c5-111">Pointer to the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="714c5-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="714c5-112">Remarks</span></span>

<span data-ttu-id="714c5-113">El receptor de flujo del representador de audio envía este evento.</span><span class="sxs-lookup"><span data-stu-id="714c5-113">This event is sent by the audio renderer's stream sink.</span></span> <span data-ttu-id="714c5-114">El evento se desencadena cuando el representador de audio recibe un evento [**IAudioSessionEvents:: OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) de la sesión de audio.</span><span class="sxs-lookup"><span data-stu-id="714c5-114">The event is triggered when the audio renderer receives an [**IAudioSessionEvents::OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) event from the audio session.</span></span>

<span data-ttu-id="714c5-115">Para obtener los nuevos parámetros de agrupación, llame a [**IMFAudioPolicy:: GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span><span class="sxs-lookup"><span data-stu-id="714c5-115">To get the new grouping parameters, call [**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).</span></span>

## <a name="requirements"></a><span data-ttu-id="714c5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="714c5-116">Requirements</span></span>



| <span data-ttu-id="714c5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="714c5-117">Requirement</span></span> | <span data-ttu-id="714c5-118">Value</span><span class="sxs-lookup"><span data-stu-id="714c5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="714c5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="714c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="714c5-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="714c5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="714c5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="714c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="714c5-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="714c5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="714c5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="714c5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="714c5-124"><dt>Mfobjects. h (incluye Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="714c5-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="714c5-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="714c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="714c5-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="714c5-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="714c5-127">**IMFAudioPolicy::GetGroupingParam**</span><span class="sxs-lookup"><span data-stu-id="714c5-127">**IMFAudioPolicy::GetGroupingParam**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[<span data-ttu-id="714c5-128">Representador de audio de streaming</span><span class="sxs-lookup"><span data-stu-id="714c5-128">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
