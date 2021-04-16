---
title: Usar el cambio de secuencia de eventos en directo
description: Usar el cambio de secuencia de eventos en directo
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
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
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268481"
---
# <a name="using-live-event-stream-switching"></a><span data-ttu-id="f9f0b-118">Usar el cambio de secuencia de eventos en directo</span><span class="sxs-lookup"><span data-stu-id="f9f0b-118">Using Live Event Stream Switching</span></span>

<span data-ttu-id="f9f0b-119">Los archivos multimedia de streaming también se pueden controlar mediante la interacción de los comandos de script insertados en una secuencia de medios con elementos de metarchivo de Windows Media en una lista de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-119">Streaming media can also be controlled by the interaction of script commands embedded in a media stream with Windows Media metafile elements in a metafile playlist.</span></span>

<span data-ttu-id="f9f0b-120">Un evento es un tipo determinado de comando de script incrustado en una secuencia de medios o un archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-120">An event is a particular type of script command embedded in a media stream or media file.</span></span> <span data-ttu-id="f9f0b-121">Cuando el control de Media Player de Windows recibe el comando de script, procesa el evento tal y como lo define el elemento de **evento** en la lista de reproducción del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-121">When the Windows Media Player control receives the script command, it processes the event as defined by the **EVENT** element in the metafile playlist.</span></span> <span data-ttu-id="f9f0b-122">Windows Media Player cambia del flujo actual que se está representando y representa el contenido al que se hace referencia en el elemento de **evento** de lista de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-122">Windows Media Player switches from the current stream it is rendering and renders the content referenced in the metafile playlist **EVENT** element.</span></span> <span data-ttu-id="f9f0b-123">El elemento de **evento** se utiliza normalmente en producción en vivo.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-123">The **EVENT** element is usually used in live production.</span></span>

<span data-ttu-id="f9f0b-124">Un elemento de **evento** tiene un aspecto similar a un elemento de **entrada** , pero cada uno de ellos controla la reproducción de secuencias y archivos multimedia de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-124">An **EVENT** element looks similar to an **ENTRY** element, but each handles the playback of streams and media files differently.</span></span> <span data-ttu-id="f9f0b-125">El elemento **entry** se usa para crear listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-125">The **ENTRY** element is used to create playlists.</span></span> <span data-ttu-id="f9f0b-126">Un flujo o un archivo multimedia al que se hace referencia en un elemento de **entrada** comienza A reproducirse cuando finaliza la secuencia o el archivo multimedia al que se hace referencia en la **entrada** anterior.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-126">A stream or media file referenced in an **ENTRY** element starts playing when the stream or media file referenced in the previous **ENTRY** finishes.</span></span> <span data-ttu-id="f9f0b-127">Un flujo al que se hace referencia en un **evento** solo se reproduce cuando se recibe un comando de script específico.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-127">A stream referenced in an **EVENT** plays only when a specific script command is received.</span></span> <span data-ttu-id="f9f0b-128">Por ejemplo, cuando Windows Media Player recibe un comando de script con la cadena de tipo "EVENT" y la cadena de comando "Adlink", busca los siguientes elementos en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-128">For example, when Windows Media Player receives a script command with type string "EVENT" and the command string "Adlink", it searches the playlist for the following elements.</span></span>


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



<span data-ttu-id="f9f0b-129">Windows Media Player, a continuación, cambia de la secuencia en directo para reproducir la secuencia o el archivo multimedia contenidos en el **evento**, en este caso Adlink. WMA.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-129">Windows Media Player then switches from the live stream to play the stream or media file contained in the **EVENT**, in this case Adlink.wma.</span></span> <span data-ttu-id="f9f0b-130">El código `WHENDONE="RESUME"` indica a Windows Media Player que reanude la reproducción de la secuencia anterior cuando Adlink. WMA ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-130">The code `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous stream when Adlink.wma is finished.</span></span>

> [!Note]  
> <span data-ttu-id="f9f0b-131">Si no se controla cada evento incrustado en una secuencia de medios o en un archivo multimedia, pueden producirse resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-131">Failure to handle every event embedded in a media stream or media file may yield unexpected results.</span></span>

 

<span data-ttu-id="f9f0b-132">Si desea usar el cambio de secuencia de eventos en directo, debe incluir un elemento de **evento** en la lista de reproducción para controlar cada comando de script de eventos incrustado en los flujos multimedia o archivos multimedia de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-132">If you want to use live event stream switching, you must include one **EVENT** element in your playlist to handle each event script command embedded in the media streams or media files in your playlist.</span></span> <span data-ttu-id="f9f0b-133">Antes de crear la lista de reproducción, debe conocer los detalles sobre qué comandos de script están incrustados en el contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-133">Before you create your playlist, you must know the details about which script commands are embedded in your digital media content.</span></span> <span data-ttu-id="f9f0b-134">Si hay un comando de script de eventos que desea que Windows Media Player omita, incluya un elemento de **evento** en la lista de reproducción para controlar el evento, pero haga referencia a una dirección URL ficticia en el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-134">If there is an event script command that you want Windows Media Player to ignore, include an **EVENT** element in your playlist to handle the event, but reference a dummy URL in the event handler.</span></span>

## <a name="ad-insertion"></a><span data-ttu-id="f9f0b-135">Inserción de anuncio</span><span class="sxs-lookup"><span data-stu-id="f9f0b-135">Ad Insertion</span></span>

<span data-ttu-id="f9f0b-136">Esta técnica se puede usar para la inserción de anuncios.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-136">This technique can be used for ad insertion.</span></span> <span data-ttu-id="f9f0b-137">Por ejemplo, durante una difusión en Internet en directo de un juego de bola, se puede enviar un comando al principio de cada interrupción comercial que indique a cada cliente (Windows Media Player) que juegue los comerciales que aparecen en su lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-137">For example, during a live Internet broadcast of a ball game, a command can be sent at the beginning of every commercial break that instructs each client (Windows Media Player) to play commercials listed in its playlist.</span></span> <span data-ttu-id="f9f0b-138">Cuando los clientes finalizan la reproducción de los comerciales, la lista de reproducción indica a cada cliente que vuelva a la difusión en directo.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-138">When clients finish playing the commercials, the playlist instructs each client to cut back to the live broadcast.</span></span> <span data-ttu-id="f9f0b-139">El contenido de los medios de **evento** solo se representará cuando el medio de streaming al que se tiene acceso difunde scripting incrustado con el nombre de **evento** correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-139">The **EVENT** media content will be rendered only when the streaming media being accessed broadcasts embedded scripting with the matching **EVENT** name.</span></span>

<span data-ttu-id="f9f0b-140">Las posibilidades inherentes al cambio de **eventos** se aprecian mejor al contrastar el modo en que los anuncios llegan a los visores a través de la difusión estándar y por aire con el modo en que los anuncios pueden llegar a los visores mediante tecnologías de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-140">The possibilities inherent in **EVENT** switching are best appreciated by contrasting how ads reach viewers through standard, over-the-air broadcasting with how ads can reach viewers using Windows Media Technologies.</span></span> <span data-ttu-id="f9f0b-141">Históricamente, los anuncios de difusión solo podían estar dirigidos aproximadamente a visores, con los datos de clasificación como criterio principal.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-141">Historically, broadcast ads could only be roughly targeted at viewers, using ratings data as the primary criteria.</span></span> <span data-ttu-id="f9f0b-142">Los anuncios enviados mediante tecnologías de Windows Media pueden estar dirigidos directamente al usuario de destino, ya que los **eventos** y las listas de reproducción se pueden crear sobre la marcha en función de los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-142">Ads sent using Windows Media Technologies can be aimed directly at the target user because **EVENTs** and playlists can be built on the fly based on user input.</span></span> <span data-ttu-id="f9f0b-143">Para obtener más información, consulte [Personalización de la entrega de contenido multimedia](personalizing-media-delivery.md).</span><span class="sxs-lookup"><span data-stu-id="f9f0b-143">For more information, see [Personalizing Media Delivery](personalizing-media-delivery.md).</span></span>

<span data-ttu-id="f9f0b-144">También puede utilizar listas de reproducción de metarchivos para mostrar gráficos, audio y texto personalizados para publicidad.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-144">You can also use metafile playlists to display customized graphics, audio and text for advertising.</span></span> <span data-ttu-id="f9f0b-145">Puede usar el elemento **banner** como un elemento secundario de un **evento** para mostrar un gráfico de mensaje de anuncio.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-145">You can use the **BANNER** element as a child element of an **EVENT** to display an advertising message graphic.</span></span> <span data-ttu-id="f9f0b-146">El elemento **banner** proporciona la ruta de acceso y el archivo que contiene los gráficos de la pancarta de publicidad.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-146">The **BANNER** element provides the path and file containing the graphics for your advertising banner.</span></span> <span data-ttu-id="f9f0b-147">También puede proporcionar un vínculo a un sitio o archivo mediante el elemento secundario **MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="f9f0b-147">You can also provide a link to a site or file using the **MOREINFO** child element.</span></span> <span data-ttu-id="f9f0b-148">La dirección URL en el elemento **MOREINFO** puede proporcionar un vínculo a incluso más anuncios en la Web.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-148">The URL in the **MOREINFO** element can provide a link to even more advertisements on the Web.</span></span> <span data-ttu-id="f9f0b-149">En el siguiente ejemplo se muestra el uso de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-149">The following example demonstrates using these elements.</span></span>

<span data-ttu-id="f9f0b-150">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9f0b-150">Example Code</span></span>


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



<span data-ttu-id="f9f0b-151">En el ejemplo siguiente se inserta ad Advert. WMA en el flujo de unidifusión de difusión BallGame cuando un cliente recibe un **evento** de comando de script con el atributo de **nombre** establecido en "tiempo de espera".</span><span class="sxs-lookup"><span data-stu-id="f9f0b-151">The following example inserts the ad Advert.wma into the broadcast unicast stream BallGame when a client receives a script command **EVENT** with the **NAME** attribute set to "Time-Out".</span></span> <span data-ttu-id="f9f0b-152">**CLIENTSKIP** está establecido en no para evitar que se omita el anuncio transmitido.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-152">**CLIENTSKIP** is set to NO to prevent the streamed ad from being skipped.</span></span> <span data-ttu-id="f9f0b-153">En este ejemplo, el anuncio transmitido por secuencias debe reproducirse antes de volver a la secuencia original.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-153">In this example, the streamed ad must be played before returning to the original stream.</span></span> <span data-ttu-id="f9f0b-154">Cuando finaliza el anuncio, el cliente reanuda la reproducción de la secuencia original.</span><span class="sxs-lookup"><span data-stu-id="f9f0b-154">When the ad is finished, the client resumes playing the original stream.</span></span>

<span data-ttu-id="f9f0b-155">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9f0b-155">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="f9f0b-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9f0b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9f0b-157">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="f9f0b-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f9f0b-158">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="f9f0b-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f9f0b-159">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f9f0b-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f9f0b-160">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f9f0b-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




