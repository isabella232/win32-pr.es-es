---
title: Escribir flujos con píxeles no cuadrados
description: Escribir flujos con píxeles no cuadrados
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- SDK de Windows Media Format, escribir secuencias de vídeo
- SDK de Windows Media Format, secuencias de vídeo
- SDK de Windows Media Format, píxeles no cuadrados
- Windows Media Format SDK, píxeles (no cuadrado)
- Advanced Systems Format (ASF), escribir secuencias de vídeo
- ASF (formato de sistemas avanzados), escribir secuencias de vídeo
- Advanced Systems Format (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Advanced Systems Format (ASF), píxeles no cuadrados
- ASF (formato de sistemas avanzados), píxeles no cuadrados
- Advanced Systems Format (ASF), píxeles (no cuadrados)
- ASF (formato de sistemas avanzados), píxeles (no cuadrados)
- escribir secuencias de vídeo
- secuencias de vídeo, escritura
- secuencias de vídeo, píxeles no cuadrados
- píxeles no cuadrados
- píxeles (no cuadrados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077309"
---
# <a name="writing-streams-with-non-square-pixels"></a><span data-ttu-id="c6bd7-120">Escribir flujos con píxeles no cuadrados</span><span class="sxs-lookup"><span data-stu-id="c6bd7-120">Writing Streams with Non-Square Pixels</span></span>

<span data-ttu-id="c6bd7-121">Hay dos formas de crear secuencias de vídeo con píxeles no cuadrados que se mostrarán correctamente en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-121">There are two ways to create video streams with non-square pixels that will be displayed correctly in Windows Media Player.</span></span> <span data-ttu-id="c6bd7-122">La primera técnica implica establecer los atributos de nivel de flujo en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-122">The first technique involves setting stream-level attributes in the file header.</span></span> <span data-ttu-id="c6bd7-123">La segunda técnica implica agregar una extensión de unidad de datos a una secuencia en el perfil y, a continuación, establecer un valor para ella en cada ejemplo que se escribe.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-123">The second technique involves adding a data unit extension to a stream in the profile, and then setting a value for it in every sample that is written.</span></span>

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a><span data-ttu-id="c6bd7-124">Para usar los atributos de encabezado de nivel de secuencia para establecer la relación de aspecto de píxeles</span><span class="sxs-lookup"><span data-stu-id="c6bd7-124">To Use Stream-level Header Attributes to Set Pixel Aspect Ratio</span></span>

1.  <span data-ttu-id="c6bd7-125">Configure el objeto de escritor.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-125">Set up the writer object.</span></span> <span data-ttu-id="c6bd7-126">Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="c6bd7-126">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="c6bd7-127">Cree o cargue un perfil con una o varias secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-127">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="c6bd7-128">Para obtener más información, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="c6bd7-128">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="c6bd7-129">Llame a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="c6bd7-129">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span> <span data-ttu-id="c6bd7-130">(Llame siempre a este método antes de establecer los atributos de encabezado).</span><span class="sxs-lookup"><span data-stu-id="c6bd7-130">(Always call this method before setting any header attributes.)</span></span>
4.  <span data-ttu-id="c6bd7-131">Llame a **QueryInterface** para obtener la interfaz [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) y llame al método [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) dos veces para agregar [**AspectRatioX**](aspectratiox.md) y [**AspectRatioY**](aspectratioy.md) como atributos de nivel de secuencia de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-131">Call **QueryInterface** to obtain the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface and call [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) twice to add [**AspectRatioX**](aspectratiox.md) and [**AspectRatioY**](aspectratioy.md) as stream-level attributes of the video stream.</span></span> <span data-ttu-id="c6bd7-132">Estos atributos son valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c6bd7-132">These attributes are **DWORD** values.</span></span>
5.  <span data-ttu-id="c6bd7-133">Escriba el archivo.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-133">Write the file.</span></span>

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a><span data-ttu-id="c6bd7-134">Para usar las extensiones de unidad de datos para establecer la relación de aspecto de píxeles</span><span class="sxs-lookup"><span data-stu-id="c6bd7-134">To Use Data Unit Extensions to Set Pixel Aspect Ratio</span></span>

<span data-ttu-id="c6bd7-135">**Antes de escribir:**</span><span class="sxs-lookup"><span data-stu-id="c6bd7-135">**Before writing:**</span></span>

1.  <span data-ttu-id="c6bd7-136">Configure el objeto de escritor.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-136">Set up the writer object.</span></span> <span data-ttu-id="c6bd7-137">Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="c6bd7-137">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="c6bd7-138">Cree o cargue un perfil con una o varias secuencias de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-138">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="c6bd7-139">Para obtener más información, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="c6bd7-139">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="c6bd7-140">Para cada secuencia (de cualquier tipo de medio) del perfil, llame a [**IWMStreamConfig:: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) para especificar un nombre único de su elección.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-140">For each stream (of any media type) in the profile, call [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) to specify a unique name of your choice.</span></span> <span data-ttu-id="c6bd7-141">No asigne a dos secuencias el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-141">Do not give two streams the same name.</span></span>
4.  <span data-ttu-id="c6bd7-142">Use [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) en el flujo de vídeo para agregar una extensión de unidad de datos para la relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-142">Use [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) on the video stream to add a data unit extension for pixel aspect ratio.</span></span>
5.  <span data-ttu-id="c6bd7-143">Llame a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="c6bd7-143">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>
6.  <span data-ttu-id="c6bd7-144">Escriba el archivo.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-144">Write the file.</span></span>

<span data-ttu-id="c6bd7-145">**Al escribir:**</span><span class="sxs-lookup"><span data-stu-id="c6bd7-145">**While writing:**</span></span>

-   <span data-ttu-id="c6bd7-146">Para cada ejemplo, llame a [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) y especifique la \_ propiedad WM SampleExtensionGUID \_ PixelAspectRatio junto con el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-146">For each sample, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) and specify the WM\_SampleExtensionGUID\_PixelAspectRatio property along with the correct value.</span></span> <span data-ttu-id="c6bd7-147">Los valores de relación de aspecto se escriben como dos valores concatenados de dos dígitos.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-147">Aspect ratio values are written as two concatenated two-digit values.</span></span> <span data-ttu-id="c6bd7-148">Por ejemplo, 16:9 se escribe como 1609 o 0x0649.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-148">For example, 16:9 is written as 1609 or 0x0649.</span></span> <span data-ttu-id="c6bd7-149">Siempre es un valor de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="c6bd7-149">This is always a 2-byte value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6bd7-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6bd7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6bd7-151">**Para leer y escribir secuencias de vídeo con píxeles no cuadrados**</span><span class="sxs-lookup"><span data-stu-id="c6bd7-151">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




