---
title: Usar HTML con Windows Media Player
description: Usar HTML con Windows Media Player
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Media Player de Windows, HTML
- Modelo de objetos de Windows Media Player, HTML
- modelo de objetos, HTML
- Control ActiveX de Windows Media Player, HTML para el modelo de objetos
- Control ActiveX, HTML para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, HTML para el modelo de objetos
- Windows Media Player Mobile, HTML para el modelo de objetos
- HTML con Media Player de Windows
- Incrustación de páginas web, HTML
- incrustación, páginas web
- comandos de script
- Volteo de URL
- transmisión por secuencias multimedia enriquecida
- compatibilidad de exploradores
- Mostrar páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903533"
---
# <a name="using-html-with-windows-media-player"></a><span data-ttu-id="f9fbd-118">Usar HTML con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="f9fbd-118">Using HTML with Windows Media Player</span></span>

## <a name="overview"></a><span data-ttu-id="f9fbd-119">Información general</span><span class="sxs-lookup"><span data-stu-id="f9fbd-119">Overview</span></span>

<span data-ttu-id="f9fbd-120">Usar HTML con Windows Media Player es una forma excelente de combinar audio y vídeo con texto y gráficos.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-120">Using HTML with Windows Media Player is an excellent way to combine audio and video with text and graphics.</span></span> <span data-ttu-id="f9fbd-121">Puede incrustar el control Media Player de Windows en una página web si desea complementar el contenido estático o crear aplicaciones web con medios digitales.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-121">You can embed the Windows Media Player control in a webpage when you want to supplement your static content or create Web applications with digital media.</span></span> <span data-ttu-id="f9fbd-122">Si desea complementar los medios digitales con HTML, puede mostrar las páginas web en el modo completo del reproductor haciendo referencia a ellas en las listas de reproducción de metarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-122">When you want to supplement your digital media with HTML, on the other hand, you can display webpages in the full mode of the Player by referencing them in Windows Media metafile playlists.</span></span>

<span data-ttu-id="f9fbd-123">Si escribe programas personalizados que insertan el control de Media Player de Windows en modo remoto, también puede controlar las páginas web que se muestran en los distintos paneles del modo completo del reproductor cuando los usuarios desacoplan el control.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-123">If you write custom programs that embed the Windows Media Player control in remote mode, you can also control the webpages displayed in the various panes of the full mode of the Player when your users undock the control.</span></span> <span data-ttu-id="f9fbd-124">Esto le permite conservar la continuidad entre los Estados acoplado y desacoplado.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-124">This lets you preserve continuity between the docked and undocked states.</span></span>

## <a name="web-embedding"></a><span data-ttu-id="f9fbd-125">Incrustación Web</span><span class="sxs-lookup"><span data-stu-id="f9fbd-125">Web Embedding</span></span>

<span data-ttu-id="f9fbd-126">Puede usar el control Media Player de Windows como parte de una página web que cree.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-126">You can use the Windows Media Player control as part of a webpage you create.</span></span> <span data-ttu-id="f9fbd-127">Vea [incrustar el Control Media Player de Windows en una página web](embedding-the-windows-media-player-control-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="f9fbd-127">See [Embedding the Windows Media Player Control in a Web Page](embedding-the-windows-media-player-control-in-a-web-page.md).</span></span>

## <a name="script-commands-and-url-flipping"></a><span data-ttu-id="f9fbd-128">Comandos de script y volteo de direcciones URL</span><span class="sxs-lookup"><span data-stu-id="f9fbd-128">Script Commands and URL Flipping</span></span>

<span data-ttu-id="f9fbd-129">Los comandos de script son pares de texto/valor que se pueden insertar en los archivos multimedia digitales o en las secuencias.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-129">Script commands are text/value pairs you can embed in your digital media files or streams.</span></span> <span data-ttu-id="f9fbd-130">Puede usar comandos de script personalizados únicamente para desencadenar código de script y permitir que Windows Media Player Controle automáticamente otros comandos de script.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-130">You might use custom script commands solely to trigger script code, while letting Windows Media Player handle other script commands automatically.</span></span>

<span data-ttu-id="f9fbd-131">Si tiene varias páginas web que acompañan a una presentación multimedia digital, los comandos de la secuencia de comandos de dirección URL pueden cambiar automáticamente la página en un marco mientras el control Media Player de Windows continúa reproduciendo medios digitales en otro marco.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-131">When you have several webpages that accompany a digital media presentation, URL script commands can automatically change the page in one frame while the Windows Media Player control continues playing digital media in another frame.</span></span> <span data-ttu-id="f9fbd-132">Esto se denomina volteo de URL y es una manera excelente de crear una presentación multimedia.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-132">This is called URL flipping, and is an excellent way to create a multimedia slide show.</span></span> <span data-ttu-id="f9fbd-133">Otros comandos de script controlados automáticamente permiten cambiar la reproducción a un archivo o secuencia de medios diferente, mostrar texto de subtítulos o desencadenar eventos como inserciones de anuncios definidas en una lista de reproducción de metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-133">Other automatically handled script commands let you switch playback to a different media file or stream, display captioning text, or trigger events such as ad insertions defined in a Windows Media metafile playlist.</span></span>

<span data-ttu-id="f9fbd-134">Para obtener más información sobre el volteo de direcciones URL, vea [crear Web-Based presentaciones](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="f9fbd-134">For more information about URL flipping, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="rich-media-streaming"></a><span data-ttu-id="f9fbd-135">Transmisión por secuencias multimedia enriquecida</span><span class="sxs-lookup"><span data-stu-id="f9fbd-135">Rich Media Streaming</span></span>

<span data-ttu-id="f9fbd-136">El volteo de direcciones URL funciona mejor con páginas simples que se cargan rápidamente.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-136">URL flipping works best with simple pages that load rapidly.</span></span> <span data-ttu-id="f9fbd-137">Con páginas más complejas, se transfieren varios componentes individualmente, lo que dificulta la sincronización de la presentación de la página con los medios digitales.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-137">With more complex pages, multiple components are transferred individually, making it difficult to synchronize page display with digital media.</span></span> <span data-ttu-id="f9fbd-138">Para permitir presentaciones multimedia complejas, las páginas web se pueden agregar a una secuencia de medios y entregarse al reproductor de la misma manera que el audio y el vídeo.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-138">To allow complex rich media presentations, webpages can be added to a media stream and delivered to the Player in the same way as audio and video.</span></span> <span data-ttu-id="f9fbd-139">Esto le permite sincronizar los componentes de la presentación mucho más fácilmente, especialmente en las conexiones de baja velocidad.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-139">This lets you synchronize the components of your presentation much more easily, especially over low-speed connections.</span></span>

<span data-ttu-id="f9fbd-140">Para obtener más información sobre la transmisión por secuencias de multimedia enriquecida, consulte [creación de Web-Based presentaciones](creating-web-based-presentations.md).</span><span class="sxs-lookup"><span data-stu-id="f9fbd-140">For more information about rich media streaming, see [Creating Web-Based Presentations](creating-web-based-presentations.md).</span></span>

## <a name="browser-support"></a><span data-ttu-id="f9fbd-141">Compatibilidad con exploradores</span><span class="sxs-lookup"><span data-stu-id="f9fbd-141">Browser Support</span></span>

<span data-ttu-id="f9fbd-142">Puede incrustar el control de Windows Media Player en Microsoft Internet Explorer, Firefox y Netscape Navigator, aunque el proceso es ligeramente diferente para cada uno.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-142">You can embed the Windows Media Player control in Microsoft Internet Explorer, Firefox, and Netscape Navigator, although the process is slightly different for each.</span></span> <span data-ttu-id="f9fbd-143">También puede crear páginas Web diseñadas para trabajar con los tres exploradores.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-143">You can also create webpages designed to work with all three browsers.</span></span>

<span data-ttu-id="f9fbd-144">Con Internet Explorer y Firefox, se incrusta el control mediante el elemento de objeto HTML.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-144">With Internet Explorer and Firefox, you embed the control using the HTML OBJECT element.</span></span> <span data-ttu-id="f9fbd-145">Sin embargo, el navegador requiere un enfoque diferente porque no admite directamente los controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-145">Navigator requires a different approach, however, because it doesn't directly support ActiveX controls.</span></span> <span data-ttu-id="f9fbd-146">Con Navigator, se usa el elemento APPLET para insertar un applet Java especial en la página.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-146">With Navigator, you use the APPLET element to embed a special Java applet into the page.</span></span> <span data-ttu-id="f9fbd-147">Este applet controla la comunicación con el control ActiveX del reproductor.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-147">This applet handles communication with the Player ActiveX control.</span></span>

<span data-ttu-id="f9fbd-148">Para obtener más información sobre la compatibilidad con Firefox, consulte [uso del control de Media Player de Windows con Firefox](using-the-windows-media-player-control-with-firefox.md).</span><span class="sxs-lookup"><span data-stu-id="f9fbd-148">For more information about Firefox support, see [Using the Windows Media Player Control with Firefox](using-the-windows-media-player-control-with-firefox.md).</span></span>

<span data-ttu-id="f9fbd-149">Para obtener más información acerca de la compatibilidad con Netscape Navigator, consulte [uso de Windows Media Player con netscape 7,1](using-windows-media-player-with-netscape-7-1.md).</span><span class="sxs-lookup"><span data-stu-id="f9fbd-149">For more information about Netscape Navigator support, see [Using Windows Media Player with Netscape 7.1](using-windows-media-player-with-netscape-7-1.md).</span></span>

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a><span data-ttu-id="f9fbd-150">Mostrar páginas web en el modo completo del reproductor</span><span class="sxs-lookup"><span data-stu-id="f9fbd-150">Displaying Web Pages in the Full Mode of the Player</span></span>

<span data-ttu-id="f9fbd-151">Puede ampliar la funcionalidad de Windows Media Player o proporcionar una vista personalizada de la información que acompaña a los archivos multimedia digitales al mostrar las páginas web en el modo completo del reproductor.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-151">You can extend the functionality of Windows Media Player or provide a custom view of information that accompanies your digital media by displaying webpages in the full mode of the Player.</span></span> <span data-ttu-id="f9fbd-152">Esta es la característica HTMLView de los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-152">This is the HTMLView feature of Windows Media metafiles.</span></span> <span data-ttu-id="f9fbd-153">Los metaarchivos proporcionan un gran control sobre el contenido de la lista de reproducción, lo que le permite realizar una transición sin problemas entre clips, insertar anuncios y mostrar imágenes fijas en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-153">Metafiles give you great control over playlist content, allowing you to seamlessly transition between clips, insert advertisements, and display still images in Windows Media Player.</span></span> <span data-ttu-id="f9fbd-154">Para mostrar las páginas web en el modo completo del reproductor, use el elemento PARAM para agregar referencias de URL a las entradas de la lista de reproducción o a todas las listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f9fbd-154">To display webpages in the full mode of the Player, you use the PARAM element to add URL references to your playlist entries or to entire playlists.</span></span>

<span data-ttu-id="f9fbd-155">Para obtener más información sobre el uso de páginas web en los metaarchivos, vea [Mostrar páginas web en Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="f9fbd-155">For more information about using webpages in metafiles, see [Displaying Web Pages in Windows Media Player](displaying-web-pages-in-windows-media-player.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9fbd-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9fbd-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9fbd-157">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="f9fbd-157">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




