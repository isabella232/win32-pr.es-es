---
title: Para usar vídeo entrelazado
description: Para usar vídeo entrelazado
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- SDK de Windows Media Format, vídeo entrelazado
- SDK de Windows Media Format, codificación de vídeo entrelazada
- SDK de Windows Media Format, codificación de vídeo entrelazado
- SDK de Windows Media Format, descodificación de vídeo entrelazado
- SDK de Windows Media Format, orden de campo
- Advanced Systems Format (ASF), vídeo entrelazado
- ASF (formato de sistemas avanzados), vídeo entrelazado
- Advanced Systems Format (ASF), codificación de vídeo entrelazada
- ASF (formato de sistemas avanzados), codificación de vídeo entrelazada
- Advanced Systems Format (ASF), codificación de vídeo entrelazado
- ASF (formato de sistemas avanzados), vídeo entrelazado de codificación
- Advanced Systems Format (ASF), descodificación de vídeo entrelazado
- ASF (formato de sistemas avanzados), descodificación de vídeo entrelazado
- Advanced Systems Format (ASF), orden de campo
- ASF (formato de sistemas avanzados), orden de campo
- vídeo entrelazado, acerca de
- vídeo entrelazado, codificación
- vídeo entrelazado, descodificación
- vídeo entrelazado, orden de los campos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904408"
---
# <a name="to-use-interlaced-video"></a><span data-ttu-id="073f4-122">Para usar vídeo entrelazado</span><span class="sxs-lookup"><span data-stu-id="073f4-122">To Use Interlaced Video</span></span>

<span data-ttu-id="073f4-123">Hay dos tipos básicos de codificación de vídeo: progresiva y entrelazada.</span><span class="sxs-lookup"><span data-stu-id="073f4-123">There are two basic types of video encoding: progressive and interlaced.</span></span> <span data-ttu-id="073f4-124">En la codificación progresiva, cada fotograma es una representación codificada de un fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="073f4-124">In progressive encoding, each frame is an encoded representation of one frame of video.</span></span> <span data-ttu-id="073f4-125">En la codificación entrelazada, cada fotograma es una representación codificada de todas las filas de píxeles pares del vídeo o de todas las filas impares.</span><span class="sxs-lookup"><span data-stu-id="073f4-125">In interlaced encoding, each frame is an encoded representation of either all of the even rows of pixels in the video, or all of the odd rows.</span></span> <span data-ttu-id="073f4-126">Cada fotograma entrelazado se denomina *campo*, por lo que hay campos impares e incluso campos.</span><span class="sxs-lookup"><span data-stu-id="073f4-126">Each interlaced frame is called a *field*, so there are odd fields and even fields.</span></span> <span data-ttu-id="073f4-127">Una pantalla entrelazada (como un televisor) representa los campos de uno en uno, alternando los campos.</span><span class="sxs-lookup"><span data-stu-id="073f4-127">An interlaced display (like a television) renders the fields one at a time, alternating fields.</span></span> <span data-ttu-id="073f4-128">Una pantalla progresiva representa fotogramas a la vez.</span><span class="sxs-lookup"><span data-stu-id="073f4-128">A progressive display renders frames all at once.</span></span>

<span data-ttu-id="073f4-129">El códec de perfil avanzado de Windows Media Video 9 proporciona compatibilidad para mantener el entrelazado en secuencias comprimidas.</span><span class="sxs-lookup"><span data-stu-id="073f4-129">The Windows Media Video 9 Advanced Profile codec provides support for maintaining interlacing in compressed streams.</span></span>

## <a name="when-to-use-interlaced-video"></a><span data-ttu-id="073f4-130">Cuándo usar vídeo entrelazado</span><span class="sxs-lookup"><span data-stu-id="073f4-130">When to Use Interlaced Video</span></span>

<span data-ttu-id="073f4-131">El vídeo entrelazado de codificación solo es útil cuando el contenido se muestra en un dispositivo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="073f4-131">Encoding interlaced video is useful only when the content is displayed on an interlaced device.</span></span> <span data-ttu-id="073f4-132">Es posible que sea necesario entrelazar el contenido que se va a ver en un televisor (a través de un decodificador u otro dispositivo).</span><span class="sxs-lookup"><span data-stu-id="073f4-132">Content that is intended to be viewed on a television (through a set-top box or other device) may need to be interlaced.</span></span> <span data-ttu-id="073f4-133">El contenido que se va a ver exclusivamente en una pantalla del equipo no se debe codificar como entrelazado.</span><span class="sxs-lookup"><span data-stu-id="073f4-133">Content that is intended to be viewed exclusively on a computer display should not be encoded as interlaced.</span></span>

<span data-ttu-id="073f4-134">Para codificar vídeo entrelazado como vídeo progresivo, debe configurar los valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="073f4-134">To encode interlaced video as progressive video, you must configure input settings.</span></span> <span data-ttu-id="073f4-135">Para obtener más información, vea [para Desentrelazar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="073f4-135">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>

## <a name="field-order"></a><span data-ttu-id="073f4-136">Orden de campos</span><span class="sxs-lookup"><span data-stu-id="073f4-136">Field Order</span></span>

<span data-ttu-id="073f4-137">La mayoría de los orígenes de vídeo entrelazado, como las tarjetas de captura de vídeo, ofrecen ejemplos de vídeo que incluyen ambos campos intercalados entre sí.</span><span class="sxs-lookup"><span data-stu-id="073f4-137">Most sources of interlaced video, such as video capture cards, deliver video samples that include both fields interleaved with each other.</span></span> <span data-ttu-id="073f4-138">El resultado es como un marco completo de vídeo, con la excepción de que las líneas impares e impares se desplazan ligeramente en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="073f4-138">The result is like a complete frame of video, except that the odd and even lines are shifted slightly in time.</span></span> <span data-ttu-id="073f4-139">No hay ningún estándar universal en el que el campo de la muestra de vídeo intercalado se produce primero en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="073f4-139">There is no universal standard as to which field in the interleaved video sample occurs first in time.</span></span>

<span data-ttu-id="073f4-140">Debe permitir que los usuarios especifiquen el orden de los campos al pasar ejemplos entrelazados a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="073f4-140">You should enable users to specify field order when passing interlaced samples to your application.</span></span>

## <a name="encoding-interlaced-video"></a><span data-ttu-id="073f4-141">Vídeo entrelazado de codificación</span><span class="sxs-lookup"><span data-stu-id="073f4-141">Encoding Interlaced Video</span></span>

<span data-ttu-id="073f4-142">Para usar la codificación entrelazada, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="073f4-142">To use interlaced encoding, perform the following steps:</span></span>

1.  <span data-ttu-id="073f4-143">Configure la secuencia de vídeo en el perfil para usar la extensión de unidad de datos de tipo de contenido llamando al método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="073f4-143">Configure the video stream in the profile to use the content type data unit extension by calling the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method.</span></span> <span data-ttu-id="073f4-144">El GUID de la extensión de ejemplo para la extensión de tipo de contenido es de WM \_ SampleExtensionsGUID \_ ContentType.</span><span class="sxs-lookup"><span data-stu-id="073f4-144">The sample extension GUID for the content type extension is WM\_SampleExtensionsGUID\_ContentType.</span></span>
2.  <span data-ttu-id="073f4-145">Establezca la secuencia en el perfil y configure el escritor con el perfil como normal.</span><span class="sxs-lookup"><span data-stu-id="073f4-145">Set the stream in the profile and configure the writer with the profile as normal.</span></span>
3.  <span data-ttu-id="073f4-146">Antes de pasar ejemplos entrelazados al escritor, llame al método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para establecer el valor de \_ entrada g wszInterlacedCoding en **true**.</span><span class="sxs-lookup"><span data-stu-id="073f4-146">Before passing interlaced samples to the writer, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method to set the g\_wszInterlacedCoding input setting to **TRUE**.</span></span>
4.  <span data-ttu-id="073f4-147">Para cada ejemplo entrelazado que pase al escritor, llame al método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer el tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="073f4-147">For every interlaced sample that you pass to the writer, call the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the content type.</span></span> <span data-ttu-id="073f4-148">Los valores de tipo de contenido son combinaciones de las marcas de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="073f4-148">Content type values are combinations of the flags in the following table.</span></span>



| <span data-ttu-id="073f4-149">Marca</span><span class="sxs-lookup"><span data-stu-id="073f4-149">Flag</span></span>                         | <span data-ttu-id="073f4-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="073f4-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="073f4-151">WM \_ CT \_ entrelazado</span><span class="sxs-lookup"><span data-stu-id="073f4-151">WM\_CT\_INTERLACED</span></span>           | <span data-ttu-id="073f4-152">Establezca siempre esta marca al codificar contenido entrelazado.</span><span class="sxs-lookup"><span data-stu-id="073f4-152">Always set this flag when encoding interlaced content.</span></span> <span data-ttu-id="073f4-153">Si usa esta marca sin establecer primero una marca de orden de campo (primer campo de WM \_ CT \_ \_ \_ o primero el \_ campo de nivel superior de WM CT \_ ), \_ \_ el códec asumirá que el campo superior es el primero.</span><span class="sxs-lookup"><span data-stu-id="073f4-153">If you use this flag without setting a field-order flag (WM\_CT\_BOTTOM\_FIELD\_FIRST or WM\_CT\_TOP\_FIELD\_FIRST) the codec will assume that the top field is first.</span></span> <span data-ttu-id="073f4-154">Si el códec usa el orden de campo incorrecto, no debería haber ningún impacto en la calidad de la imagen, pero la eficacia de la codificación se verá afectada.</span><span class="sxs-lookup"><span data-stu-id="073f4-154">If the codec uses the wrong field order, there should be no impact on image quality, but the encoding efficiency will be affected.</span></span> |
| <span data-ttu-id="073f4-155">\_campo inferior CT de WM \_ \_ \_ primero</span><span class="sxs-lookup"><span data-stu-id="073f4-155">WM\_CT\_BOTTOM\_FIELD\_FIRST</span></span> | <span data-ttu-id="073f4-156">Cuando se combina con la \_ marca de WM CT \_ , este marcador indica que el campo inferior (el campo que comienza con la segunda línea del ejemplo) se produce primero en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="073f4-156">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the bottom field (the field starting with the second line in the sample) occurs first in time.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="073f4-157">\_ \_ \_ primer campo SUP CT \_</span><span class="sxs-lookup"><span data-stu-id="073f4-157">WM\_CT\_TOP\_FIELD\_FIRST</span></span>    | <span data-ttu-id="073f4-158">Cuando se combina con la \_ marca WM CT \_ , esta marca indica que el campo superior (el campo que comienza con la primera línea del ejemplo) se produce primero en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="073f4-158">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the top field (the field starting with the first line in the sample) occurs first in time.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="073f4-159">\_ \_ \_ primer campo de repetición CT de WM \_</span><span class="sxs-lookup"><span data-stu-id="073f4-159">WM\_CT\_REPEAT\_FIRST\_FIELD</span></span> | <span data-ttu-id="073f4-160">Indica que el primer campo del ejemplo debe repetirse en la reproducción.</span><span class="sxs-lookup"><span data-stu-id="073f4-160">Indicates that the first field in the sample should be repeated on playback.</span></span> <span data-ttu-id="073f4-161">Esta marca se usa para el vídeo que ha creado a partir de la película mediante el proceso de telecine. Si no se establece ninguna marca de orden de campo junto con esta marca, se supone que el campo superior se produce por primera vez.</span><span class="sxs-lookup"><span data-stu-id="073f4-161">This flag is used for video that has created from film by the telecine process.If no field-order flag is set in conjunction with this flag, the top field is assumed to occur first in time.</span></span><br/>                                                                             |



 

> [!Note]  
> <span data-ttu-id="073f4-162">Si \_ \_ no se establece la marca de WM CT, se supone que el ejemplo contiene un fotograma de vídeo progresivo.</span><span class="sxs-lookup"><span data-stu-id="073f4-162">If the WM\_CT\_INTERLACED flag is not set, the sample is assumed to contain a progressive video frame.</span></span>

 

## <a name="decoding-interlaced-video"></a><span data-ttu-id="073f4-163">Descodificación de vídeo entrelazado</span><span class="sxs-lookup"><span data-stu-id="073f4-163">Decoding Interlaced Video</span></span>

<span data-ttu-id="073f4-164">Al descodificar vídeo entrelazado, debe establecer el valor de g \_ wszAllowInterlacedOutput en **true** mediante el método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="073f4-164">When decoding interlaced video, you must set the g\_wszAllowInterlacedOutput setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="073f4-165">De lo contrario, el códec proporcionará tramas progresivas.</span><span class="sxs-lookup"><span data-stu-id="073f4-165">Otherwise the codec will deliver progressive frames.</span></span>

<span data-ttu-id="073f4-166">La extensión de unidad de datos de tipo de contenido se mantiene en los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="073f4-166">The content type data unit extension is maintained on the output samples.</span></span> <span data-ttu-id="073f4-167">Debe pasar la orientación del campo al dispositivo de representación para asegurarse de que la reproducción sea correcta.</span><span class="sxs-lookup"><span data-stu-id="073f4-167">You should pass the field orientation to the rendering device to ensure proper playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="073f4-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="073f4-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="073f4-169">**Temas avanzados**</span><span class="sxs-lookup"><span data-stu-id="073f4-169">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





