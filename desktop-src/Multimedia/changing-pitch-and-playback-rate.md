---
title: Cambiar la velocidad de reproducción y el tono
description: Cambiar la velocidad de reproducción y el tono
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- audio de una onda, paso
- 'onda: interfaz de audio, paso'
- audio de onda, velocidad de reproducción
- 'onda: interfaz de audio, velocidad de reproducción'
- audio de una onda, cambiar el tono
- 'onda: interfaz de audio, cambio de tono'
- audio de onda, cambio de velocidad de reproducción
- 'onda: interfaz de audio, cambio de velocidad de reproducción'
- cambiar la velocidad de reproducción de audio de onda
- cambiar onda-tono de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487723"
---
# <a name="changing-pitch-and-playback-rate"></a><span data-ttu-id="ddd60-113">Cambiar la velocidad de reproducción y el tono</span><span class="sxs-lookup"><span data-stu-id="ddd60-113">Changing Pitch and Playback Rate</span></span>

<span data-ttu-id="ddd60-114">Algunos dispositivos de salida de onda-audio pueden variar el paso y la velocidad de reproducción de los datos de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="ddd60-114">Some waveform-audio output devices can vary the pitch and the playback rate of waveform-audio data.</span></span> <span data-ttu-id="ddd60-115">No todos los dispositivos de audio de onda admiten cambios de tono y de velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="ddd60-115">Not all waveform-audio devices support pitch and playback-rate changes.</span></span> <span data-ttu-id="ddd60-116">Para obtener información sobre cómo determinar si un dispositivo de audio de forma de onda determinado admite cambios de velocidad y de reproducción, consulte [dispositivos y tipos de datos](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="ddd60-116">For information about how to determine whether a particular waveform-audio device supports pitch and playback rate changes, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="ddd60-117">Las diferencias entre cambiar el tono y la velocidad de reproducción son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ddd60-117">The differences between changing pitch and playback rate are as follows:</span></span>

-   <span data-ttu-id="ddd60-118">El controlador de dispositivo realiza el cambio de la velocidad de reproducción y no requiere hardware especializado.</span><span class="sxs-lookup"><span data-stu-id="ddd60-118">Changing the playback rate is performed by the device driver and does not require specialized hardware.</span></span> <span data-ttu-id="ddd60-119">La velocidad de muestra no cambia, pero el controlador se interpola omitiendo o sintetizando ejemplos.</span><span class="sxs-lookup"><span data-stu-id="ddd60-119">The sample rate is not changed, but the driver interpolates by skipping or synthesizing samples.</span></span> <span data-ttu-id="ddd60-120">Por ejemplo, si se cambia la velocidad de reproducción en un factor de dos, el controlador omite cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ddd60-120">For example, if the playback rate is changed by a factor of two, the driver skips every other sample.</span></span>
-   <span data-ttu-id="ddd60-121">Cambiar el tono requiere hardware especializado.</span><span class="sxs-lookup"><span data-stu-id="ddd60-121">Changing the pitch requires specialized hardware.</span></span> <span data-ttu-id="ddd60-122">La velocidad de reproducción y la velocidad de muestreo no cambian.</span><span class="sxs-lookup"><span data-stu-id="ddd60-122">The playback rate and sample rate are not changed.</span></span>

<span data-ttu-id="ddd60-123">Windows proporciona las siguientes funciones para consultar y establecer las frecuencias de reproducción y paso de audio y de onda.</span><span class="sxs-lookup"><span data-stu-id="ddd60-123">Windows provides the following functions to query and set waveform-audio pitch and playback rates.</span></span>



| <span data-ttu-id="ddd60-124">Función</span><span class="sxs-lookup"><span data-stu-id="ddd60-124">Function</span></span>                                                 | <span data-ttu-id="ddd60-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddd60-125">Description</span></span>                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ddd60-126">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="ddd60-126">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | <span data-ttu-id="ddd60-127">Recupera el tono para el dispositivo de salida de audio de onda especificado.</span><span class="sxs-lookup"><span data-stu-id="ddd60-127">Retrieves the pitch for the specified waveform-audio output device.</span></span>         |
| [<span data-ttu-id="ddd60-128">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="ddd60-128">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | <span data-ttu-id="ddd60-129">Recupera la velocidad de reproducción para el dispositivo de salida de audio de onda especificado.</span><span class="sxs-lookup"><span data-stu-id="ddd60-129">Retrieves the playback rate for the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="ddd60-130">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="ddd60-130">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | <span data-ttu-id="ddd60-131">Establece el tono para el dispositivo de salida de audio de onda especificado.</span><span class="sxs-lookup"><span data-stu-id="ddd60-131">Sets the pitch for the specified waveform-audio output device.</span></span>              |
| [<span data-ttu-id="ddd60-132">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="ddd60-132">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | <span data-ttu-id="ddd60-133">Establece la velocidad de reproducción para el dispositivo de salida de audio de onda especificado.</span><span class="sxs-lookup"><span data-stu-id="ddd60-133">Sets the playback rate for the specified waveform-audio output device.</span></span>      |



 

<span data-ttu-id="ddd60-134">Las tasas de paso y reproducción se cambian mediante un factor especificado con un número de punto fijo empaquetado en un valor de palabra.</span><span class="sxs-lookup"><span data-stu-id="ddd60-134">The pitch and playback rates are changed by a factor specified with a fixed-point number packed into a doubleword value.</span></span> <span data-ttu-id="ddd60-135">Los 16 bits superiores especifican la parte entera del número; los 16 bits inferiores especifican la parte fraccionaria.</span><span class="sxs-lookup"><span data-stu-id="ddd60-135">The upper 16 bits specify the integer part of the number; the lower 16 bits specify the fractional part.</span></span> <span data-ttu-id="ddd60-136">Por ejemplo, el valor 1,5 se representa como 0x00018000L.</span><span class="sxs-lookup"><span data-stu-id="ddd60-136">For example, the value 1.5 is represented as 0x00018000L.</span></span> <span data-ttu-id="ddd60-137">El valor 0,75 se representa como 0x0000C000L.</span><span class="sxs-lookup"><span data-stu-id="ddd60-137">The value 0.75 is represented as 0x0000C000L.</span></span> <span data-ttu-id="ddd60-138">Un valor de 1,0 (0x00010000) significa que el paso o la velocidad de reproducción no cambian.</span><span class="sxs-lookup"><span data-stu-id="ddd60-138">A value of 1.0 (0x00010000) means the pitch or playback rate is unchanged.</span></span>

 

 