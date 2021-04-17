---
title: Obtener acceso a medios
description: Obtener acceso a medios
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Listas de reproducción de metarchivos de Windows Media, acceso a medios
- listas de reproducción, acceso a medios
- listas de reproducción de metarchivos, acceso a medios
- Listas de reproducción de metarchivos de Windows Media, acceso a medios
- listas de reproducción, acceso a medios
- listas de reproducción de metarchivos, acceso a medios
- Listas de reproducción de metarchivo de Windows Media, controlar la reproducción
- listas de reproducción, controlar la reproducción
- listas de reproducción de metarchivos, controlar la reproducción
- Listas de reproducción de metarchivos de Windows Media, configuración de duración
- listas de reproducción, configuración de la duración
- listas de reproducción de metarchivos, establecer duración
- Windows Media Player, acceso a medios
- Media Player de Windows, acceso a medios
- Windows Media Player, controlar la reproducción
- Windows Media Player, establecer la duración
- obtener acceso a medios
- acceso a medios
- controlar la reproducción
- configuración de la duración
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695406"
---
# <a name="accessing-media"></a><span data-ttu-id="a15f1-123">Obtener acceso a medios</span><span class="sxs-lookup"><span data-stu-id="a15f1-123">Accessing Media</span></span>

<span data-ttu-id="a15f1-124">Use listas de reproducción para especificar y controlar los archivos multimedia o multimedia de streaming que reproduce Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a15f1-124">Use playlists to specify and to control the streaming media or media files that Windows Media Player plays.</span></span>

<span data-ttu-id="a15f1-125">Use el elemento **entry** para especificar un elemento multimedia único (un archivo multimedia o una secuencia en directo) y los elementos secundarios (como imágenes, vínculos **MOREINFO** y texto **abstracto** ).</span><span class="sxs-lookup"><span data-stu-id="a15f1-125">Use the **ENTRY** element to specify a single media element (a media file or a live stream) and any child elements (such as images, **MOREINFO** links, and **ABSTRACT** text).</span></span> <span data-ttu-id="a15f1-126">Use un elemento **ENTRYREF** para especificar una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a15f1-126">Use an **ENTRYREF** element to specify a playlist.</span></span> <span data-ttu-id="a15f1-127">Una lista de reproducción puede contener uno o varios elementos de **entrada** o **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="a15f1-127">A playlist can contain one or more **ENTRY** or **ENTRYREF** elements.</span></span> <span data-ttu-id="a15f1-128">Windows Media Player ejecuta una lista de reproducción empezando por la primera entrada y reproduciendo cada entrada a su vez hasta que se complete la lista.</span><span class="sxs-lookup"><span data-stu-id="a15f1-128">Windows Media Player executes a playlist by starting with the first entry and then playing each entry in turn until the list is finished.</span></span>

<span data-ttu-id="a15f1-129">Un elemento de **entrada** puede apuntar a cualquier tipo de medio que Windows Media Player pueda reproducir.</span><span class="sxs-lookup"><span data-stu-id="a15f1-129">An **ENTRY** element can point to any type of media that Windows Media Player can play.</span></span> <span data-ttu-id="a15f1-130">Esto incluye no solo archivos. WMA,. wmv,. ASF y. avi, por nombrar algunos, pero también secuencias en directo.</span><span class="sxs-lookup"><span data-stu-id="a15f1-130">This includes not only .wma, .wmv, .asf, and .avi files, to name a few, but live streams as well.</span></span> <span data-ttu-id="a15f1-131">Mediante el uso de una serie de elementos **entry** o **ENTRYREF** para hacer referencia a contenido multimedia, puede usar una lista de reproducción para enviar un flujo único compuesto por varios orígenes.</span><span class="sxs-lookup"><span data-stu-id="a15f1-131">By using a series of **ENTRY** or **ENTRYREF** elements to reference media content, you can use a playlist to send a single stream that consists of multiple sources.</span></span> <span data-ttu-id="a15f1-132">Los flujos a los que se hace referencia se reproducirán secuencialmente y el visor lo verá como una secuencia continua.</span><span class="sxs-lookup"><span data-stu-id="a15f1-132">The referenced streams will play sequentially and be seen as one continuous stream by the viewer.</span></span> <span data-ttu-id="a15f1-133">Por ejemplo, la lista de reproducción puede contener dos elementos de **entrada** : una introducción estándar de un archivo de Windows Media con una extensión. WMA y una secuencia de medios de Windows activa.</span><span class="sxs-lookup"><span data-stu-id="a15f1-133">For example, the playlist can contain two **ENTRY** elements: a standard introduction from a Windows Media file with a .wma extension, and a live Windows Media stream.</span></span>

> [!Note]  
> <span data-ttu-id="a15f1-134">Una lista de reproducción no debe contener vínculos a archivos multimedia que tengan contenido creado con versiones diferentes de Rights Management digitales (DRM).</span><span class="sxs-lookup"><span data-stu-id="a15f1-134">A playlist must not contain links to media files that have content created with different versions of Digital Rights Management (DRM).</span></span> <span data-ttu-id="a15f1-135">En una lista de reproducción de metarchivo, si hay vínculos para archivos multimedia con contenido de DRM versión 1 y para archivos multimedia creados con versiones posteriores de DRM, Windows Media Player solo reproducirá el contenido de DRM versión 1.</span><span class="sxs-lookup"><span data-stu-id="a15f1-135">In a metafile playlist, if there are links for media files with DRM version 1 content and for media files created with later DRM versions, Windows Media Player will only play the DRM version 1 content.</span></span>

 

## <a name="controlling-playback"></a><span data-ttu-id="a15f1-136">Controlar la reproducción</span><span class="sxs-lookup"><span data-stu-id="a15f1-136">Controlling Playback</span></span>

<span data-ttu-id="a15f1-137">Use listas de reproducción para controlar no solo qué clip multimedia se reproduce, sino también qué partes del clip se reproducen y cómo.</span><span class="sxs-lookup"><span data-stu-id="a15f1-137">Use playlists to control not only which media clip is played, but also which portions of the clip are played and how.</span></span> <span data-ttu-id="a15f1-138">Puede usar listas de reproducción para definir un conjunto de clips que se repiten o se repiten, para establecer la duración de la reproducción y para asignar las horas de inicio, así como los marcadores de inicio y finalización de cada entrada.</span><span class="sxs-lookup"><span data-stu-id="a15f1-138">You can use playlists to define a set of clips to be looped or repeated, to set the duration of play, and to assign start times, and start and end markers for each entry.</span></span> <span data-ttu-id="a15f1-139">Los elementos **STARTTIME**, **STARTMARKER** y **ENDMARKER** funcionan junto con los marcadores del archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a15f1-139">The **STARTTIME**, **STARTMARKER**, and **ENDMARKER** elements work in conjunction with markers in the media file.</span></span>

<span data-ttu-id="a15f1-140">Por ejemplo, la siguiente lista de reproducción usa un banner de AD y el vínculo de **MOREINFO** asociado en una **entrada** y hace referencia a **STARTMARKER** y **ENDMARKER**.</span><span class="sxs-lookup"><span data-stu-id="a15f1-140">For example, the following playlist uses an ad banner and the associated **MOREINFO** link in one **ENTRY**, and references a **STARTMARKER** and **ENDMARKER**.</span></span>


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a><span data-ttu-id="a15f1-141">Configuración de la duración</span><span class="sxs-lookup"><span data-stu-id="a15f1-141">Setting Duration</span></span>

<span data-ttu-id="a15f1-142">Use el elemento **Duration** para especificar cuánto tiempo se reproduce un clip o un conjunto de clips.</span><span class="sxs-lookup"><span data-stu-id="a15f1-142">Use the **DURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="a15f1-143">También puede usar el atributo **PREVIEWMODE** del elemento **ASX** junto con el elemento **PREVIEWDURATION** para especificar cuánto tiempo se reproduce un clip o un conjunto de clips.</span><span class="sxs-lookup"><span data-stu-id="a15f1-143">You can also use the **PREVIEWMODE** attribute of the **ASX** element in conjunction with the **PREVIEWDURATION** element to specify how long to play a clip or set of clips.</span></span> <span data-ttu-id="a15f1-144">Establezca el atributo **PREVIEWMODE** en sí para usar el elemento **PREVIEWDURATION** para especificar cuánto tiempo se va a reproducir el clip asociado.</span><span class="sxs-lookup"><span data-stu-id="a15f1-144">Set the **PREVIEWMODE** attribute to YES to use the **PREVIEWDURATION** element to specify how long to play the associated clip.</span></span> <span data-ttu-id="a15f1-145">Los elementos **PREVIEWDURATION** y **Duration** tienen el mismo comportamiento.</span><span class="sxs-lookup"><span data-stu-id="a15f1-145">The **PREVIEWDURATION** and **DURATION** elements have the same behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a15f1-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a15f1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a15f1-147">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="a15f1-147">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a15f1-148">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="a15f1-148">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a15f1-149">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a15f1-149">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a15f1-150">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a15f1-150">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




