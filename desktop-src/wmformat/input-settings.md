---
title: Configuración de entrada
description: Configuración de entrada
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- SDK de Windows Media Format, constantes globales
- Advanced Systems Format (ASF), constantes globales
- ASF (formato de sistemas avanzados), constantes globales
- constantes globales, lista de
- SDK de Windows Media Format, constantes
- Advanced Systems Format (ASF), constantes
- ASF (formato de sistemas avanzados), constantes
- constantes, lista de
- SDK de Windows Media Format, configuración de entrada
- Advanced Systems Format (ASF), configuración de entrada
- ASF (formato de sistemas avanzados), configuración de entrada
- configuración de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077283"
---
# <a name="input-settings"></a><span data-ttu-id="82c4d-115">Configuración de entrada</span><span class="sxs-lookup"><span data-stu-id="82c4d-115">Input Settings</span></span>

<span data-ttu-id="82c4d-116">Las constantes globales siguientes se utilizan para identificar la configuración de entrada del escritor.</span><span class="sxs-lookup"><span data-stu-id="82c4d-116">The following global constants are used to identify input settings for the writer.</span></span>



| <span data-ttu-id="82c4d-117">Constante global</span><span class="sxs-lookup"><span data-stu-id="82c4d-117">Global constant</span></span>                        | <span data-ttu-id="82c4d-118">tipo de DataType del \_ atributo WMT \_</span><span class="sxs-lookup"><span data-stu-id="82c4d-118">WMT\_ATTR\_DATATYPE</span></span>                                                                                                                       | <span data-ttu-id="82c4d-119">Descripción de *pValue*</span><span class="sxs-lookup"><span data-stu-id="82c4d-119">Description of *pValue*</span></span>                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c4d-120">g \_ wszDeinterlaceMode</span><span class="sxs-lookup"><span data-stu-id="82c4d-120">g\_wszDeinterlaceMode</span></span>                  | <span data-ttu-id="82c4d-121">**WMT \_ Escriba \_ DWORD** establecido en uno de los valores de la tabla modo del tema [para Desentrelazar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="82c4d-121">**WMT\_TYPE\_DWORD** set to one of the values in the mode table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span>            | <span data-ttu-id="82c4d-122">Cuando se establece, especifica el tipo de contenido entrelazado de la entrada.</span><span class="sxs-lookup"><span data-stu-id="82c4d-122">When set, specifies the type of interlaced content of the input.</span></span> <span data-ttu-id="82c4d-123">Para obtener más información, vea [para Desentrelazar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="82c4d-123">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>                                                                                                                            |
| <span data-ttu-id="82c4d-124">g \_ wszFixedFrameRate</span><span class="sxs-lookup"><span data-stu-id="82c4d-124">g\_wszFixedFrameRate</span></span>                   | <span data-ttu-id="82c4d-125">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="82c4d-125">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="82c4d-126">Cuando se establece en true, indica al códec que no quite ningún fotograma durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="82c4d-126">When set to True, instructs the codec not to drop any frames during encoding.</span></span> <span data-ttu-id="82c4d-127">Esto hará que la [*velocidad de fotogramas*](wmformat-glossary.md) de la secuencia de vídeo de salida sea constante.</span><span class="sxs-lookup"><span data-stu-id="82c4d-127">This will cause the [*frame rate*](wmformat-glossary.md) of the output video stream to be constant.</span></span> <span data-ttu-id="82c4d-128">No es necesario que la velocidad de fotogramas del flujo de entrada sea constante.</span><span class="sxs-lookup"><span data-stu-id="82c4d-128">The frame rate of the input stream does not need to be constant.</span></span> |
| <span data-ttu-id="82c4d-129">g \_ wszInitialPatternForInverseTelecine</span><span class="sxs-lookup"><span data-stu-id="82c4d-129">g\_wszInitialPatternForInverseTelecine</span></span> | <span data-ttu-id="82c4d-130">**WMT \_ Escriba \_ DWORD** establecido en uno de los valores de la tabla patrón inicial del tema [para Desentrelazar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="82c4d-130">**WMT\_TYPE\_DWORD** set to one of the values in the initial pattern table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span> | <span data-ttu-id="82c4d-131">Cuando el modo de desentrelazado se establece en el \_ \_ desentrelazado de WM DM \_ INVERSETELECINE, se puede establecer para especificar el patrón de la entrada de [*telecine*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="82c4d-131">When the deinterlace mode is set to WM\_DM\_DEINTERLACE\_INVERSETELECINE, this can be set to specify the pattern of the [*telecine*](wmformat-glossary.md) input.</span></span> <span data-ttu-id="82c4d-132">Para obtener más información, vea [para Desentrelazar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="82c4d-132">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>        |
| <span data-ttu-id="82c4d-133">g \_ wszInterlacedCoding</span><span class="sxs-lookup"><span data-stu-id="82c4d-133">g\_wszInterlacedCoding</span></span>                 | <span data-ttu-id="82c4d-134">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="82c4d-134">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="82c4d-135">Cuando se establece en true, especifica que el códec debe codificar el flujo como contenido entrelazado.</span><span class="sxs-lookup"><span data-stu-id="82c4d-135">When set to True, specifies that that the codec should encode the stream as interlaced content.</span></span> <span data-ttu-id="82c4d-136">Para obtener más información, consulte [uso de vídeo entrelazado](to-use-interlaced-video.md).</span><span class="sxs-lookup"><span data-stu-id="82c4d-136">For more information, see [To Use Interlaced Video](to-use-interlaced-video.md).</span></span>                                                                                       |
| <span data-ttu-id="82c4d-137">g \_ wszJPEGCompressionQuality</span><span class="sxs-lookup"><span data-stu-id="82c4d-137">g\_wszJPEGCompressionQuality</span></span>           | <span data-ttu-id="82c4d-138">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="82c4d-138">**WMT\_TYPE\_DWORD**</span></span>                                                                                                                      | <span data-ttu-id="82c4d-139">Especifica el nivel de calidad JPEG (de 1 a 100) que se va a usar en la entrada.</span><span class="sxs-lookup"><span data-stu-id="82c4d-139">Specifies the JPEG quality level (from 1 to 100) to be used on the input.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="82c4d-140">g \_ wszWatermarkCLSID</span><span class="sxs-lookup"><span data-stu-id="82c4d-140">g\_wszWatermarkCLSID</span></span>                   | <span data-ttu-id="82c4d-141">**\_GUID de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="82c4d-141">**WMT\_TYPE\_GUID**</span></span>                                                                                                                       | <span data-ttu-id="82c4d-142">El valor se establece en el GUID de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="82c4d-142">The value is set to the watermark GUID.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="82c4d-143">g \_ wszWatermarkConfig</span><span class="sxs-lookup"><span data-stu-id="82c4d-143">g\_wszWatermarkConfig</span></span>                  | <span data-ttu-id="82c4d-144">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="82c4d-144">**WMT\_TYPE\_STRING**</span></span>                                                                                                                     | <span data-ttu-id="82c4d-145">El valor se establece en la configuración de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="82c4d-145">The value is set to the watermark configuration.</span></span> <span data-ttu-id="82c4d-146">Este valor variará en función del DMO de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="82c4d-146">This value will vary depending upon the watermarking DMO.</span></span> <span data-ttu-id="82c4d-147">Consulte la documentación del sistema de marcas de agua para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="82c4d-147">Consult the documentation of the watermarking system for more information.</span></span>                                                                                   |



 

> [!Note]  
> <span data-ttu-id="82c4d-148">Los valores de entrada configurados para una secuencia no se conservan en el archivo escrito.</span><span class="sxs-lookup"><span data-stu-id="82c4d-148">The input settings configured for a stream are not persisted in the written file.</span></span> <span data-ttu-id="82c4d-149">Si desea que el lector personalizado tenga acceso a estos parámetros de codificación, debe crear atributos personalizados para almacenarlos en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="82c4d-149">If you want your custom reader to have access to these encoding parameters, you must create custom attributes to store them in the file header.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="82c4d-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82c4d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c4d-151">**IWMWriterAdvanced2::GetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="82c4d-151">**IWMWriterAdvanced2::GetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[<span data-ttu-id="82c4d-152">**IWMWriterAdvanced2::SetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="82c4d-152">**IWMWriterAdvanced2::SetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




