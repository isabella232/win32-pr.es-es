---
title: Funciones de devolución de llamada AVICap
description: Funciones de devolución de llamada AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Clase AVICap, funciones de devolución de llamada
- Funciones de devolución de llamada AVICap, acerca de
- Mensaje WM_CAP_SET_CALLBACK_CAPCONTROL
- Mensaje WM_CAP_SET_CALLBACK_ERROR
- Mensaje WM_CAP_SET_CALLBACK_FRAME
- Mensaje WM_CAP_SET_CALLBACK_STATUS
- Mensaje WM_CAP_SET_CALLBACK_VIDEOSTREAM
- Mensaje WM_CAP_SET_CALLBACK_WAVESTREAM
- Mensaje WM_CAP_SET_CALLBACK_YIELD
- capSetCallbackOnCapControl (macro)
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame (macro)
- capSetCallbackOnStatus (macro)
- capSetCallbackOnVideoStream (macro)
- capSetCallbackOnWaveStream (macro)
- capSetCallbackOnYield (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994561"
---
# <a name="avicap-callback-functions"></a><span data-ttu-id="63712-119">Funciones de devolución de llamada AVICap</span><span class="sxs-lookup"><span data-stu-id="63712-119">AVICap Callback Functions</span></span>

<span data-ttu-id="63712-120">La aplicación puede registrar funciones de devolución de llamada con una ventana de captura para notificar a la aplicación cuando cambia el estado, cuando se produce un error, cuando los búferes de audio y fotogramas de vídeo están disponibles y para obtener resultados durante la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="63712-120">Your application can register callback functions with a capture window to have it notify your application when the status changes, when errors occur, when video frame and audio buffers become available, and to yield during streaming capture.</span></span> <span data-ttu-id="63712-121">Los siguientes mensajes establecen la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="63712-121">The following messages set the callback function.</span></span>



| <span data-ttu-id="63712-122">Message</span><span class="sxs-lookup"><span data-stu-id="63712-122">Message</span></span>                                                                        | <span data-ttu-id="63712-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="63712-123">Description</span></span>                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63712-124">**devolución de llamada de conjunto de Cap de WM \_ \_ \_ \_ CAPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="63712-124">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)   | <span data-ttu-id="63712-125">Especifica la función de devolución de llamada en la aplicación a la que se llama para proporcionar un control preciso sobre el inicio y el final de la captura.</span><span class="sxs-lookup"><span data-stu-id="63712-125">Specifies the callback function in the application called to give precise control over capture start and end.</span></span> <span data-ttu-id="63712-126">También puede usar la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63712-126">You can also use the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro to send this message.</span></span>                   |
| [<span data-ttu-id="63712-127">**\_error de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="63712-127">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)             | <span data-ttu-id="63712-128">Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="63712-128">Specifies the callback function in the application called when an error occurs.</span></span> <span data-ttu-id="63712-129">También puede usar la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63712-129">You can also use the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro to send this message.</span></span>                                                           |
| [<span data-ttu-id="63712-130">**\_marco de \_ devolución de llamada de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="63712-130">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)             | <span data-ttu-id="63712-131">Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se capturan los marcos de vista previa.</span><span class="sxs-lookup"><span data-stu-id="63712-131">Specifies the callback function in the application called when preview frames are captured.</span></span> <span data-ttu-id="63712-132">También puede usar la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63712-132">You can also use the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro to send this message.</span></span>                                               |
| [<span data-ttu-id="63712-133">**\_Estado de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="63712-133">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)           | <span data-ttu-id="63712-134">Especifica la función de devolución de llamada en la aplicación a la que se llama cuando cambia el estado.</span><span class="sxs-lookup"><span data-stu-id="63712-134">Specifies the callback function in the application called when the status changes.</span></span> <span data-ttu-id="63712-135">También puede usar la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63712-135">You can also use the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro to send this message.</span></span>                                                      |
| [<span data-ttu-id="63712-136">**\_secuencia de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="63712-136">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md) | <span data-ttu-id="63712-137">Especifica la función de devolución de llamada en la aplicación a la que se llama durante la captura de streaming cuando hay disponible un nuevo búfer de vídeo.</span><span class="sxs-lookup"><span data-stu-id="63712-137">Specifies the callback function in the application called during streaming capture when a new video buffer becomes available.</span></span> <span data-ttu-id="63712-138">También puede usar la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63712-138">You can also use the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro to send this message.</span></span> |
| [<span data-ttu-id="63712-139">**\_WAVESTREAM de \_ devolución de llamada del conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="63712-139">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)   | <span data-ttu-id="63712-140">Especifica la función de devolución de llamada en la aplicación a la que se llama durante la captura de streaming cuando un nuevo búfer de audio está disponible.</span><span class="sxs-lookup"><span data-stu-id="63712-140">Specifies the callback function in the application called during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="63712-141">También puede usar la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63712-141">You can also use the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro to send this message.</span></span>   |
| [<span data-ttu-id="63712-142">**\_rendimiento de \_ devolución de llamada de conjunto de Cap de \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="63712-142">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)             | <span data-ttu-id="63712-143">Especifica la función de devolución de llamada en la aplicación a la que se llama cuando se produce durante la captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="63712-143">Specifies the callback function in the application called when yielding during streaming capture.</span></span> <span data-ttu-id="63712-144">También puede usar la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) para enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="63712-144">You can also use the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro to send this message.</span></span>                                         |



 

<span data-ttu-id="63712-145">En los temas siguientes se describen las distintas funciones de devolución de llamada, las notificaciones enviadas a las funciones y sus usos.</span><span class="sxs-lookup"><span data-stu-id="63712-145">The following topics describe the different callback functions, the notifications sent to the functions, and their uses.</span></span>

 

 




