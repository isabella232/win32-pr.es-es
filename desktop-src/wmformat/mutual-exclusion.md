---
title: Exclusión mutua
description: Exclusión mutua
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- SDK de Windows Media Format, exclusión mutua
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- SDK de Windows Media Format, exclusión mutua de MBR
- Advanced Systems Format (ASF), exclusión mutua de MBR
- ASF (formato de sistemas avanzados), exclusión mutua de MBR
- Windows Media Format SDK, velocidad de bits múltiple (MBR)
- Advanced Systems Format (ASF), velocidad de bits múltiple (MBR)
- ASF (formato de sistemas avanzados), velocidad de bits múltiple (MBR)
- exclusión mutua, acerca de
- velocidad de bits múltiple (MBR), exclusión mutua
- MBR (velocidad de varios bits), exclusión mutua
- exclusión mutua, velocidad de bits
- exclusión mutua, lenguaje
- exclusión mutua, presentación
- exclusión mutua, desconocida
- exclusión mutua, características
- exclusión mutua, características avanzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903846"
---
# <a name="mutual-exclusion"></a><span data-ttu-id="22bff-121">Exclusión mutua</span><span class="sxs-lookup"><span data-stu-id="22bff-121">Mutual Exclusion</span></span>

<span data-ttu-id="22bff-122">Cada archivo ASF contiene una o más secuencias, cada una de las cuales contiene datos multimedia digitales.</span><span class="sxs-lookup"><span data-stu-id="22bff-122">Every ASF file contains one or more streams, each containing digital media data.</span></span> <span data-ttu-id="22bff-123">En circunstancias normales, cada flujo está asociado a una sola salida.</span><span class="sxs-lookup"><span data-stu-id="22bff-123">Under normal circumstances, each stream is associated with a single output.</span></span> <span data-ttu-id="22bff-124">En la reproducción, el objeto de lector proporciona ejemplos para cada salida.</span><span class="sxs-lookup"><span data-stu-id="22bff-124">On playback, the reader object delivers samples for each output.</span></span> <span data-ttu-id="22bff-125">Por lo tanto, de forma predeterminada, el lector entrega cada secuencia en un archivo ASF en la reproducción.</span><span class="sxs-lookup"><span data-stu-id="22bff-125">So, as a default, every stream in an ASF file is delivered by the reader on playback.</span></span>

<span data-ttu-id="22bff-126">Hay situaciones en las que no desea que cada flujo se entregue al cliente.</span><span class="sxs-lookup"><span data-stu-id="22bff-126">There are situations where you do not want every stream delivered to the client.</span></span> <span data-ttu-id="22bff-127">Por ejemplo, si crea un archivo de vídeo con cinco flujos de audio, uno para cada uno de los cinco idiomas, querrá que solo se entregue uno de ellos a la vez.</span><span class="sxs-lookup"><span data-stu-id="22bff-127">For example, if you create a video file with five audio streams, one for each of five languages, you want only one of them to be delivered at a time.</span></span> <span data-ttu-id="22bff-128">La exclusión mutua es una característica del SDK de Windows Media Format que le permite especificar un número de flujos mutuamente excluyentes que equivalen a la misma salida.</span><span class="sxs-lookup"><span data-stu-id="22bff-128">Mutual exclusion is a feature of the Windows Media Format SDK that enables you to specify a number of mutually exclusive streams that all equate to the same output.</span></span>

<span data-ttu-id="22bff-129">La exclusión mutua se define en el perfil que se usa para crear un archivo.</span><span class="sxs-lookup"><span data-stu-id="22bff-129">Mutual exclusion is defined in the profile used to create a file.</span></span> <span data-ttu-id="22bff-130">La exclusión mutua se configura en un perfil mediante el uso de objetos de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="22bff-130">You configure mutual exclusion in a profile by using mutual exclusion objects.</span></span> <span data-ttu-id="22bff-131">Las secuencias se agregan de una en una al objeto de exclusión mutua, se establece el tipo e incluyen el objeto en el perfil.</span><span class="sxs-lookup"><span data-stu-id="22bff-131">You add streams one at a time to the mutual exclusion object, set the type, and include the object in the profile.</span></span>

<span data-ttu-id="22bff-132">El SDK de Windows Media Format reconoce cuatro tipos de exclusión mutua:</span><span class="sxs-lookup"><span data-stu-id="22bff-132">The Windows Media Format SDK recognizes four types of mutual exclusion:</span></span>

-   <span data-ttu-id="22bff-133">Velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="22bff-133">Bit rate</span></span>
-   <span data-ttu-id="22bff-134">Idioma</span><span class="sxs-lookup"><span data-stu-id="22bff-134">Language</span></span>
-   <span data-ttu-id="22bff-135">Presentación</span><span class="sxs-lookup"><span data-stu-id="22bff-135">Presentation</span></span>
-   <span data-ttu-id="22bff-136">Unknown</span><span class="sxs-lookup"><span data-stu-id="22bff-136">Unknown</span></span>

## <a name="mutual-exclusion-by-bit-rate"></a><span data-ttu-id="22bff-137">Exclusión mutua por velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="22bff-137">Mutual Exclusion by Bit Rate</span></span>

<span data-ttu-id="22bff-138">La exclusión mutua de velocidad de bits es un tipo especial de exclusión mutua y se conoce más comúnmente como exclusión mutua de velocidad de bits múltiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="22bff-138">Bit rate mutual exclusion is a special type of mutual exclusion and is more commonly referred to as multiple bit rate (MBR) mutual exclusion.</span></span> <span data-ttu-id="22bff-139">Una exclusión mutua de MBR contiene un número de flujos que se originan a partir de la misma entrada, pero se codifican a velocidades de bits diferentes.</span><span class="sxs-lookup"><span data-stu-id="22bff-139">An MBR mutual exclusion contains a number of streams that all originate from the same input, but are encoded at different bit rates.</span></span> <span data-ttu-id="22bff-140">Al reproducir un archivo con MBR, el lector determina el mejor flujo que se va a usar en función del ancho de banda disponible.</span><span class="sxs-lookup"><span data-stu-id="22bff-140">When playing a file with MBR, the reader determines the best stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="22bff-141">El SDK de Windows Media Format admite MBR para secuencias de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="22bff-141">The Windows Media Format SDK supports MBR for audio and video streams.</span></span> <span data-ttu-id="22bff-142">El SDK también admite un tipo especial de vídeo MBR denominado Multiple video size MBR.</span><span class="sxs-lookup"><span data-stu-id="22bff-142">The SDK also supports a special type of MBR video called multiple video size MBR.</span></span> <span data-ttu-id="22bff-143">Esto es como el vídeo MBR normal, salvo que los flujos individuales pueden tener distintos tamaños de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="22bff-143">This is like normal MBR video except that the individual streams can have different frame sizes.</span></span> <span data-ttu-id="22bff-144">Por ejemplo, podría tener algunos flujos con el tamaño de vídeo de 320 x 240 predeterminado y otros con velocidades de bits más altas y un tamaño de vídeo de 640 x 480.</span><span class="sxs-lookup"><span data-stu-id="22bff-144">For example, you might have some streams at the default 320 x 240 video size and some others with higher bit rates and 640 x 480 video size.</span></span>

## <a name="mutual-exclusion-by-language"></a><span data-ttu-id="22bff-145">Exclusión mutua por idioma</span><span class="sxs-lookup"><span data-stu-id="22bff-145">Mutual Exclusion by Language</span></span>

<span data-ttu-id="22bff-146">La exclusión mutua basada en el lenguaje está diseñada para su uso con contenido (normalmente audio) registrado en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="22bff-146">Language-based mutual exclusion is designed for use with content (usually audio) recorded in several languages.</span></span> <span data-ttu-id="22bff-147">Una exclusión mutua basada en el lenguaje incluye varios flujos que se originan a partir de entradas únicas.</span><span class="sxs-lookup"><span data-stu-id="22bff-147">A language-based mutual exclusion includes several streams that originate from unique inputs.</span></span> <span data-ttu-id="22bff-148">Cada entrada es el mismo contenido, pero en un lenguaje diferente.</span><span class="sxs-lookup"><span data-stu-id="22bff-148">Each input is the same content, but in a different language.</span></span>

<span data-ttu-id="22bff-149">Para que la exclusión mutua esté en funcionamiento, la aplicación de lectura debe incluir lógica para seleccionar el idioma adecuado.</span><span class="sxs-lookup"><span data-stu-id="22bff-149">For mutual exclusion by language to work, the reading application must include logic to select the appropriate language.</span></span> <span data-ttu-id="22bff-150">Si escribe una aplicación para reproducir archivos ASF y desea admitir archivos con exclusión mutua basada en el idioma, debe seleccionar la secuencia adecuada antes de comenzar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="22bff-150">If you write an application to play ASF files, and you want to support files with language-based mutual exclusion, you should select the appropriate stream before beginning playback.</span></span>

## <a name="mutual-exclusion-by-presentation"></a><span data-ttu-id="22bff-151">Exclusión mutua por presentación</span><span class="sxs-lookup"><span data-stu-id="22bff-151">Mutual Exclusion by Presentation</span></span>

<span data-ttu-id="22bff-152">La exclusión mutua basada en la presentación se proporciona para admitir secuencias de vídeo que contienen el mismo contenido codificado con diferentes relaciones de aspecto.</span><span class="sxs-lookup"><span data-stu-id="22bff-152">Presentation-based mutual exclusion is provided to support video streams that contain the same content encoded with different aspect ratios.</span></span> <span data-ttu-id="22bff-153">Normalmente, se usa cuando se proporciona vídeo en una versión de pantalla panorámica (relación de aspecto 16:9), así como con formato para pantallas de televisión (relación de aspecto 4:3).</span><span class="sxs-lookup"><span data-stu-id="22bff-153">Typically, this is used when providing video in a letterbox version (aspect ratio 16:9) as well as formatted for television screens (aspect ratio 4:3).</span></span>

<span data-ttu-id="22bff-154">La selección de una presentación para la reproducción suele estar determinada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="22bff-154">The selection of a presentation for playback is most often determined by the user.</span></span> <span data-ttu-id="22bff-155">Si escribe una aplicación para reproducir archivos ASF y desea admitir archivos con exclusión mutua basada en la presentación, debe presentar al usuario la opción de seleccionar un tipo de presentación para su visualización.</span><span class="sxs-lookup"><span data-stu-id="22bff-155">If you write an application to play ASF files and want to support files with presentation based mutual exclusion, you should present the user with the option of selecting a presentation type for viewing.</span></span>

## <a name="unknown-mutual-exclusion"></a><span data-ttu-id="22bff-156">Exclusión mutua desconocida</span><span class="sxs-lookup"><span data-stu-id="22bff-156">Unknown Mutual Exclusion</span></span>

<span data-ttu-id="22bff-157">Puede crear una exclusión mutua en función de los criterios que desee.</span><span class="sxs-lookup"><span data-stu-id="22bff-157">You can create mutual exclusion based on any criteria you like.</span></span> <span data-ttu-id="22bff-158">Todos los tipos de exclusión mutua personalizados se deben crear con el tipo desconocido.</span><span class="sxs-lookup"><span data-stu-id="22bff-158">All custom mutual exclusion types should be created using the unknown type.</span></span>

## <a name="advanced-mutual-exclusion-features"></a><span data-ttu-id="22bff-159">Características avanzadas de exclusión mutua</span><span class="sxs-lookup"><span data-stu-id="22bff-159">Advanced Mutual Exclusion Features</span></span>

<span data-ttu-id="22bff-160">También puede usar la exclusión mutua para asignar secuencias a grupos que se excluyen mutuamente entre sí.</span><span class="sxs-lookup"><span data-stu-id="22bff-160">You can also use mutual exclusion to assign streams to groups that are mutually exclusive of one another.</span></span> <span data-ttu-id="22bff-161">Por ejemplo, puede que desee tener secuencias de audio en varios idiomas y asignar un flujo de vídeo diferente a cada una.</span><span class="sxs-lookup"><span data-stu-id="22bff-161">For example, you might want to have audio streams in multiple languages and assign a different video stream to each.</span></span> <span data-ttu-id="22bff-162">La exclusión mutua se usa para agrupar cada secuencia de audio con su secuencia de vídeo correspondiente y hacer que todos los grupos sean mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="22bff-162">You use mutual exclusion to group each audio stream with its corresponding video stream and make all groups mutually exclusive.</span></span>

<span data-ttu-id="22bff-163">El lector selecciona automáticamente las secuencias para todas las exclusiones mutuas.</span><span class="sxs-lookup"><span data-stu-id="22bff-163">The reader automatically selects streams for all mutual exclusions.</span></span> <span data-ttu-id="22bff-164">Para todos los tipos de exclusión mutua, excepto el MBR y la exclusión mutua basada en el lenguaje, el lector selecciona siempre la secuencia predeterminada, que es la primera secuencia que se agrega al objeto de exclusión mutua en el perfil.</span><span class="sxs-lookup"><span data-stu-id="22bff-164">For all types of mutual exclusion except MBR and language-based mutual exclusion, the reader always selects the default stream, which is the first stream added to the mutual exclusion object in the profile.</span></span> <span data-ttu-id="22bff-165">En el caso de MBR, el lector selecciona la secuencia que mejor se adapta al ancho de banda disponible en el momento de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="22bff-165">For MBR, the reader selects the stream that best suits the available bandwidth at the time of playback.</span></span> <span data-ttu-id="22bff-166">Si no desea usar el flujo predeterminado, puede establecer la selección de la secuencia en manual antes de empezar a leer un archivo.</span><span class="sxs-lookup"><span data-stu-id="22bff-166">If you do not want to use the default stream, you can set stream selection to manual before starting to read a file.</span></span>

<span data-ttu-id="22bff-167">La selección de secuencias manual se aplica a todo el archivo.</span><span class="sxs-lookup"><span data-stu-id="22bff-167">Manual stream selection applies to the entire file.</span></span> <span data-ttu-id="22bff-168">Pueden surgir dificultades si tiene exclusiones mutuas de diferentes tipos en el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="22bff-168">Difficulties can arise when you have mutual exclusions of different types in the same file.</span></span> <span data-ttu-id="22bff-169">Por ejemplo, un archivo puede contener la exclusión mutua basada en tasas de bits y la exclusión mutua personalizada.</span><span class="sxs-lookup"><span data-stu-id="22bff-169">For example, a file can contain both bit-rate-based mutual exclusion and custom mutual exclusion.</span></span> <span data-ttu-id="22bff-170">Para seleccionar una secuencia que no sea la predeterminada en la exclusión mutua personalizada, debe utilizar la selección de flujo manual.</span><span class="sxs-lookup"><span data-stu-id="22bff-170">To select a stream other than the default in the custom mutual exclusion, you must use manual stream selection.</span></span> <span data-ttu-id="22bff-171">Sin embargo, si usa la selección de flujo manual, el lector no seleccionará automáticamente el flujo de velocidad de bits múltiple.</span><span class="sxs-lookup"><span data-stu-id="22bff-171">If you use manual stream selection, however, the reader will not automatically select the multiple bit rate stream.</span></span> <span data-ttu-id="22bff-172">Debe planear esta eventualidad en la aplicación si tiene previsto admitir varios tipos de exclusiones mutuas en un único archivo.</span><span class="sxs-lookup"><span data-stu-id="22bff-172">You must plan for this eventuality in your application if you plan to support multiple types of mutual exclusion in a single file.</span></span> <span data-ttu-id="22bff-173">Normalmente esto significa la creación de sus propias rutinas de selección de secuencias para tipos de exclusión mutua normalmente automáticos.</span><span class="sxs-lookup"><span data-stu-id="22bff-173">Typically this means creating your own stream selection routines for normally automatic types of mutual exclusion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22bff-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22bff-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22bff-175">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="22bff-175">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="22bff-176">**Usar exclusión mutua**</span><span class="sxs-lookup"><span data-stu-id="22bff-176">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> </dl>

 

 




