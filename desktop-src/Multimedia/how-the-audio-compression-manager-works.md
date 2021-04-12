---
title: Cómo funciona el administrador de compresión de audio
description: Cómo funciona el administrador de compresión de audio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimedia, administrador de compresión de audio (ACM)
- audio, administrador de compresión de audio (ACM)
- Administrador de compresión de audio (ACM), acerca de
- ACM (Administrador de compresión de audio), acerca de
- Administrador de compresión de audio (ACM), controladores de códecs
- ACM (Administrador de compresión de audio), controladores de códecs
- Administrador de compresión de audio (ACM), controladores de convertidor de formato
- ACM (Administrador de compresión de audio), controladores de convertidor de formato
- Administrador de compresión de audio (ACM), controladores de filtro
- ACM (Administrador de compresión de audio), controladores de filtro
- Administrador de compresión de audio (ACM), controladores de compresores
- ACM (Administrador de compresión de audio), controladores de compresores
- Administrador de compresión de audio (ACM), controladores de descompresor
- ACM (Administrador de compresión de audio), controladores de descompresor
- Controladores de códecs
- Controladores de convertidor de formato
- Controladores de filtro
- Controladores de compresores
- Controladores de descompresor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357253"
---
# <a name="how-the-audio-compression-manager-works"></a><span data-ttu-id="04d37-122">Cómo funciona el administrador de compresión de audio</span><span class="sxs-lookup"><span data-stu-id="04d37-122">How the Audio Compression Manager Works</span></span>

<span data-ttu-id="04d37-123">ACM usa enlaces de interfaz de controlador existentes para invalidar el algoritmo de asignación predeterminado para dispositivos de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="04d37-123">The ACM uses existing driver interface hooks to override the default mapping algorithm for waveform-audio devices.</span></span> <span data-ttu-id="04d37-124">Esto permite a ACM interceptar las llamadas de apertura del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04d37-124">This allows the ACM to intercept device-open calls.</span></span> <span data-ttu-id="04d37-125">Una vez interceptada una llamada, el ACM puede realizar una serie de tareas para procesar los datos de audio, como insertar un compresor externo o descompresor en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="04d37-125">After a call has been intercepted, the ACM can perform a variety of tasks to process the audio data, such as inserting an external compressor or decompressor into the sequence.</span></span>

<span data-ttu-id="04d37-126">ACM administra los siguientes tipos de controladores:</span><span class="sxs-lookup"><span data-stu-id="04d37-126">The ACM manages the following types of drivers:</span></span>

-   <span data-ttu-id="04d37-127">Controladores de compresor y descompresor (codec)</span><span class="sxs-lookup"><span data-stu-id="04d37-127">Compressor and decompressor (codec) drivers</span></span>
-   <span data-ttu-id="04d37-128">Controladores de convertidor de formato</span><span class="sxs-lookup"><span data-stu-id="04d37-128">Format converter drivers</span></span>
-   <span data-ttu-id="04d37-129">Controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="04d37-129">Filter drivers</span></span>

<span data-ttu-id="04d37-130">Los compresores y descompresores cambian un tipo de formato a otro.</span><span class="sxs-lookup"><span data-stu-id="04d37-130">Compressors and decompressors change one format type to another.</span></span> <span data-ttu-id="04d37-131">Por ejemplo, un compresor o descompresor puede cambiar un archivo PCM (modulación por pulsos de código) a un archivo ADPCM (modulación de código de impulso diferencial adaptativo).</span><span class="sxs-lookup"><span data-stu-id="04d37-131">For example, a compressor or decompressor can change a PCM (Pulse Code Modulation) file to an ADPCM (Adaptive Differential Pulse Code Modulation) file.</span></span> <span data-ttu-id="04d37-132">Los convertidores de formato cambian el formato, pero no el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="04d37-132">Format converters change the format, but not the data type.</span></span> <span data-ttu-id="04d37-133">Por ejemplo, un convertidor puede cambiar los datos de 44 kHz de 16 bits a los datos de 8 bits a 44-kHz.</span><span class="sxs-lookup"><span data-stu-id="04d37-133">For example, a converter can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span> <span data-ttu-id="04d37-134">Los filtros no cambian el formato de los datos, pero cambian los datos de audio de forma de onda de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="04d37-134">Filters do not change the data format at all, but they change the waveform-audio data in some manner.</span></span> <span data-ttu-id="04d37-135">Por ejemplo, un filtro podría combinar un flujo de datos y un eco de sí mismo.</span><span class="sxs-lookup"><span data-stu-id="04d37-135">For example, a filter could combine a data stream and an echo of itself.</span></span> <span data-ttu-id="04d37-136">Un solo controlador ACM, una etiqueta de filtro o una etiqueta de formato dentro de un controlador, podrían admitir también combinaciones de los tipos anteriores.</span><span class="sxs-lookup"><span data-stu-id="04d37-136">A single ACM driver, or a filter tag or format tag within a driver, might also support combinations of the preceding types.</span></span>

<span data-ttu-id="04d37-137">En el caso de la salida de audio de forma de onda, ACM pasa cada búfer de datos al convertidor cuando llega.</span><span class="sxs-lookup"><span data-stu-id="04d37-137">For waveform-audio output, the ACM passes each buffer of data to the converter as it arrives.</span></span> <span data-ttu-id="04d37-138">El convertidor descomprime los datos y devuelve los datos descomprimidos a ACM en un búfer "Shadow".</span><span class="sxs-lookup"><span data-stu-id="04d37-138">The converter decompresses the data and returns the decompressed data to the ACM in a "shadow" buffer.</span></span> <span data-ttu-id="04d37-139">A continuación, ACM pasa el búfer de instantáneas descomprimidos al controlador de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="04d37-139">The ACM then passes the decompressed shadow buffer to the waveform-audio driver.</span></span> <span data-ttu-id="04d37-140">El ACM asigna los búferes de instantáneas cada vez que recibe un mensaje de preparación.</span><span class="sxs-lookup"><span data-stu-id="04d37-140">The ACM allocates the shadow buffers whenever it receives a prepare message.</span></span>

<span data-ttu-id="04d37-141">En el caso de la entrada de audio de onda, ACM pasa búferes de instantáneas vacíos al controlador.</span><span class="sxs-lookup"><span data-stu-id="04d37-141">For waveform-audio input, the ACM passes empty shadow buffers to the driver.</span></span> <span data-ttu-id="04d37-142">Usa una tarea en segundo plano para recibir una notificación una vez que el controlador ha rellenado el búfer de sombra.</span><span class="sxs-lookup"><span data-stu-id="04d37-142">It uses a background task to receive a notification after the driver has filled the shadow buffer.</span></span> <span data-ttu-id="04d37-143">A continuación, el ACM pasa los búferes al controlador para la compresión.</span><span class="sxs-lookup"><span data-stu-id="04d37-143">The ACM then passes the buffers to the driver for compression.</span></span> <span data-ttu-id="04d37-144">Una vez finalizada la compresión, el controlador pasa los datos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04d37-144">After compression is finished, the driver passes the data to the application.</span></span>

 

 




