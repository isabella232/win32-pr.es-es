---
title: Usar metaarchivos para la conmutación de flujos sin problemas
description: Usar metaarchivos para la conmutación de flujos sin problemas
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Listas de reproducción de metarchivos de Windows Media, conmutación de flujos de eventos en directo
- listas de reproducción, conmutación de flujos de eventos en directo
- listas de reproducción de metarchivos, conmutación de flujos de eventos en directo
- Listas de reproducción de metarchivos de Windows Media, conmutación de flujos de eventos
- listas de reproducción, conmutación de flujos de eventos
- listas de reproducción de metarchivos, conmutación de flujos de eventos
- Listas de reproducción de metarchivos de Windows Media, inserción de anuncios
- listas de reproducción, inserción de anuncios
- listas de reproducción de metarchivos, inserción de anuncios
- Windows Media Player, conmutación por secuencias de eventos en directo
- Windows Media Player, conmutación de flujos de eventos
- Windows Media Player, inserción de anuncios
- cambio de secuencia de eventos en directo
- conmutación de flujos de eventos
- inserción de anuncio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704593"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a><span data-ttu-id="aced0-118">Usar metaarchivos para la conmutación de flujos sin problemas</span><span class="sxs-lookup"><span data-stu-id="aced0-118">Using Metafiles for Seamless Stream Switching</span></span>

<span data-ttu-id="aced0-119">Puede facilitar el intercambio de flujos sin problemas mediante listas de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="aced0-119">You can facilitate seamless stream switching using metafile playlists.</span></span> <span data-ttu-id="aced0-120">Normalmente, cuando un fragmento de contenido finaliza, el almacenamiento en búfer se produce para el siguiente clip o secuencia antes de que se abra (si se trata de contenido recibido de un servidor de streaming multimedia).</span><span class="sxs-lookup"><span data-stu-id="aced0-120">Usually, when a piece of content ends, buffering occurs for the next clip or stream before it opens (if it is content received from a streaming media server).</span></span> <span data-ttu-id="aced0-121">Microsoft Windows Media Services permite eliminar, o al menos minimizar, este tiempo de almacenamiento en búfer y hacer que otro fragmento de contenido transmitido empiece a reproducirse casi de inmediato.</span><span class="sxs-lookup"><span data-stu-id="aced0-121">Microsoft Windows Media Services enables you to eliminate, or at least minimize, this buffering time and have another piece of streamed content begin playing nearly immediately.</span></span> <span data-ttu-id="aced0-122">El modo normal de funcionamiento de Windows Media Player es abrir la siguiente secuencia de medios a la que hace referencia la lista de reproducción 20 segundos antes del final del flujo representado actualmente.</span><span class="sxs-lookup"><span data-stu-id="aced0-122">The normal mode of operation for Windows Media Player is to open the next media stream referenced by the playlist 20 seconds before the end of the currently rendered stream.</span></span> <span data-ttu-id="aced0-123">Por lo general, esto proporciona una transición sin problemas entre flujos multimedia, en función de otros factores, como los tiempos de acceso web.</span><span class="sxs-lookup"><span data-stu-id="aced0-123">This generally provides a seamless transition between media streams, depending on other factors such as Web access times.</span></span>

<span data-ttu-id="aced0-124">Use el elemento **Event** en una lista de reproducción junto con los comandos OPENEVENT del codificador para facilitar el cambio sin problemas entre las secuencias o los archivos.</span><span class="sxs-lookup"><span data-stu-id="aced0-124">Use the **EVENT** element in a playlist in conjunction with OPENEVENT commands from the encoder to facilitate seamless switching between streams or files.</span></span> <span data-ttu-id="aced0-125">El envío de un comando OPENEVENT de 20 segundos o más antes del comando de evento puede minimizar los retrasos en el cambio de secuencia.</span><span class="sxs-lookup"><span data-stu-id="aced0-125">Sending an OPENEVENT command 20 seconds or more prior to the EVENT command can minimize delays in stream switching.</span></span> <span data-ttu-id="aced0-126">A continuación, Windows Media Player puede cargar previamente una parte del próximo contenido de streaming en un búfer.</span><span class="sxs-lookup"><span data-stu-id="aced0-126">Then Windows Media Player is able to preload a portion of the upcoming streaming content into a buffer.</span></span>

<span data-ttu-id="aced0-127">Use el codificador de Windows Media para enviar un comando de script en la secuencia con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="aced0-127">Use Windows Media Encoder to send a script command in the stream using the following format:</span></span>


```XML
OPENEVENT eventname 

```



<span data-ttu-id="aced0-128">El nombre del evento debe ser el que se haya definido en el elemento de **evento** de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="aced0-128">The event name must be the one defined in the **EVENT** element in the playlist.</span></span> <span data-ttu-id="aced0-129">Cuando Windows Media Player recibe un comando de script de OPENEVENT desde el codificador, busca el elemento de **evento** en la lista de reproducción y comienza a almacenar en búfer el clip o el flujo definido en el elemento de **evento** .</span><span class="sxs-lookup"><span data-stu-id="aced0-129">When Windows Media Player receives an OPENEVENT script command from the encoder, it looks to the **EVENT** element in the playlist and begins buffering the clip or stream defined in the **EVENT** element.</span></span> <span data-ttu-id="aced0-130">Windows Media Player contiene esta información hasta el evento real del mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="aced0-130">Windows Media Player then holds this information until the actual event of the same name.</span></span> <span data-ttu-id="aced0-131">Cuando se recibe el evento con nombre, Windows Media Player cambia a ese contenido almacenado previamente en el búfer.</span><span class="sxs-lookup"><span data-stu-id="aced0-131">When the named event is received, Windows Media Player switches to that previously buffered content.</span></span>

> [!Note]  
> <span data-ttu-id="aced0-132">No se pueden usar caracteres Unicode para el comando de script OPENEVENT en el archivo multimedia o en el elemento de **evento** de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="aced0-132">You cannot use Unicode characters for the OPENEVENT script command in the media file or the **EVENT** element in the playlist.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aced0-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aced0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aced0-134">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="aced0-134">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="aced0-135">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="aced0-135">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="aced0-136">**Evento Player. comando**</span><span class="sxs-lookup"><span data-stu-id="aced0-136">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="aced0-137">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="aced0-137">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="aced0-138">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="aced0-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="aced0-139">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="aced0-139">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




