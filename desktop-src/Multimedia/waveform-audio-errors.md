---
title: Errores de Waveform-Audio
description: Errores de Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Valores devueltos de MCIERR, errores de audio de onda
- referencia multimedia, errores de audio de onda
- referencia de errores de audio multimedia y de onda
- Interfaz de control de medios (MCI), errores de audio de onda
- MCI (interfaz de control multimedia), errores de audio de onda
- referencia de errores de audio y de onda
- Referencia de MCI, errores de audio de onda
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- onda-errores de audio
- 'Onda de onda de MCI: errores de audio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075317"
---
# <a name="waveform-audio-errors"></a><span data-ttu-id="4d3e9-116">Errores de Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="4d3e9-116">Waveform-Audio Errors</span></span>

<span data-ttu-id="4d3e9-117">Se definen los siguientes valores devueltos adicionales para los dispositivos de audio de onda de onda MCI:</span><span class="sxs-lookup"><span data-stu-id="4d3e9-117">The following additional return values are defined for MCI waveform-audio devices:</span></span>



| <span data-ttu-id="4d3e9-118">Value</span><span class="sxs-lookup"><span data-stu-id="4d3e9-118">Value</span></span>                             | <span data-ttu-id="4d3e9-119">Significado</span><span class="sxs-lookup"><span data-stu-id="4d3e9-119">Meaning</span></span>                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3e9-120">MCIERR \_ Wave \_ INPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-120">MCIERR\_WAVE\_INPUTSINUSE</span></span>         | <span data-ttu-id="4d3e9-121">Todos los dispositivos de forma de onda que pueden grabar archivos en el formato actual están en uso.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-121">All waveform devices that can record files in the current format are in use.</span></span> <span data-ttu-id="4d3e9-122">Espere hasta que uno de estos dispositivos sea gratuito; a continuación, vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-122">Wait until one of these devices is free; then, try again.</span></span>                              |
| <span data-ttu-id="4d3e9-123">MCIERR \_ Wave \_ INPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-123">MCIERR\_WAVE\_INPUTSUNSUITABLE</span></span>    | <span data-ttu-id="4d3e9-124">Ningún dispositivo de forma de onda instalado puede grabar archivos en el formato actual.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-124">No installed waveform device can record files in the current format.</span></span> <span data-ttu-id="4d3e9-125">Use la opción controladores del panel de control para instalar un dispositivo de grabación de forma de onda adecuado.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-125">Use the Drivers option from the Control Panel to install a suitable waveform recording device.</span></span> |
| <span data-ttu-id="4d3e9-126">MCIERR \_ Wave \_ INPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="4d3e9-126">MCIERR\_WAVE\_INPUTUNSPECIFIED</span></span>    | <span data-ttu-id="4d3e9-127">Puede especificar cualquier dispositivo de grabación de onda compatible.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-127">You can specify any compatible waveform recording device.</span></span>                                                                                                           |
| <span data-ttu-id="4d3e9-128">MCIERR \_ Wave \_ OUTPUTSINUSE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-128">MCIERR\_WAVE\_OUTPUTSINUSE</span></span>        | <span data-ttu-id="4d3e9-129">Todos los dispositivos de forma de onda que pueden reproducir archivos en el formato actual están en uso.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-129">All waveform devices that can play files in the current format are in use.</span></span> <span data-ttu-id="4d3e9-130">Espere hasta que uno de estos dispositivos sea gratuito; a continuación, vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-130">Wait until one of these devices is free; then, try again.</span></span>                                |
| <span data-ttu-id="4d3e9-131">MCIERR \_ Wave \_ OUTPUTSUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-131">MCIERR\_WAVE\_OUTPUTSUNSUITABLE</span></span>   | <span data-ttu-id="4d3e9-132">Ningún dispositivo de forma de onda instalado puede reproducir archivos en el formato actual.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-132">No installed waveform device can play files in the current format.</span></span> <span data-ttu-id="4d3e9-133">Use la opción controladores del panel de control para instalar un dispositivo de forma de onda adecuado.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-133">Use the Drivers option from the Control Panel to install a suitable waveform device.</span></span>             |
| <span data-ttu-id="4d3e9-134">MCIERR \_ Wave \_ OUTPUTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="4d3e9-134">MCIERR\_WAVE\_OUTPUTUNSPECIFIED</span></span>   | <span data-ttu-id="4d3e9-135">Puede especificar cualquier dispositivo de reproducción de onda de onda compatible.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-135">You can specify any compatible waveform playback device.</span></span>                                                                                                            |
| <span data-ttu-id="4d3e9-136">MCIERR \_ Wave \_ SETINPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-136">MCIERR\_WAVE\_SETINPUTINUSE</span></span>       | <span data-ttu-id="4d3e9-137">El dispositivo de forma de onda actual está en uso.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-137">The current waveform device is in use.</span></span> <span data-ttu-id="4d3e9-138">Espere hasta que el dispositivo sea gratuito; a continuación, vuelva a intentar establecer el dispositivo para la grabación.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-138">Wait until the device is free; then, try again to set the device for recording.</span></span>                                              |
| <span data-ttu-id="4d3e9-139">MCIERR \_ Wave \_ SETINPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-139">MCIERR\_WAVE\_SETINPUTUNSUITABLE</span></span>  | <span data-ttu-id="4d3e9-140">El dispositivo que está usando para grabar una forma de onda no puede reconocer el formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-140">The device you are using to record a waveform cannot recognize the data format.</span></span>                                                                                     |
| <span data-ttu-id="4d3e9-141">MCIERR \_ Wave \_ SETOUTPUTINUSE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-141">MCIERR\_WAVE\_SETOUTPUTINUSE</span></span>      | <span data-ttu-id="4d3e9-142">El dispositivo de forma de onda actual está en uso.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-142">The current waveform device is in use.</span></span> <span data-ttu-id="4d3e9-143">Espere hasta que el dispositivo sea gratuito; después, vuelva a intentar establecer el dispositivo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-143">Wait until the device is free; then, try again to set the device for playback.</span></span>                                               |
| <span data-ttu-id="4d3e9-144">MCIERR \_ Wave \_ SETOUTPUTUNSUITABLE</span><span class="sxs-lookup"><span data-stu-id="4d3e9-144">MCIERR\_WAVE\_SETOUTPUTUNSUITABLE</span></span> | <span data-ttu-id="4d3e9-145">El dispositivo que está usando para reproducir una forma de onda no puede reconocer el formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-145">The device you are using to playback a waveform cannot recognize the data format.</span></span>                                                                                   |



 

 

 




