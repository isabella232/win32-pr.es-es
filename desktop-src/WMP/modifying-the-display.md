---
title: Modificar la presentación
description: Modificar la presentación
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Listas de reproducción de metarchivos de Windows Media, modificar pantallas
- listas de reproducción, modificar pantallas
- listas de reproducción de metarchivos, modificar pantallas
- Listas de reproducción de metarchivos de Windows Media, modificación de pantalla
- listas de reproducción, modificación de pantalla
- listas de reproducción de metarchivos, modificación de pantalla
- Windows Media Player, modificación de la presentación
- Windows Media Player, modificar pantallas
- Media Player de Windows, propiedades de texto
- Windows Media Player, propiedades de imagen
- Media Player de Windows, propiedades de MOREINFO
- Media Player de Windows, texto ABSTRACTo
- Propiedades de MOREINFO
- Texto ABSTRACTo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075508"
---
# <a name="modifying-the-display"></a><span data-ttu-id="bedca-117">Modificar la presentación</span><span class="sxs-lookup"><span data-stu-id="bedca-117">Modifying the Display</span></span>

<span data-ttu-id="bedca-118">Las listas de reproducción pueden modificar la interfaz de usuario de Media Player de Windows de cuatro maneras principales:</span><span class="sxs-lookup"><span data-stu-id="bedca-118">Playlists can alter the Windows Media Player user interface in four main ways:</span></span>

-   <span data-ttu-id="bedca-119">Propiedades de texto</span><span class="sxs-lookup"><span data-stu-id="bedca-119">Text properties</span></span>
-   <span data-ttu-id="bedca-120">Propiedades de la imagen</span><span class="sxs-lookup"><span data-stu-id="bedca-120">Image properties</span></span>
-   <span data-ttu-id="bedca-121">Propiedades de MOREINFO</span><span class="sxs-lookup"><span data-stu-id="bedca-121">MOREINFO properties</span></span>
-   <span data-ttu-id="bedca-122">Texto ABSTRACTo</span><span class="sxs-lookup"><span data-stu-id="bedca-122">ABSTRACT text</span></span>

## <a name="text-properties"></a><span data-ttu-id="bedca-123">Propiedades de texto</span><span class="sxs-lookup"><span data-stu-id="bedca-123">Text properties</span></span>

<span data-ttu-id="bedca-124">Windows Media Player habilita la presentación de texto de metadatos de título, autor, copyright y descripción.</span><span class="sxs-lookup"><span data-stu-id="bedca-124">Windows Media Player enables the display of Title, Author, Copyright, and Description metadata text.</span></span> <span data-ttu-id="bedca-125">Los metadatos de clip pueden provienen de la secuencia o el archivo multimedia, o pueden proviene de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="bedca-125">Clip metadata can come from the stream or media file, or it can come from a playlist.</span></span> <span data-ttu-id="bedca-126">Mostrar metadatos proceden de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="bedca-126">Show metadata comes from the playlist.</span></span> <span data-ttu-id="bedca-127">En general, las listas de reproducción son un método mejor para pasar las propiedades de texto a Windows Media Player, especialmente si es probable que los elementos de texto cambien.</span><span class="sxs-lookup"><span data-stu-id="bedca-127">In general, playlists are a better method of passing text properties to Windows Media Player, especially if text elements are likely to change.</span></span> <span data-ttu-id="bedca-128">Es más fácil editar el texto de una lista de reproducción que volver a crear un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="bedca-128">It is easier to edit text in a playlist than to re-author a media file.</span></span> <span data-ttu-id="bedca-129">Y dado que las propiedades leídas de una lista de reproducción invalidan las contenidas en el archivo multimedia, puede actualizar fácilmente el texto de la pantalla agregando el nuevo texto a la propiedad correspondiente en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="bedca-129">And because properties read from a playlist override those contained in the media file, you can easily update display text by adding the new text to the corresponding property in a playlist.</span></span> <span data-ttu-id="bedca-130">En el ejemplo siguiente, el texto de los metadatos de título y de autor de la lista de reproducción invalida el título y el texto del autor contenidos en el archivo multimedia, sample. WMA.</span><span class="sxs-lookup"><span data-stu-id="bedca-130">In the following example, the text of the Title and Author metadata in the playlist overrides the Title and Author text contained in the media file, sample.wma.</span></span>

<span data-ttu-id="bedca-131">El texto de **Descripción** se recupera de un archivo de Windows Media al que se hace referencia en un elemento de **entrada** a menos que haya un elemento **abstracto** en una lista de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="bedca-131">**DESCRIPTION** text is retrieved from a Windows Media file referenced in an **ENTRY** element unless there is an **ABSTRACT** element in a metafile playlist.</span></span> <span data-ttu-id="bedca-132">Si hay texto **abstracto** , se mostrará, reemplazando el texto de **Descripción** .</span><span class="sxs-lookup"><span data-stu-id="bedca-132">If there is **ABSTRACT** text, it will be displayed, overriding the **DESCRIPTION** text.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a><span data-ttu-id="bedca-133">Propiedades de la imagen</span><span class="sxs-lookup"><span data-stu-id="bedca-133">Image properties</span></span>

<span data-ttu-id="bedca-134">Se pueden agregar imágenes de banner a la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bedca-134">Banner images can be added to the user interface of Windows Media Player.</span></span> <span data-ttu-id="bedca-135">El gráfico se puede usar para anunciar, proporcionar información y proporcionar acceso a sitios web, para nombrar algunas posibilidades.</span><span class="sxs-lookup"><span data-stu-id="bedca-135">The graphic can be used for advertising, providing information, and providing access to websites, to name a few possibilities.</span></span>

<span data-ttu-id="bedca-136">Use el elemento **banner** para especificar una imagen gráfica (32 píxeles de alto por 194 píxeles de ancho) para que la muestre Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bedca-136">Use the **BANNER** element to specify a graphic image (32 pixels high by 194 pixels wide) for display by Windows Media Player.</span></span> <span data-ttu-id="bedca-137">El gráfico se muestra debajo de cualquier contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bedca-137">The graphic is displayed below any video content.</span></span> <span data-ttu-id="bedca-138">Se puede Agregar un hipervínculo al banner mediante el elemento secundario **MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="bedca-138">A hyperlink can be added to the banner using the **MOREINFO** child element.</span></span>

<span data-ttu-id="bedca-139">Una información sobre herramientas se puede definir mediante un elemento **abstract** dentro del ámbito del elemento **banner** .</span><span class="sxs-lookup"><span data-stu-id="bedca-139">A ToolTip can be defined by an **ABSTRACT** element within the scope of the **BANNER** element.</span></span> <span data-ttu-id="bedca-140">Cualquier texto de información sobre herramientas definido se puede mostrar al pausar el puntero del mouse sobre el gráfico del banner.</span><span class="sxs-lookup"><span data-stu-id="bedca-140">Any defined ToolTip text can be displayed by pausing the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="bedca-141">Al seleccionar el gráfico de encabezado con el puntero del mouse se activará cualquier hipervínculo definido con el elemento **MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="bedca-141">Selecting the banner graphic with the mouse pointer will activate any hyperlink defined with the **MOREINFO** element.</span></span>

<span data-ttu-id="bedca-142">El formato de gráfico de **banner** preferido es el formato GIF.</span><span class="sxs-lookup"><span data-stu-id="bedca-142">The preferred **BANNER** graphics format is the GIF format.</span></span> <span data-ttu-id="bedca-143">Se puede usar el formato JPG si el gráfico tiene el tamaño adecuado.</span><span class="sxs-lookup"><span data-stu-id="bedca-143">The JPG format can be used if the graphic is properly sized.</span></span>

<span data-ttu-id="bedca-144">En el ejemplo anterior se muestra el uso del elemento **banner** .</span><span class="sxs-lookup"><span data-stu-id="bedca-144">The previous example illustrates use of the **BANNER** element.</span></span>

> [!Note]  
> <span data-ttu-id="bedca-145">Las imágenes de **banner** no son compatibles con los archivos DRM o cuando Windows Media Player está incrustado en una página web.</span><span class="sxs-lookup"><span data-stu-id="bedca-145">**BANNER** images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

 

<span data-ttu-id="bedca-146">Para obtener más información sobre los banners, vea [gráficos personalizados en Windows Media Player](custom-graphics-in-windows-media-player.md).</span><span class="sxs-lookup"><span data-stu-id="bedca-146">For more information about banners, see [Custom Graphics in Windows Media Player](custom-graphics-in-windows-media-player.md).</span></span>

## <a name="moreinfo-properties"></a><span data-ttu-id="bedca-147">Propiedades de MOREINFO</span><span class="sxs-lookup"><span data-stu-id="bedca-147">MOREINFO properties</span></span>

<span data-ttu-id="bedca-148">Las áreas de texto e imagen de la interfaz de usuario pueden asociarse con direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="bedca-148">Text and image areas of the user interface can be associated with URLs.</span></span> <span data-ttu-id="bedca-149">Durante la reproducción, los usuarios pueden seleccionar una de estas secciones para conectarse a la dirección URL asociada a ella en su explorador Web.</span><span class="sxs-lookup"><span data-stu-id="bedca-149">During playback, users can select one of these sections to connect to the URL associated with it in their Web browser.</span></span> <span data-ttu-id="bedca-150">Por ejemplo, puede asociar el sitio web de un anunciante a una imagen de banner de ad, como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="bedca-150">For example, you can associate an advertiser's website with an ad banner image as shown in the following code snippet.</span></span>


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a><span data-ttu-id="bedca-151">Texto ABSTRACTo</span><span class="sxs-lookup"><span data-stu-id="bedca-151">ABSTRACT text</span></span>

<span data-ttu-id="bedca-152">Texto **abstracto** se usa para mostrar una breve descripción emergente de las áreas de texto o imagen de la interfaz de usuario a la que está asociada.</span><span class="sxs-lookup"><span data-stu-id="bedca-152">**ABSTRACT** text is used to display a short pop-up description of the text or image areas of the user interface it is associated with.</span></span> <span data-ttu-id="bedca-153">Durante la reproducción, si el puntero del mouse se desplaza sobre una de estas áreas, aparece una información sobre herramientas junto al puntero del mouse que muestra el texto **abstracto** asociado al área.</span><span class="sxs-lookup"><span data-stu-id="bedca-153">During playback, if the mouse pointer hovers over one of these areas, a ToolTip appears beside the mouse pointer displaying the **ABSTRACT** text associated with the area.</span></span> <span data-ttu-id="bedca-154">El texto **abstracto** se recupera de un metarchivo y se define con el elemento **abstracto** .</span><span class="sxs-lookup"><span data-stu-id="bedca-154">**ABSTRACT** text is retrieved from a metafile and is defined with the **ABSTRACT** element.</span></span> <span data-ttu-id="bedca-155">El elemento **abstracto** puede ser un elemento secundario de una **entrada** o un elemento **banner** .</span><span class="sxs-lookup"><span data-stu-id="bedca-155">The **ABSTRACT** element can be a child element of either an **ENTRY** or a **BANNER** element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bedca-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bedca-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bedca-157">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="bedca-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="bedca-158">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="bedca-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="bedca-159">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bedca-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="bedca-160">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="bedca-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




