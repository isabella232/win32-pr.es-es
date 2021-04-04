---
title: Para Desentrelazar vídeo
description: Para Desentrelazar vídeo
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- SDK de Windows Media Format, vídeo desentrelazado
- Windows Media Format SDK, Telecine inverso
- SDK de Windows Media Format, telecine
- Advanced Systems Format (ASF), vídeo desentrelazado
- ASF (formato de sistemas avanzados), vídeo desentrelazado
- Advanced Systems Format (ASF), Telecine inverso
- ASF (formato de sistemas avanzados), Telecine inverso
- Advanced Systems Format (ASF), telecine
- ASF (formato de sistemas avanzados), telecine
- vídeo desentrelazado
- Telecine inverso, acerca de
- Telecine, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077330"
---
# <a name="to-deinterlace-video"></a><span data-ttu-id="4cf3e-115">Para Desentrelazar vídeo</span><span class="sxs-lookup"><span data-stu-id="4cf3e-115">To Deinterlace Video</span></span>

<span data-ttu-id="4cf3e-116">Algunos orígenes de vídeo, como las tarjetas de captura de vídeo, proporcionan datos de vídeo para la visualización entrelazada.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-116">Some sources of video, such as video capture cards, deliver video data for interlaced display.</span></span> <span data-ttu-id="4cf3e-117">Cada fotograma de vídeo entrelazado se compone de dos campos.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-117">Each frame of interlaced video is made up of two fields.</span></span> <span data-ttu-id="4cf3e-118">El campo superior contiene la primera línea de vídeo y todas las demás líneas a partir de entonces.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-118">The top field contains the first line of video and every other line thereafter.</span></span> <span data-ttu-id="4cf3e-119">El campo inferior contiene la segunda línea de vídeo y todas las demás líneas posteriores.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-119">The bottom field contains the second line of video and every other line thereafter.</span></span> <span data-ttu-id="4cf3e-120">Por lo tanto, un campo contiene todas las líneas pares y la otra contiene todas las líneas con número impar.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-120">So one field contains all of the even numbered lines and the other contains all of the odd numbered lines.</span></span> <span data-ttu-id="4cf3e-121">Los campos que componen un fotograma representan tiempos de presentación ligeramente diferentes, de modo que, cuando se intercalan, no forman una imagen estática.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-121">The fields that make up a frame represent slightly different presentation times so that, when interleaved, they do not form a static image.</span></span>

<span data-ttu-id="4cf3e-122">Si desea mostrar vídeo en un monitor de equipo, cada fotograma del vídeo debe mostrarse como una imagen (este método de visualización de vídeo de un fotograma completo a la vez se denomina vídeo *progresivo* ). Si muestra vídeo entrelazado progresivamente, es posible que los fotogramas no tengan el aspecto correcto, debido a la diferencia de tiempo entre los dos campos.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-122">When you want to display video on a computer monitor, each frame of the video should be displayed as one image (this method of displaying video one whole frame at a time is called *progressive* video.) If you display interlaced video progressively, the frames may not look right, because of the time difference between the two fields.</span></span> <span data-ttu-id="4cf3e-123">El códec de Windows Media Video y el códec de perfil avanzado de Windows Media Video admiten una característica de preprocesamiento que convierte el contenido entrelazado en fotogramas progresivos.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-123">The Windows Media Video codec and the Windows Media Video Advanced Profile codec both support a preprocessing feature that converts interlaced content into progressive frames.</span></span>

<span data-ttu-id="4cf3e-124">Para que el vídeo de entrada desentrelazado de códecs, llame al método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) .</span><span class="sxs-lookup"><span data-stu-id="4cf3e-124">To have the codec deinterlace input video, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method.</span></span> <span data-ttu-id="4cf3e-125">La configuración que se va a usar es g \_ wszDeinterlaceMode.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-125">The setting to use is g\_wszDeinterlaceMode.</span></span> <span data-ttu-id="4cf3e-126">Establezca el modo de desentrelazado en uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-126">Set the deinterlacing mode to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cf3e-127">Value</span><span class="sxs-lookup"><span data-stu-id="4cf3e-127">Value</span></span></th>
<th><span data-ttu-id="4cf3e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cf3e-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cf3e-129">WM_DM_NOTINTERLACED</span><span class="sxs-lookup"><span data-stu-id="4cf3e-129">WM_DM_NOTINTERLACED</span></span></td>
<td><span data-ttu-id="4cf3e-130">La entrada es progresiva.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-130">Input is progressive.</span></span> <span data-ttu-id="4cf3e-131">Use esta opción para detener el desentrelazado cuando haya establecido previamente el modo de desentrelazado en otro valor.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-131">Use this setting to stop deinterlacing when you have previously set the deinterlacing mode to another value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cf3e-132">WM_DM_DEINTERLACE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="4cf3e-132">WM_DM_DEINTERLACE_NORMAL</span></span></td>
<td><span data-ttu-id="4cf3e-133">Seleccione este modo para mezclar los campos pares e impares de un fotograma entrelazado (mediante un mecanismo de compensación de movimiento). Privilegios</span><span class="sxs-lookup"><span data-stu-id="4cf3e-133">Select this mode to blend the even and odd fields of an interlaced frame (using a motion compensation mechanism).Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="4cf3e-134">Los artefactos entrelazados de la pantalla progresiva se reducen significativamente.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-134">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
<li><span data-ttu-id="4cf3e-135">El códec de Windows Media Video produce un vídeo comprimido de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-135">The Windows Media Video codec produces higher quality compressed video.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cf3e-136">WM_DM_DEINTERLACE_HALFSIZE</span><span class="sxs-lookup"><span data-stu-id="4cf3e-136">WM_DM_DEINTERLACE_HALFSIZE</span></span></td>
<td><span data-ttu-id="4cf3e-137">Seleccione este modo cuando la resolución de salida sea la mitad o menos de la resolución de entrada.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-137">Select this mode when the output resolution is half, or less, of the input resolution.</span></span> <span data-ttu-id="4cf3e-138">Por ejemplo, use este modo cuando la resolución de vídeo de entrada sea 640 x 480 píxeles y la resolución de vídeo de salida sea de 320 x 240 píxeles. Privilegios</span><span class="sxs-lookup"><span data-stu-id="4cf3e-138">For example, use this mode when the input video resolution is 640 x 480 pixels and the output video resolution is 320 x 240 pixels.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="4cf3e-139">Los artefactos entrelazados de la pantalla progresiva se reducen significativamente.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-139">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cf3e-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="4cf3e-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="4cf3e-141">Seleccione este modo cuando la resolución de salida sea la mitad o menos de la resolución de entrada y la <a href="wmformat-glossary.md"><em>velocidad de fotogramas</em></a> de salida sea el doble de alta.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-141">Select this mode when the output resolution is half, or less, of the input resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="4cf3e-142">Por ejemplo, use este modo cuando la resolución de vídeo de entrada sea 640 x 480 píxeles en 30 fotogramas entrelazados/s y la resolución de vídeo de salida sea de 320 x 240 píxeles en 60 fotogramas/s. Privilegios</span><span class="sxs-lookup"><span data-stu-id="4cf3e-142">For example, use this mode when the input video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="4cf3e-143">Esto produce fotogramas progresivos de alta calidad, ya que cada campo se convierte en un fotograma y, por tanto, no es necesario mezclar ninguna información.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-143">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="4cf3e-144">Se captura el movimiento completo de los campos entrelazados.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-144">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cf3e-145">WM_DM_DEINTERLACE_INVERSETELECINE</span><span class="sxs-lookup"><span data-stu-id="4cf3e-145">WM_DM_DEINTERLACE_INVERSETELECINE</span></span></td>
<td><span data-ttu-id="4cf3e-146">Seleccione este modo para convertir el vídeo de 30 fotogramas/seg en los 24 fotogramas por segundo de la película original. Privilegios</span><span class="sxs-lookup"><span data-stu-id="4cf3e-146">Select this mode to convert telecined 30 frames/sec video into the 24 frames/sec of the original film.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="4cf3e-147">La calidad de compresión mejora significativamente porque solo es necesario codificar 24 fotogramas por segundo en lugar de 30 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-147">The compression quality improves significantly because only 24 frames/sec instead of 30 frames/sec need to be encoded.</span></span></li>
<li><span data-ttu-id="4cf3e-148">Dado que el resultado es progresivo, se realizan las mismas ventajas de compresión y visualización del desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-148">Because the result is progressive, the same compression and display benefits of deinterlacing are realized.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cf3e-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="4cf3e-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="4cf3e-150">Seleccione este modo cuando la resolución de salida vertical sea la mitad, o menos, de la resolución vertical de entrada y la <a href="wmformat-glossary.md"><em>velocidad de fotogramas</em></a> de salida sea dos veces superior.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-150">Select this mode when the vertical output resolution is half, or less, of the input vertical resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="4cf3e-151">Por ejemplo, la resolución de vídeo vertical de entrada es 640 x 480 píxeles en 30 fotogramas entrelazados/s y la resolución de vídeo vertical de salida es de 320 x 240 píxeles en 60 fotogramas/s. Privilegios</span><span class="sxs-lookup"><span data-stu-id="4cf3e-151">For example, the input vertical video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output vertical video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="4cf3e-152">Esto produce fotogramas progresivos de alta calidad, ya que cada campo se convierte en un fotograma y, por tanto, no es necesario mezclar ninguna información.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-152">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="4cf3e-153">Se captura el movimiento completo de los campos entrelazados.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-153">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4cf3e-154">En el caso de contenido mixto, establezca el modo de desentrelazado según sea necesario antes de pasar muestras de un nuevo tipo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-154">For mixed content, set the deinterlacing mode as needed before passing samples of a new type.</span></span> <span data-ttu-id="4cf3e-155">Por ejemplo, para iniciar la codificación con una entrada progresiva, no es necesario establecer ningún modo de desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-155">For example, to start encoding with progressive input, you don't need to set any deinterlacing mode.</span></span> <span data-ttu-id="4cf3e-156">Si algunos ejemplos requieren desentrelazado normal, debe establecer el modo de desentrelazado en WM \_ DM \_ desentrelazado \_ normal.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-156">If some samples then require normal deinterlacing, you must set the deinterlacing mode to WM\_DM\_DEINTERLACE\_NORMAL.</span></span> <span data-ttu-id="4cf3e-157">Para procesar más ejemplos progresivos, debe establecer el modo de desentrelazado en WM \_ DM \_ NOTINTERLACED.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-157">To then process additional progressive samples you must set the deinterlacing mode to WM\_DM\_NOTINTERLACED.</span></span>

## <a name="inverse-telecine-settings"></a><span data-ttu-id="4cf3e-158">Configuración de telecine inversa</span><span class="sxs-lookup"><span data-stu-id="4cf3e-158">Inverse Telecine Settings</span></span>

<span data-ttu-id="4cf3e-159">Para obtener una descripción de telecine inversa, consulte [para usar telecine inversa](to-use-inverse-telecine.md).</span><span class="sxs-lookup"><span data-stu-id="4cf3e-159">For a description of inverse telecine, see [To Use Inverse Telecine](to-use-inverse-telecine.md).</span></span>

<span data-ttu-id="4cf3e-160">Si establece el modo de desentrelazado en \_ INVERSETELECINE de WM DM \_ \_ , puede especificar el patrón de telecine del primer fotograma de entrada mediante una llamada a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="4cf3e-160">If you set the deinterlacing mode to WM\_DM\_DEINTERLACE\_INVERSETELECINE, you can specify the telecine pattern of the first input frame by calling the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="4cf3e-161">La configuración que se va a usar es g \_ wszInitialPatternForInverseTelecine.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-161">The setting to use is g\_wszInitialPatternForInverseTelecine.</span></span> <span data-ttu-id="4cf3e-162">Establezca el patrón inicial en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-162">Set the initial pattern to one of the following values.</span></span>



| <span data-ttu-id="4cf3e-163">Value</span><span class="sxs-lookup"><span data-stu-id="4cf3e-163">Value</span></span>                                              | <span data-ttu-id="4cf3e-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cf3e-164">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf3e-165">\_ \_ \_ deshabilitación del \_ \_ modo coherente de WM DM</span><span class="sxs-lookup"><span data-stu-id="4cf3e-165">WM\_DM\_IT\_DISABLE\_COHERENT\_MODE</span></span>                | <span data-ttu-id="4cf3e-166">Especifica que el medio de entrada ha pasado por el proceso de telecine, pero que los fotogramas ya no se encuentran en un patrón de predicción.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-166">Specifies that the input media has gone through the telecine process but that the frames are no longer in a predictable pattern.</span></span> <span data-ttu-id="4cf3e-167">Esto normalmente indica que el medio se editó después del procesamiento de telecine.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-167">This usually indicates that the media was edited after the telecine processing.</span></span> <span data-ttu-id="4cf3e-168">Cuando se usa esta opción, el códec intenta reconstruir los fotogramas originales por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-168">When you use this setting, the codec attempts to reconstruct the original frames on its own.</span></span> |
| <span data-ttu-id="4cf3e-169">\_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ AA \_</span><span class="sxs-lookup"><span data-stu-id="4cf3e-169">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_TOP</span></span>    | <span data-ttu-id="4cf3e-170">Especifica que el campo superior del marco AA es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-170">Specifies that the top field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="4cf3e-171">\_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ BB \_</span><span class="sxs-lookup"><span data-stu-id="4cf3e-171">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_TOP</span></span>    | <span data-ttu-id="4cf3e-172">Especifica que el campo superior del marco BB es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-172">Specifies that the top field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="4cf3e-173">\_ \_ \_ la primera trama de WM DM it \_ en el \_ \_ clip \_ es \_ BC \_ Top</span><span class="sxs-lookup"><span data-stu-id="4cf3e-173">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_TOP</span></span>    | <span data-ttu-id="4cf3e-174">Especifica que el campo superior del fotograma BC es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-174">Specifies that the top field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="4cf3e-175">\_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip es el \_ \_ CD \_ superior</span><span class="sxs-lookup"><span data-stu-id="4cf3e-175">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_TOP</span></span>    | <span data-ttu-id="4cf3e-176">Especifica que el campo superior del fotograma del CD es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-176">Specifies that the top field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="4cf3e-177">\_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es DD en la \_ \_ parte superior</span><span class="sxs-lookup"><span data-stu-id="4cf3e-177">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_TOP</span></span>    | <span data-ttu-id="4cf3e-178">Especifica que el campo superior del marco DD es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-178">Specifies that the top field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="4cf3e-179">\_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ AA \_ inferior</span><span class="sxs-lookup"><span data-stu-id="4cf3e-179">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_BOTTOM</span></span> | <span data-ttu-id="4cf3e-180">Especifica que el campo inferior del marco AA es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-180">Specifies that the bottom field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4cf3e-181">\_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es \_ BB \_ inferior</span><span class="sxs-lookup"><span data-stu-id="4cf3e-181">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_BOTTOM</span></span> | <span data-ttu-id="4cf3e-182">Especifica que el campo inferior del marco BB es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-182">Specifies that the bottom field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4cf3e-183">\_ \_ \_ \_ la primera trama \_ de \_ \_ \_ \_ WM DM</span><span class="sxs-lookup"><span data-stu-id="4cf3e-183">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_BOTTOM</span></span> | <span data-ttu-id="4cf3e-184">Especifica que el campo inferior del fotograma BC es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-184">Specifies that the bottom field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4cf3e-185">\_ \_ trama de WM \_ DM \_ en primer lugar en el \_ \_ clip es el \_ \_ CD \_ inferior</span><span class="sxs-lookup"><span data-stu-id="4cf3e-185">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_BOTTOM</span></span> | <span data-ttu-id="4cf3e-186">Especifica que el campo inferior del fotograma del CD es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-186">Specifies that the bottom field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4cf3e-187">\_ \_ \_ \_ la primera trama de WM DM en el \_ \_ clip \_ es DD de la \_ \_ parte inferior</span><span class="sxs-lookup"><span data-stu-id="4cf3e-187">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_BOTTOM</span></span> | <span data-ttu-id="4cf3e-188">Especifica que el campo inferior del marco DD es el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4cf3e-188">Specifies that the bottom field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="4cf3e-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4cf3e-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cf3e-190">**Temas avanzados**</span><span class="sxs-lookup"><span data-stu-id="4cf3e-190">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





