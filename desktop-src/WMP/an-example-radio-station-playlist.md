---
title: Lista de reproducción de la estación de radio de ejemplo
description: Lista de reproducción de la estación de radio de ejemplo
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Listas de reproducción de metarchivos de Windows Media, ejemplos de listas de reproducción
- listas de reproducción, ejemplos de listas de reproducción
- listas de reproducción de metarchivos, ejemplos de listas de reproducción
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, listas de reproducción de ejemplo
- listas de reproducción, listas de reproducción de ejemplo
- listas de reproducción de metarchivos, listas de reproducción de ejemplo
- Listas de reproducción de metarchivos de Windows Media, ejemplo de código
- listas de reproducción, ejemplo de código
- listas de reproducción de metarchivos, ejemplo de código
- Listas de reproducción de metarchivo de Windows Media, ejemplo de lista de reproducción de la estación de radio
- listas de reproducción, ejemplo de lista de reproducción de la estación de radio
- listas de reproducción de metarchivo, ejemplo de lista de reproducción de la estación de radio
- Media Player de Windows, ejemplos de lista de reproducción
- Windows Media Player, listas de reproducción de ejemplo
- Windows Media Player, listas de reproducción de ejemplo
- Ejemplo de Windows Media Player, lista de reproducción de la estación de radio
- ejemplos de listas de reproducción
- listas de reproducción de ejemplo
- listas de reproducción de ejemplo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418580"
---
# <a name="an-example-radio-station-playlist"></a><span data-ttu-id="a3db2-125">Lista de reproducción de la estación de radio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3db2-125">An Example Radio Station Playlist</span></span>

<span data-ttu-id="a3db2-126">En el ejemplo de código siguiente se muestra cómo crear una lista de reproducción para examinar tres emisoras de radio de rock.</span><span class="sxs-lookup"><span data-stu-id="a3db2-126">The following example code illustrates how to create a playlist to scan three rock radio stations.</span></span> <span data-ttu-id="a3db2-127">La marca de radio de Adventure Works de la empresa ficticia está en la lista de reproducción y en todas las secuencias individuales de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a3db2-127">The fictitious company Adventure Works Radio brand is on the playlist and on all of the individual streams within the playlist.</span></span> <span data-ttu-id="a3db2-128">Al escribir el código, cambie todas las direcciones URL y los nombres de archivo a nombres de archivo válidos a los que pueda tener acceso su Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="a3db2-128">When you write your code, change all URLs and file names to valid file names that are accessible to your Windows Media Player.</span></span>

<span data-ttu-id="a3db2-129">Se crea una lista de reproducción para cada una de las estaciones.</span><span class="sxs-lookup"><span data-stu-id="a3db2-129">A playlist is created for each of the stations.</span></span> <span data-ttu-id="a3db2-130">Una cuarta lista de reproducción examina los tres primeros.</span><span class="sxs-lookup"><span data-stu-id="a3db2-130">A fourth playlist scans through the first three.</span></span> <span data-ttu-id="a3db2-131">Las listas de reproducción se crean para hacer referencia a anuncios generados dinámicamente y tienen una marca de radio de Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="a3db2-131">The playlists are created to reference dynamically generated advertisements and have Adventure Works Radio branding.</span></span>

<span data-ttu-id="a3db2-132">Una de las listas de reproducción que representan una emisora de radio podría tener este aspecto.</span><span class="sxs-lookup"><span data-stu-id="a3db2-132">One of the playlists representing a radio station might look like this.</span></span>


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="a3db2-133">A continuación, la lista de reproducción se puede crear a partir de referencias a las listas de reproducción individuales.</span><span class="sxs-lookup"><span data-stu-id="a3db2-133">The playlist can then be constructed of references to the individual playlists.</span></span>

<span data-ttu-id="a3db2-134">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3db2-134">Example Code</span></span>


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



<span data-ttu-id="a3db2-135">En este ejemplo se reproduce un anuncio seguido de 30 segundos de cada una de las tres estaciones a las que se hace referencia, una tras otra.</span><span class="sxs-lookup"><span data-stu-id="a3db2-135">This example would play an ad followed by 30 seconds of each of the three stations referenced, one after the other.</span></span> <span data-ttu-id="a3db2-136">Este ciclo se repite indefinidamente porque no se define el atributo **Count** del elemento **REPEAT** .</span><span class="sxs-lookup"><span data-stu-id="a3db2-136">This cycle will repeat indefinitely because the **COUNT** attribute of the **REPEAT** element is not defined.</span></span>

-   <span data-ttu-id="a3db2-137">Las empresas, las organizaciones, los productos, las personas y los eventos usados en los ejemplos son ficticios.</span><span class="sxs-lookup"><span data-stu-id="a3db2-137">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="a3db2-138">No se entenderá o deducirá ninguna asociación con ninguna empresa, organización, producto, persona o acontecimiento reales.</span><span class="sxs-lookup"><span data-stu-id="a3db2-138">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3db2-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3db2-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3db2-140">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="a3db2-140">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a3db2-141">**Listas de reproducción de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="a3db2-141">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="a3db2-142">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="a3db2-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="a3db2-143">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a3db2-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="a3db2-144">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="a3db2-144">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




