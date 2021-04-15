---
title: Compatibilidad con marcas de agua
description: Compatibilidad con marcas de agua
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- SDK de Windows Media Format, compatibilidad con marca de agua
- Windows Media Format SDK, marca de agua digital
- Advanced Systems Format (ASF), compatibilidad con marcas de agua
- ASF (formato de sistemas avanzados), compatibilidad con marca de agua
- Advanced Systems Format (ASF), marca de agua digital
- ASF (formato de sistemas avanzados), marca de agua digital
- Windows Media Format SDK, DMO
- Advanced Systems Format (ASF), DMO
- ASF (formato de sistemas avanzados), DMO
- SDK de Windows Media Format, interfaz IWMWatermarkInfo
- Advanced Systems Format (ASF), IWMWatermarkInfo (interfaz)
- ASF (formato de sistemas avanzados), interfaz IWMWatermarkInfo
- marcas de agua, acerca de
- marca de agua digital
- Objeto multimedia de DirectX (DMO), acerca de
- DMO (objeto multimedia de DirectX), acerca de
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695558"
---
# <a name="watermarking-support"></a><span data-ttu-id="47f54-120">Compatibilidad con marcas de agua</span><span class="sxs-lookup"><span data-stu-id="47f54-120">Watermarking Support</span></span>

<span data-ttu-id="47f54-121">La marca de agua digital es una manera de insertar derechos de autor u otra información en los datos de una secuencia de medios.</span><span class="sxs-lookup"><span data-stu-id="47f54-121">Digital watermarking is a way to embed copyright or other information in the data of a media stream.</span></span> <span data-ttu-id="47f54-122">Las técnicas para la marca de agua varían mucho de una solución a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="47f54-122">Techniques for watermarking vary widely from one solution to the next.</span></span> <span data-ttu-id="47f54-123">La forma más sencilla de marca de agua es simplemente agregar una imagen de identificación a cada fotograma de una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="47f54-123">The simplest form of watermarking is simply adding an identifying image to each frame of a video stream.</span></span> <span data-ttu-id="47f54-124">Las estaciones de televisión suelen usar esta técnica para insertar un logotipo semitransparente en una esquina inferior de la difusión.</span><span class="sxs-lookup"><span data-stu-id="47f54-124">Television stations frequently use this technique to insert a semi-transparent logo in a bottom corner of their broadcast.</span></span> <span data-ttu-id="47f54-125">Las formas más sofisticadas de la marca de agua digital son imperceptibles para el usuario que ve o escucha el contenido.</span><span class="sxs-lookup"><span data-stu-id="47f54-125">More sophisticated forms of digital watermarking are imperceptible to the user watching or listening to the content.</span></span>

<span data-ttu-id="47f54-126">El SDK de Windows Media Format admite el uso de [*DMOs*](wmformat-glossary.md)de marca de agua digital.</span><span class="sxs-lookup"><span data-stu-id="47f54-126">The Windows Media Format SDK supports the use of digital watermarking [*DMOs*](wmformat-glossary.md).</span></span> <span data-ttu-id="47f54-127">En la práctica, un sistema de marca de agua es muy similar a un códec: toma muestras multimedia, ejecuta algoritmos en los datos y genera los ejemplos alterados.</span><span class="sxs-lookup"><span data-stu-id="47f54-127">In practice, a watermarking system is very similar to a codec: it takes media samples, runs algorithms on the data, and outputs the altered samples.</span></span> <span data-ttu-id="47f54-128">Cuando se especifica un sistema de marcas de agua para una secuencia, el objeto de escritor incluye DMO en el procesamiento de los ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="47f54-128">When a watermarking system is specified for a stream, the writer object includes the DMO in its processing of input samples.</span></span>

<span data-ttu-id="47f54-129">Debe especificar la información de configuración de marca de agua al configurar una secuencia para la marca de agua.</span><span class="sxs-lookup"><span data-stu-id="47f54-129">You must specify watermark configuration information when you configure a stream for watermarking.</span></span> <span data-ttu-id="47f54-130">Los valores de configuración serán diferentes en función del DMO de marca de agua.</span><span class="sxs-lookup"><span data-stu-id="47f54-130">The configuration values will be different depending upon the watermarking DMO.</span></span> <span data-ttu-id="47f54-131">La DMO que use debe tener instrucciones que describan los valores de configuración que admite.</span><span class="sxs-lookup"><span data-stu-id="47f54-131">The DMO you use should come with instructions describing the configuration values it supports.</span></span>

<span data-ttu-id="47f54-132">Para obtener información sobre la configuración que se usa para especificar un sistema de marca de agua, vea [ **IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span><span class="sxs-lookup"><span data-stu-id="47f54-132">For information about the settings used to specify a watermarking system, see [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span></span>

<span data-ttu-id="47f54-133">Puede programar la aplicación para enumerar el DMOs de marca de agua instalado en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="47f54-133">You can program your application to enumerate the watermarking DMOs installed on the client computer.</span></span> <span data-ttu-id="47f54-134">Para obtener más información, consulte la interfaz [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .</span><span class="sxs-lookup"><span data-stu-id="47f54-134">For more information, see the [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47f54-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47f54-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47f54-136">**Características de escritura de archivos**</span><span class="sxs-lookup"><span data-stu-id="47f54-136">**File Writing Features**</span></span>](file-writing-features.md)
</dt> </dl>

 

 




