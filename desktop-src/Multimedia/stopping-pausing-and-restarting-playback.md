---
title: Detener, pausar y reiniciar la reproducción
description: Detener, pausar y reiniciar la reproducción
ms.assetid: 39751342-63bc-4e68-bf9e-38665db8a05c
keywords:
- audio de onda, Detener reproducción
- 'onda: interfaz de audio, Detener reproducción'
- reproducir los archivos de audio de onda, detener la reproducción
- audio de onda, pausar reproducción
- 'onda: interfaz de audio, pausar reproducción'
- reproducir archivos de audio de onda, pausar la reproducción
- audio de la onda, reinicio de la reproducción
- 'onda: interfaz de audio, reinicio de la reproducción'
- reproducir los archivos de audio de onda, reiniciando la reproducción
- waveOutPause función)
- waveOutReset función)
- waveOutRestart función)
- detención de la reproducción de audio de onda
- pausar la reproducción de onda-audio
- reinicio de la reproducción de onda-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6a4756a08317923056114259588a95bc62e97f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149199"
---
# <a name="stopping-pausing-and-restarting-playback"></a><span data-ttu-id="82ed8-118">Detener, pausar y reiniciar la reproducción</span><span class="sxs-lookup"><span data-stu-id="82ed8-118">Stopping, Pausing, and Restarting Playback</span></span>

<span data-ttu-id="82ed8-119">Puede detener o pausar la reproducción mientras se reproduce el audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="82ed8-119">You can stop or pause playback while waveform audio is playing.</span></span> <span data-ttu-id="82ed8-120">Una vez que se haya pausado la reproducción, puede reiniciarla.</span><span class="sxs-lookup"><span data-stu-id="82ed8-120">After playback has been paused, you can restart it.</span></span> <span data-ttu-id="82ed8-121">Windows proporciona las siguientes funciones para controlar la reproducción de audio de una onda.</span><span class="sxs-lookup"><span data-stu-id="82ed8-121">Windows provides the following functions for controlling waveform-audio playback.</span></span>



| <span data-ttu-id="82ed8-122">Función</span><span class="sxs-lookup"><span data-stu-id="82ed8-122">Function</span></span>                                 | <span data-ttu-id="82ed8-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ed8-123">Description</span></span>                                                                                 |
|------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82ed8-124">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="82ed8-124">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)     | <span data-ttu-id="82ed8-125">Pausa la reproducción en un dispositivo de salida de onda-audio.</span><span class="sxs-lookup"><span data-stu-id="82ed8-125">Pauses playback on a waveform-audio output device.</span></span>                                          |
| [<span data-ttu-id="82ed8-126">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="82ed8-126">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)     | <span data-ttu-id="82ed8-127">Detiene la reproducción en un dispositivo de salida de onda-audio y marca todos los bloques de datos pendientes como terminados.</span><span class="sxs-lookup"><span data-stu-id="82ed8-127">Stops playback on a waveform-audio output device and marks all pending data blocks as done.</span></span> |
| [<span data-ttu-id="82ed8-128">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="82ed8-128">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart) | <span data-ttu-id="82ed8-129">Reanuda la reproducción en un dispositivo de salida de audio de onda en pausa.</span><span class="sxs-lookup"><span data-stu-id="82ed8-129">Resumes playback on a paused waveform-audio output device.</span></span>                                  |



 

<span data-ttu-id="82ed8-130">Pausar un dispositivo de audio de forma de onda mediante [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) puede no ser instantáneo; el controlador puede acabar de reproducir el bloque actual antes de pausar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="82ed8-130">Pausing a waveform-audio device by using [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause) might not be instantaneous; the driver may finish playing the current block before pausing playback.</span></span>

<span data-ttu-id="82ed8-131">Generalmente, en cuanto se envía el primer bloque de datos de audio de forma de onda mediante la función [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) , el dispositivo de audio de forma de onda comienza a reproducirse.</span><span class="sxs-lookup"><span data-stu-id="82ed8-131">Generally, as soon as the first waveform-audio data block is sent by using the [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) function, the waveform-audio device begins playing.</span></span> <span data-ttu-id="82ed8-132">Si no desea que el sonido empiece a reproducirse inmediatamente, llame a **waveOutPause** antes de llamar a **waveOutWrite**.</span><span class="sxs-lookup"><span data-stu-id="82ed8-132">If you do not want the sound to start playing immediately, call **waveOutPause** before calling **waveOutWrite**.</span></span> <span data-ttu-id="82ed8-133">A continuación, cuando desee comenzar a reproducir datos de audio de onda, llame a [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span><span class="sxs-lookup"><span data-stu-id="82ed8-133">Then, when you want to begin playing waveform-audio data, call [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart).</span></span>

<span data-ttu-id="82ed8-134">No se puede usar **waveOutRestart** para reiniciar un dispositivo detenido con [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset). debe usar **waveOutWrite** para enviar el primer bloque de datos para reanudar la reproducción en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="82ed8-134">You cannot use **waveOutRestart** to restart a device that has been stopped with [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset); you must use **waveOutWrite** to send the first data block to resume playback on the device.</span></span>

 

 