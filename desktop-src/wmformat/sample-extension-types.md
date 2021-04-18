---
title: Tipos de extensión de ejemplo
description: Tipos de extensión de ejemplo
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- SDK de Windows Media Format, extensiones de ejemplo
- Advanced Systems Format (ASF), extensiones de ejemplo
- ASF (formato de sistemas avanzados), extensiones de ejemplo
- Windows Media Format SDK, extensiones de unidad de datos
- Advanced Systems Format (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- SDK de Windows Media Format, propiedades de búfer
- Advanced Systems Format (ASF), propiedades de búfer
- ASF (formato de sistemas avanzados), propiedades de búfer
- extensiones de ejemplo, tipos
- extensiones de unidad de datos, tipos
- propiedades de búfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "105714349"
---
# <a name="sample-extension-types"></a><span data-ttu-id="0eca8-115">Tipos de extensión de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0eca8-115">Sample Extension Types</span></span>

<span data-ttu-id="0eca8-116">Las extensiones de ejemplo, también denominadas extensiones de unidad de datos (cuotas) o propiedades de búfer, son elementos de datos que se adjuntan a los ejemplos de medios en la sección de datos del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="0eca8-116">Sample extensions, also called data unit extensions (DUEs) or buffer properties, are items of data that are attached to the media samples in the data section of the ASF file.</span></span> <span data-ttu-id="0eca8-117">En el SDK de Windows Media Format se definen varios tipos de extensiones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-117">Several types of sample extensions are defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="0eca8-118">También puede crear sus propios tipos de extensión.</span><span class="sxs-lookup"><span data-stu-id="0eca8-118">You can also create your own extension types.</span></span>

<span data-ttu-id="0eca8-119">Para usar las extensiones de ejemplo, debe identificar el tipo de extensión en los datos de configuración de la secuencia del perfil.</span><span class="sxs-lookup"><span data-stu-id="0eca8-119">To use sample extensions, you must identify the extension type in the stream configuration data of the profile.</span></span> <span data-ttu-id="0eca8-120">Llame al método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para configurar una secuencia que acepte ejemplos con datos extendidos.</span><span class="sxs-lookup"><span data-stu-id="0eca8-120">Call the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method to configure a stream to accept samples with extended data.</span></span>

<span data-ttu-id="0eca8-121">Las extensiones de ejemplo individuales se deben agregar a los ejemplos de entrada mediante una llamada al método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="0eca8-121">Individual sample extensions must be added to the input samples by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="0eca8-122">Al leer ejemplos, puede llamar al método [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) para recuperar los datos de la extensión.</span><span class="sxs-lookup"><span data-stu-id="0eca8-122">When reading samples, you can call the [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) method to retrieve the extension data.</span></span> <span data-ttu-id="0eca8-123">También puede utilizar los métodos de la interfaz [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) para enumerar las extensiones de unidad de datos adjuntas a un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-123">You can also use the methods of the [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) interface to enumerate the data unit extensions attached to a sample.</span></span>

<span data-ttu-id="0eca8-124">En la tabla siguiente se enumeran los identificadores de extensión de unidad de datos predefinidos y se describen los datos que se adjuntan a los ejemplos de cada uno.</span><span class="sxs-lookup"><span data-stu-id="0eca8-124">The following table lists the predefined data unit extension identifiers, and describes the data that is attached to samples for each.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0eca8-125">GUID de extensión de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0eca8-125">Sample extension GUID</span></span></th>
<th><span data-ttu-id="0eca8-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="0eca8-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0eca8-127">WM_SampleExtensionGUID_OutputCleanPoint</span><span class="sxs-lookup"><span data-stu-id="0eca8-127">WM_SampleExtensionGUID_OutputCleanPoint</span></span></td>
<td><span data-ttu-id="0eca8-128">Los datos indican si el ejemplo es un <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span><span class="sxs-lookup"><span data-stu-id="0eca8-128">The data indicates whether the sample is a <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span></span> <span data-ttu-id="0eca8-129">Un valor de cero indica que el ejemplo no es un cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="0eca8-129">A value of zero indicates that the sample is not a cleanpoint.</span></span> <span data-ttu-id="0eca8-130">Un valor distinto de cero indica que se trata de un cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="0eca8-130">A non-zero value indicates that it is a cleanpoint.</span></span> <span data-ttu-id="0eca8-131">Este tipo de extensión de unidad de datos (vencimiento) de ejemplo se usa para realizar un seguimiento de cleanpoints al escribir secuencias de medios precomprimidos codificados con códecs de terceros.</span><span class="sxs-lookup"><span data-stu-id="0eca8-131">This sample data unit extension (DUE) type is used to keep track of cleanpoints when writing precompressed media streams that were encoded with third-party codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0eca8-132">WM_SampleExtensionGUID_Timecode</span><span class="sxs-lookup"><span data-stu-id="0eca8-132">WM_SampleExtensionGUID_Timecode</span></span></td>
<td><span data-ttu-id="0eca8-133">Los datos son una estructura <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> que contiene datos de código de tiempo SMPTE asociados al ejemplo. El tamaño de este debido siempre es WM_SampleExtension_Timecode_Size, que es 14 bytes.</span><span class="sxs-lookup"><span data-stu-id="0eca8-133">The data is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> structure containing SMPTE time code data associated with the sample.The size for this DUE is always WM_SampleExtension_Timecode_Size, which is 14 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0eca8-134">WM_SampleExtensionGUID_FileName</span><span class="sxs-lookup"><span data-stu-id="0eca8-134">WM_SampleExtensionGUID_FileName</span></span></td>
<td><span data-ttu-id="0eca8-135">Este tipo de extensión de ejemplo se usa para las secuencias de archivo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-135">This type of sample extension is used for file streams.</span></span> <span data-ttu-id="0eca8-136">Los datos de un ejemplo de secuencia de archivos son una parte de un archivo de datos.</span><span class="sxs-lookup"><span data-stu-id="0eca8-136">The data in a file stream sample is a piece of a data file.</span></span> <span data-ttu-id="0eca8-137">Los datos de la extensión de ejemplo especifican el nombre del archivo del que se tomó el contenido de la muestra. El nombre de archivo es una cadena de caracteres anchos que contiene el nombre de archivo en el formato Name. Extension sin información de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="0eca8-137">The data in the sample extension specifies the name of the file from which the content in the sample was taken.The file name is a wide-character string containing the file name in name.extension format without any path information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0eca8-138">WM_SampleExtensionGUID_ContentType</span><span class="sxs-lookup"><span data-stu-id="0eca8-138">WM_SampleExtensionGUID_ContentType</span></span></td>
<td><span data-ttu-id="0eca8-139">Los datos identifican el tipo de contenido que contiene el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-139">The data identifies the type of content that the sample contains.</span></span> <span data-ttu-id="0eca8-140">Este tipo de extensión de ejemplo se usa con secuencias de vídeo entrelazadas. Todo el contenido entrelazado utiliza la marca WM_CT_INTERLACED combinada por <strong>una operación OR bit a bit</strong> con WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST o WM_CT_REPEAT_FIRST_FIELD.</span><span class="sxs-lookup"><span data-stu-id="0eca8-140">This type of sample extension is used with interlaced video streams.All interlaced content uses the WM_CT_INTERLACED flag combined by a bitwise <strong>OR</strong> with either WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST, or WM_CT_REPEAT_FIRST_FIELD.</span></span><br/> <span data-ttu-id="0eca8-141">El orden de los campos no se utiliza en el proceso de codificación, pero se mantiene con los ejemplos comprimidos para que se pueda pasar al hardware de representación.</span><span class="sxs-lookup"><span data-stu-id="0eca8-141">The field order is not used in the encoding process, but is maintained with the compressed samples so that it can be passed to the rendering hardware.</span></span> <span data-ttu-id="0eca8-142">La reproducción de contenido entrelazado con el orden de campo incorrecto presenta artefactos como la vibración de movimiento en el vídeo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-142">Playing interlaced content with the incorrect field order introduces artifacts such as motion jitter in the video.</span></span><br/> <span data-ttu-id="0eca8-143">El tamaño de este debido siempre es WM_SampleExtension_ContentType_Size.</span><span class="sxs-lookup"><span data-stu-id="0eca8-143">The size for this DUE is always WM_SampleExtension_ContentType_Size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0eca8-144">WM_SampleExtensionGUID_PixelAspectRatio</span><span class="sxs-lookup"><span data-stu-id="0eca8-144">WM_SampleExtensionGUID_PixelAspectRatio</span></span></td>
<td><span data-ttu-id="0eca8-145">Los datos indican la relación de aspecto de píxeles del contenido en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-145">The data indicates the pixel aspect ratio of the content in the sample.</span></span> <span data-ttu-id="0eca8-146">Esto solo se aplica al vídeo. Este tipo de extensión se usa para identificar la relación de aspecto de los píxeles no cuadrados.</span><span class="sxs-lookup"><span data-stu-id="0eca8-146">This applies only to video.This extension type is used to identify the aspect ratio of non-square pixels.</span></span> <span data-ttu-id="0eca8-147">Para obtener más información, vea <a href="to-read-and-write-video-streams-with-non-square-pixels.md">para leer y escribir secuencias de vídeo con píxeles no cuadrados</a>.</span><span class="sxs-lookup"><span data-stu-id="0eca8-147">For more information, see <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.</span></span><br/> <span data-ttu-id="0eca8-148">Los valores de relación de aspecto se almacenan como una palabra cuyo byte bajo es el aspecto X y cuyo byte alto es el aspecto Y.</span><span class="sxs-lookup"><span data-stu-id="0eca8-148">Aspect ratio values are stored as a word whose low byte is the X aspect and whose high byte is the Y aspect.</span></span> <span data-ttu-id="0eca8-149">Por ejemplo, 16:9 se almacena como 0x0910.</span><span class="sxs-lookup"><span data-stu-id="0eca8-149">For example, 16:9 is stored as 0x0910.</span></span><br/> <span data-ttu-id="0eca8-150">El tamaño de este debido siempre es WM_SampleExtension_PixelAspectRatio_Size, que es 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="0eca8-150">The size for this DUE is always WM_SampleExtension_PixelAspectRatio_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0eca8-151">WM_SampleExtensionGUID_SampleDuration</span><span class="sxs-lookup"><span data-stu-id="0eca8-151">WM_SampleExtensionGUID_SampleDuration</span></span></td>
<td><span data-ttu-id="0eca8-152">Los datos indican la duración, en milisegundos, del ejemplo contenido en el objeto de búfer.</span><span class="sxs-lookup"><span data-stu-id="0eca8-152">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span> <span data-ttu-id="0eca8-153">En la reproducción, si esta causa se establece, el objeto de lector la usará para sobrescribir el valor de duración de ejemplo existente. Esto se debe a que los componentes en tiempo de ejecución de SDK establecen automáticamente en secuencias de vídeo con velocidades de bits de 100 kbps o superiores, donde la sobrecarga de la información debida no es significativa.</span><span class="sxs-lookup"><span data-stu-id="0eca8-153">On playback, if this DUE is set the reader object will use it to overwrite the existing sample duration value.This DUE is set automatically by the SDK run-time components on video streams with bit rates of 100 kbps or greater, where the overhead of the DUE information is not significant.</span></span> <span data-ttu-id="0eca8-154">No se establece para las secuencias con velocidades de bits en 100 kbps.</span><span class="sxs-lookup"><span data-stu-id="0eca8-154">It is not set for streams with bit rates under 100 kbps.</span></span> <span data-ttu-id="0eca8-155">Las aplicaciones no deben establecer esto debido a que el escritor (en flujos de velocidad de bits alto) sobrescribirá el valor con sus propios datos.</span><span class="sxs-lookup"><span data-stu-id="0eca8-155">Applications should not set this DUE manually because the writer (on high-bit-rate streams) will overwrite the value with its own data.</span></span><br/> <span data-ttu-id="0eca8-156">El tamaño de este debido siempre es WM_SampleExtension_SampleDuration_Size, que es 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="0eca8-156">The size for this DUE is always WM_SampleExtension_SampleDuration_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0eca8-157">WM_SampleExtensionGUID_ChromaLocation</span><span class="sxs-lookup"><span data-stu-id="0eca8-157">WM_SampleExtensionGUID_ChromaLocation</span></span></td>
<td><span data-ttu-id="0eca8-158">Los datos indican el tipo de submuestreo de croma usado en el formato de vídeo i420. El valor de esta extensión se establece en uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="0eca8-158">The data indicates the type of chroma subsampling used in the I420 video format.The value of this extension is set to one of the follow values:</span></span><br/>
<ul>
<li><span data-ttu-id="0eca8-159">WM_CL_INTERLACED420</span><span class="sxs-lookup"><span data-stu-id="0eca8-159">WM_CL_INTERLACED420</span></span></li>
<li><span data-ttu-id="0eca8-160">WM_CL_PROGRESSIVE420</span><span class="sxs-lookup"><span data-stu-id="0eca8-160">WM_CL_PROGRESSIVE420</span></span></li>
</ul>
<span data-ttu-id="0eca8-161">Esta extensión de unidad de datos no está configurada en el perfil.</span><span class="sxs-lookup"><span data-stu-id="0eca8-161">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="0eca8-162">Se incluye en los resultados de los ejemplos del descodificador.</span><span class="sxs-lookup"><span data-stu-id="0eca8-162">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="0eca8-163">El tamaño de este debido siempre es WM_SampleExtension_ChromaLocation_Size, que es 1 byte.</span><span class="sxs-lookup"><span data-stu-id="0eca8-163">The size of this DUE is always WM_SampleExtension_ChromaLocation_Size, which is 1 byte.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0eca8-164">WM_SampleExtensionGUID_ColorSpaceInfo</span><span class="sxs-lookup"><span data-stu-id="0eca8-164">WM_SampleExtensionGUID_ColorSpaceInfo</span></span></td>
<td><span data-ttu-id="0eca8-165">Los datos proporcionan información sobre el espacio de colores usado para el fotograma de vídeo actual. El valor de esta extensión es una estructura de <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0eca8-165">The data provides information about the color space used for the current video frame.The value of this extension is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> structure.</span></span><br/> <span data-ttu-id="0eca8-166">Esta extensión de unidad de datos no está configurada en el perfil.</span><span class="sxs-lookup"><span data-stu-id="0eca8-166">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="0eca8-167">Se incluye en los resultados de los ejemplos del descodificador.</span><span class="sxs-lookup"><span data-stu-id="0eca8-167">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="0eca8-168">El tamaño de este debido siempre es WM_SampleExtension_ColorSpaceInfo_Size, que es 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="0eca8-168">The size of this DUE is always WM_SampleExtension_ColorSpaceInfo_Size, which is 3 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0eca8-169">WM_SampleExtensionGUID_UserDataInfo</span><span class="sxs-lookup"><span data-stu-id="0eca8-169">WM_SampleExtensionGUID_UserDataInfo</span></span></td>
<td><span data-ttu-id="0eca8-170">Los datos son datos de usuario personalizados. Los primeros cuatro bytes de los datos contienen el tamaño de los datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="0eca8-170">The data is custom user data.The first four bytes of the data contain the size of the custom data.</span></span><br/> <span data-ttu-id="0eca8-171">El siguiente byte contiene el tipo de datos de usuario proporcionados en la extensión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-171">The next byte contains the type of user data provided in the sample extension.</span></span> <span data-ttu-id="0eca8-172">Se admiten los siguientes tipos:</span><span class="sxs-lookup"><span data-stu-id="0eca8-172">The following types are supported:</span></span><br/>
<ul>
<li><span data-ttu-id="0eca8-173">0x1F: datos de usuario de nivel de secuencia</span><span class="sxs-lookup"><span data-stu-id="0eca8-173">0x1F - Sequence level user data</span></span></li>
<li><span data-ttu-id="0eca8-174">0x1E: datos de usuario de nivel de punto de entrada</span><span class="sxs-lookup"><span data-stu-id="0eca8-174">0x1E - Entry-point level user data</span></span></li>
<li><span data-ttu-id="0eca8-175">0x1D: datos de usuario de nivel de marco</span><span class="sxs-lookup"><span data-stu-id="0eca8-175">0x1D - Frame level user data</span></span></li>
<li><span data-ttu-id="0eca8-176">0x1C-datos de usuario de nivel de campo</span><span class="sxs-lookup"><span data-stu-id="0eca8-176">0x1C - Field level user data</span></span></li>
<li><span data-ttu-id="0eca8-177">0x1B: datos de usuario de nivel de segmento</span><span class="sxs-lookup"><span data-stu-id="0eca8-177">0x1B - Slice level user data</span></span></li>
</ul>
<span data-ttu-id="0eca8-178">Los bytes sexto y siguiente contienen los datos del usuario.</span><span class="sxs-lookup"><span data-stu-id="0eca8-178">The sixth and subsequent bytes contain the user data.</span></span> <span data-ttu-id="0eca8-179">Hay tantos bytes de datos de usuario como especifica el número en los primeros cuatro bytes.</span><span class="sxs-lookup"><span data-stu-id="0eca8-179">There are as many bytes of user data as specified by the number in the first four bytes.</span></span><br/> <span data-ttu-id="0eca8-180">Esta extensión de unidad de datos no está configurada en el perfil.</span><span class="sxs-lookup"><span data-stu-id="0eca8-180">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="0eca8-181">Se incluye en los ejemplos que se generan desde el descodificador.</span><span class="sxs-lookup"><span data-stu-id="0eca8-181">It is included in samples that are output from the decoder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0eca8-182">WM_SampleExtensionGUID_SampleProtectionSalt</span><span class="sxs-lookup"><span data-stu-id="0eca8-182">WM_SampleExtensionGUID_SampleProtectionSalt</span></span></td>
<td><span data-ttu-id="0eca8-183">Los datos se cifran mediante un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0eca8-183">The data is encrypted by sample.</span></span> <span data-ttu-id="0eca8-184">Este tipo de extensión de ejemplo se usa para el contenido que se importa desde un formato de archivo no ASF y un esquema de protección de derechos distinto de DRM de Windows Media. Al importar contenido protegido, cada ejemplo debe incluir un valor Salt único.</span><span class="sxs-lookup"><span data-stu-id="0eca8-184">This sample extension type is used for content that is imported from a non-ASF file format and a rights protection scheme other than Windows Media DRM.When importing protected content, each sample must include a unique salt.</span></span> <span data-ttu-id="0eca8-185">Normalmente, este valor es un contador que aumenta de forma continuada.</span><span class="sxs-lookup"><span data-stu-id="0eca8-185">Typically, this value is a monotonically increasing counter.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0eca8-186">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0eca8-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eca8-187">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="0eca8-187">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 





