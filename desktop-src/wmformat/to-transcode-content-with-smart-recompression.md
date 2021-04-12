---
title: Para transcodificar contenido con recompresión inteligente
description: Para transcodificar contenido con recompresión inteligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- SDK de Windows Media Format, transcodificación de contenido
- SDK de Windows Media Format, recompresión inteligente
- SDK de Windows Media Format, recompresión
- Windows Media Format SDK, códecs de Windows Media Audio
- Formato de sistemas avanzados (ASF), transcodificación de contenido
- ASF (formato de sistemas avanzados), transcodificar contenido
- Advanced Systems Format (ASF), recompresión inteligente
- ASF (formato de sistemas avanzados), recompresión inteligente
- Advanced Systems Format (ASF), recompresión
- ASF (formato de sistemas avanzados), recompresión
- Formatos de sistema avanzado (ASF), códecs de Windows Media Audio
- ASF (formato de sistemas avanzados), códecs de Windows Media Audio
- transcodificar contenido
- recompresión inteligente
- recompresión
- Códecs de Windows Media Audio, transcodificación de contenido
- códecs, códecs de Windows Media Audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358692"
---
# <a name="to-transcode-content-with-smart-recompression"></a><span data-ttu-id="e87a8-120">Para transcodificar contenido con recompresión inteligente</span><span class="sxs-lookup"><span data-stu-id="e87a8-120">To Transcode Content with Smart Recompression</span></span>

<span data-ttu-id="e87a8-121">Puede transcodificar contenido de una velocidad de bits a otra mediante el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="e87a8-121">You can transcode content from one bit rate to another using the Windows Media Format SDK.</span></span> <span data-ttu-id="e87a8-122">Normalmente, esto implica simplemente descodificar el contenido y codificarlo de nuevo a la velocidad de bits deseada.</span><span class="sxs-lookup"><span data-stu-id="e87a8-122">Normally, this involves simply decoding the content and encoding it again to the desired bit rate.</span></span> <span data-ttu-id="e87a8-123">El códec Windows Media Audio 9 admite la recompresión inteligente, que permite la transcodificación que consigue una mejor calidad que la normal.</span><span class="sxs-lookup"><span data-stu-id="e87a8-123">The Windows Media Audio 9 codec supports smart recompression, which enables transcoding that achieves better quality than normal.</span></span>

<span data-ttu-id="e87a8-124">Para la recompresión inteligente, la secuencia de audio original debe estar codificada con el códec Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="e87a8-124">For smart recompression, the original audio stream must be encoded with the Windows Media Audio codec.</span></span> <span data-ttu-id="e87a8-125">Se admiten todas las versiones del códec, pero no los códecs de audio especializados (Windows Media Audio 9 Professional y Windows Media Audio 9 Voice).</span><span class="sxs-lookup"><span data-stu-id="e87a8-125">All versions of the codec are supported, but the specialized audio codecs (Windows Media Audio 9 Professional and Windows Media Audio 9 Voice) are not.</span></span> <span data-ttu-id="e87a8-126">Si el audio original se ha codificado con el códec Windows Media Audio 9 Lossless, no es necesario utilizar la recompresión inteligente, ya que no se ha perdido información en la codificación original.</span><span class="sxs-lookup"><span data-stu-id="e87a8-126">If the original audio was encoded with the Windows Media Audio 9 Lossless codec, there is no need to use smart recompression, because no information was lost in the original encoding.</span></span>

<span data-ttu-id="e87a8-127">Para usar la recompresión inteligente, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="e87a8-127">To use smart recompression, perform the following steps.</span></span>

1.  <span data-ttu-id="e87a8-128">Configure un objeto de lector con el archivo de origen para leerlo.</span><span class="sxs-lookup"><span data-stu-id="e87a8-128">Set up a reader object with the source file for reading.</span></span> <span data-ttu-id="e87a8-129">Para obtener más información, consulte [leer archivos ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="e87a8-129">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="e87a8-130">Configure un objeto de escritor que se usará para transcodificar el archivo.</span><span class="sxs-lookup"><span data-stu-id="e87a8-130">Set up a writer object to use for transcoding the file.</span></span> <span data-ttu-id="e87a8-131">Establezca el nombre de archivo para el nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="e87a8-131">Set the file name for the new file.</span></span> <span data-ttu-id="e87a8-132">Seleccione un perfil para usarlo con el nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="e87a8-132">Select a profile to use for the new file.</span></span> <span data-ttu-id="e87a8-133">Establezca el perfil seleccionado en el objeto escritor.</span><span class="sxs-lookup"><span data-stu-id="e87a8-133">Set the selected profile in the writer object.</span></span> <span data-ttu-id="e87a8-134">Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="e87a8-134">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
3.  <span data-ttu-id="e87a8-135">Obtiene un puntero a la interfaz [**IWMProfile**](iwmprofile.md) del objeto lector llamando a **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e87a8-135">Get a pointer to the [**IWMProfile**](iwmprofile.md) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
4.  <span data-ttu-id="e87a8-136">Recupere la interfaz [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) para la secuencia de audio que se va a transcodificar mediante una llamada a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="e87a8-136">Retrieve the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface for the audio stream to be transcoded by calling [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span>
5.  <span data-ttu-id="e87a8-137">Obtenga la interfaz [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) para el objeto de configuración de flujo llamando a **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e87a8-137">Get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface for the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
6.  <span data-ttu-id="e87a8-138">Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para la secuencia realizando dos llamadas a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="e87a8-138">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="e87a8-139">Obtiene el tamaño de la estructura en la primera llamada y asigna memoria para un búfer que se va a pasar en la segunda llamada.</span><span class="sxs-lookup"><span data-stu-id="e87a8-139">Get the size of the structure on the first call, and allocate memory for a buffer to pass on the second call.</span></span>
7.  <span data-ttu-id="e87a8-140">Obtiene un puntero a la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para la entrada en el escritor llamando a [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="e87a8-140">Get a pointer to the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input in the writer by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
8.  <span data-ttu-id="e87a8-141">Obtenga la interfaz [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) para el objeto de las propiedades de los medios de entrada mediante una llamada a **IWMInputMediaProps:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e87a8-141">Get the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface for the input media properties object by calling **IWMInputMediaProps::QueryInterface**.</span></span>
9.  <span data-ttu-id="e87a8-142">Use el método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para establecer la \_ propiedad g wszOriginalWaveFormat.</span><span class="sxs-lookup"><span data-stu-id="e87a8-142">Use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method to set the g\_wszOriginalWaveFormat property.</span></span> <span data-ttu-id="e87a8-143">Use la estructura **WAVEFORMATEX** obtenida en el paso 6 como el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e87a8-143">Use the **WAVEFORMATEX** structure obtained in step 6 as the value of the property.</span></span>
10. <span data-ttu-id="e87a8-144">Incluya los cambios realizados en las propiedades de los medios de entrada mediante una llamada a [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) y pasándole un puntero a la interfaz **IWMInputMediaProps** .</span><span class="sxs-lookup"><span data-stu-id="e87a8-144">Include changes made to the input media properties by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and passing it a pointer to the **IWMInputMediaProps** interface.</span></span>
11. <span data-ttu-id="e87a8-145">Comience a leer ejemplos del archivo original y a pasarlos al escritor con llamadas a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="e87a8-145">Begin reading samples from the original file and passing them to the writer with calls to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e87a8-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e87a8-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e87a8-147">**Temas avanzados**</span><span class="sxs-lookup"><span data-stu-id="e87a8-147">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="e87a8-148">**Interfaz IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="e87a8-148">**IWMInputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[<span data-ttu-id="e87a8-149">**Interfaz IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="e87a8-149">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="e87a8-150">**Interfaz IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="e87a8-150">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="e87a8-151">**Interfaz IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="e87a8-151">**IWMPropertyVault Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[<span data-ttu-id="e87a8-152">**Interfaz IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="e87a8-152">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




