---
title: Agregar subtítulos a medios digitales
description: Agregar subtítulos a medios digitales
ms.assetid: 0fdd2cdc-32d4-4fda-9596-b050107abd5f
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Intercambio de multimedia accesible sincronizado (SAMI), acerca de
- SAMI (intercambio de multimedia accesible sincronizado), acerca de
- Windows Media Player, agregar subtítulos (CC)
- Modelo de objetos de Windows Media Player, agregar subtítulos (CC)
- modelo de objetos, agregar subtítulos (CC)
- Windows Media Player Mobile, agregar subtítulos (CC)
- Control ActiveX de Windows Media Player, agregar subtítulos (CC)
- Control ActiveX móvil de Windows Media Player, agregar subtítulos (CC)
- Control ActiveX, agregar subtítulos (CC)
- Intercambio de multimedia accesible sincronizado (SAMI), agregar subtítulos (CC)
- SAMI (intercambio de multimedia accesible sincronizado), agregar subtítulos (CC)
- agregar subtítulos (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc464fb879df1c7642cd0a04b319383654bae4aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075394"
---
# <a name="adding-closed-captions-to-digital-media"></a><span data-ttu-id="450be-122">Agregar subtítulos a medios digitales</span><span class="sxs-lookup"><span data-stu-id="450be-122">Adding Closed Captions to Digital Media</span></span>

<span data-ttu-id="450be-123">El intercambio de multimedia accesible sincronizado (SAMI) es un formato de archivo diseñado para ofrecer texto sincronizado como leyendas, subtítulos o descripciones de audio con contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="450be-123">Synchronized Accessible Media Interchange (SAMI) is a file format designed to deliver synchronized text such as captions, subtitles, or audio descriptions with digital media content.</span></span> <span data-ttu-id="450be-124">Integrado en un explorador Web con el modelo de objetos de Windows Media Player, SAMI promueve la accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="450be-124">Integrated in a Web browser using the Windows Media Player object model, SAMI promotes accessibility.</span></span> <span data-ttu-id="450be-125">Mediante el uso de SAMI, puede crear contenido multimedia enriquecido que llegue a un público más grande y más diverso.</span><span class="sxs-lookup"><span data-stu-id="450be-125">By using SAMI, you can create rich media content that reaches a larger, more diverse audience.</span></span>

<span data-ttu-id="450be-126">Además de las fuentes estándar, SAMI puede admitir otros estilos de texto, como diferentes colores, tamaños o lenguajes, para ayudar a una gran variedad de usuarios.</span><span class="sxs-lookup"><span data-stu-id="450be-126">In addition to standard fonts, SAMI can support other text styles, such as different colors, sizes, or languages to aid a variety of users.</span></span> <span data-ttu-id="450be-127">SAMI puede ser especialmente útil para personas que tienen deficiencias visuales o personas sordas o con dificultades auditivas.</span><span class="sxs-lookup"><span data-stu-id="450be-127">SAMI can be particularly useful for individuals who have low vision or those who are deaf or hard-of-hearing.</span></span> <span data-ttu-id="450be-128">El formato SAMI también puede ayudar en el uso educativo, como la enseñanza de estudiantes en un segundo idioma.</span><span class="sxs-lookup"><span data-stu-id="450be-128">The SAMI format can also assist in educational purposes, such as teaching students a second language.</span></span>

<span data-ttu-id="450be-129">Este tema se centra en la incorporación de SAMI con el modelo de objetos de control ActiveX de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="450be-129">This topic focuses on the incorporation of SAMI with the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="450be-130">Los archivos SAMI existen de forma independiente de los archivos multimedia digitales y no se basan en un formato de vídeo o audio específico para funcionar.</span><span class="sxs-lookup"><span data-stu-id="450be-130">SAMI files exist independently from digital media files and do not rely on a specific video or audio format to function.</span></span> <span data-ttu-id="450be-131">Puesto que los archivos son independientes, el control Media Player de Windows buscará, analizará, sincronizará y representará cada archivo en el equipo del cliente.</span><span class="sxs-lookup"><span data-stu-id="450be-131">Since the files are separate, the Windows Media Player control will locate, parse, synchronize, and render each file on the client's computer.</span></span> <span data-ttu-id="450be-132">Esto proporciona una mayor flexibilidad y funcionalidad, ya que permite la edición de archivos SAMI individuales, la incorporación del archivo SAMI con distintos formatos de medios digitales y el almacenamiento de archivos SAMI en diferentes ubicaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="450be-132">This provides for added flexibility and functionality because it allows for the editing of individual SAMI files, the incorporation of the SAMI file with different digital media formats, and the storage of SAMI files on different server locations.</span></span>

<span data-ttu-id="450be-133">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="450be-133">This topic contains the following sections.</span></span>



| <span data-ttu-id="450be-134">Sección</span><span class="sxs-lookup"><span data-stu-id="450be-134">Section</span></span>                                                                                                                            | <span data-ttu-id="450be-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="450be-135">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="450be-136">Acerca de los archivos SAMI</span><span class="sxs-lookup"><span data-stu-id="450be-136">About SAMI Files</span></span>](about-sami-files.md)                                                                                           | <span data-ttu-id="450be-137">Describe la estructura básica de los archivos SAMI.</span><span class="sxs-lookup"><span data-stu-id="450be-137">Describes the basic structure of SAMI files.</span></span>                                               |
| [<span data-ttu-id="450be-138">Ejemplo de archivo SAMI</span><span class="sxs-lookup"><span data-stu-id="450be-138">SAMI File Example</span></span>](sami-file-example.md)                                                                                         | <span data-ttu-id="450be-139">Describe la estructura de un archivo SAMI de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="450be-139">Describes the structure of an example SAMI file.</span></span>                                           |
| [<span data-ttu-id="450be-140">Usar SAMI con el control de Media Player de Windows en un explorador</span><span class="sxs-lookup"><span data-stu-id="450be-140">Using SAMI with the Windows Media Player Control in a Browser</span></span>](using-sami-with-the-windows-media-player-control-in-a-browser.md) | <span data-ttu-id="450be-141">Describe cómo usar SAMI en una página web con el control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="450be-141">Describes how to use SAMI in a webpage with the Windows Media Player control.</span></span>              |
| [<span data-ttu-id="450be-142">Acerca de las direcciones URL de SAMI</span><span class="sxs-lookup"><span data-stu-id="450be-142">About SAMI URLs</span></span>](about-sami-urls.md)                                                                                             | <span data-ttu-id="450be-143">Describe cómo se pueden asociar los archivos multimedia digitales a los archivos SAMI usando una sola dirección URL.</span><span class="sxs-lookup"><span data-stu-id="450be-143">Describes how digital media files can be associated with SAMI files by using a single URL.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="450be-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="450be-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="450be-145">**Guía de control del reproductor**</span><span class="sxs-lookup"><span data-stu-id="450be-145">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




