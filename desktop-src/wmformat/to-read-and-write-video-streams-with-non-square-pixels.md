---
title: Para leer y escribir secuencias de vídeo con píxeles no cuadrados
description: Para leer y escribir secuencias de vídeo con píxeles no cuadrados
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- SDK de Windows Media Format, lectura de secuencias de vídeo
- SDK de Windows Media Format, escribir secuencias de vídeo
- SDK de Windows Media Format, secuencias de vídeo
- SDK de Windows Media Format, píxeles no cuadrados
- Windows Media Format SDK, píxeles (no cuadrado)
- Advanced Systems Format (ASF), lectura de secuencias de vídeo
- ASF (formato de sistemas avanzados), lectura de secuencias de vídeo
- Advanced Systems Format (ASF), escribir secuencias de vídeo
- ASF (formato de sistemas avanzados), escribir secuencias de vídeo
- Advanced Systems Format (ASF), secuencias de vídeo
- ASF (formato de sistemas avanzados), secuencias de vídeo
- Advanced Systems Format (ASF), píxeles no cuadrados
- ASF (formato de sistemas avanzados), píxeles no cuadrados
- Advanced Systems Format (ASF), píxeles (no cuadrados)
- ASF (formato de sistemas avanzados), píxeles (no cuadrados)
- lectura de secuencias de vídeo
- escribir secuencias de vídeo
- secuencias de vídeo, lectura
- secuencias de vídeo, escritura
- secuencias de vídeo, píxeles no cuadrados
- píxeles no cuadrados
- píxeles (no cuadrados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357046"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a><span data-ttu-id="760df-125">Para leer y escribir secuencias de vídeo con píxeles no cuadrados</span><span class="sxs-lookup"><span data-stu-id="760df-125">To Read and Write Video Streams with Non-Square Pixels</span></span>

<span data-ttu-id="760df-126">Los monitores de equipo tienen píxeles cuadrados, pero otros tipos de pantallas de vídeo, incluidos los televisores NTSC, tienen píxeles rectangulares o no cuadrados.</span><span class="sxs-lookup"><span data-stu-id="760df-126">Computer monitors have square pixels, but other types of video screens, including NTSC televisions, have rectangular or non-square pixels.</span></span> <span data-ttu-id="760df-127">Además, algunos dispositivos de entrada, como las cámaras de vídeo digital (DV), han cargado pares de dispositivos con píxeles no cuadrados.</span><span class="sxs-lookup"><span data-stu-id="760df-127">Also, some input devices, such as Digital Video (DV) cameras, have charged couple devices with non-square pixels.</span></span> <span data-ttu-id="760df-128">Al escribir archivos que se basan en datos de origen de píxeles no cuadrados o que se van a mostrar en dispositivos con píxeles no cuadrados, la información de relación de aspecto de píxeles debe incluirse en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="760df-128">When you are writing files that are either based on non-square pixel source data or else intended for display on devices with non-square pixels, the pixel aspect ratio information must be included in the ASF file.</span></span> <span data-ttu-id="760df-129">Las aplicaciones de lector deben examinar esa información y usarla para ajustar la relación de aspecto del rectángulo de vídeo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="760df-129">Reader applications must examine that information and use it to adjust the aspect ratio of the video rectangle as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="760df-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="760df-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="760df-131">**Temas avanzados**</span><span class="sxs-lookup"><span data-stu-id="760df-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="760df-132">**Lectura de secuencias con píxeles no cuadrados**</span><span class="sxs-lookup"><span data-stu-id="760df-132">**Reading Streams with Non-Square Pixels**</span></span>](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[<span data-ttu-id="760df-133">**Escribir flujos con píxeles no cuadrados**</span><span class="sxs-lookup"><span data-stu-id="760df-133">**Writing Streams with Non-Square Pixels**</span></span>](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




