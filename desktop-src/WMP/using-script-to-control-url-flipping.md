---
title: Usar script para controlar el volteo de URL
description: Usar script para controlar el volteo de URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, presentaciones basadas en Web
- Modelo de objetos de Windows Media Player, presentaciones basadas en Web
- modelo de objetos, presentaciones basadas en Web
- Windows Media Player presentaciones móviles y basadas en Web
- Control ActiveX de Windows Media Player, presentaciones basadas en Web
- Control ActiveX móvil de Windows Media Player, presentaciones basadas en Web
- Control ActiveX, presentaciones basadas en Web
- Media Player de Windows, volteo de URL
- Modelo de objetos de Windows Media Player, volteo de direcciones URL
- modelo de objetos, volteo de URL
- Windows Media Player Mobile, volteo de direcciones URL
- Control ActiveX de Windows Media Player, volteo de direcciones URL
- Control ActiveX móvil de Windows Media Player, volteo de direcciones URL
- Control ActiveX, volteo de direcciones URL
- Presentaciones basadas en Web, volteo de direcciones URL
- crear presentaciones basadas en Web, volteo de direcciones URL
- Volteo de URL
- Windows Media Player, transmisión por secuencias multimedia enriquecida
- Modelo de objetos de Windows Media Player, transmisión por secuencias multimedia enriquecida
- modelo de objetos, streaming multimedia enriquecido
- Windows Media Player Mobile, streaming multimedia enriquecido
- Control ActiveX de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX móvil de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX, transmisión por secuencias multimedia enriquecida
- Presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- crear presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- transmisión por secuencias multimedia enriquecida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104419233"
---
# <a name="using-script-to-control-url-flipping"></a><span data-ttu-id="1c2e9-130">Usar script para controlar el volteo de URL</span><span class="sxs-lookup"><span data-stu-id="1c2e9-130">Using Script to Control URL Flipping</span></span>

<span data-ttu-id="1c2e9-131">Cuando un usuario se conecta a una secuencia multimedia enriquecida mientras la secuencia ya está en curso, es posible que la página web transmitida se muestre antes de que todos los elementos hayan llegado y estén almacenados en caché si Windows Media Player invoca automáticamente la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-131">When a user connects to a rich media stream while the stream is already in progress, it is possible for the streamed webpage to display before all the elements have arrived and been cached if Windows Media Player automatically invokes the URL.</span></span> <span data-ttu-id="1c2e9-132">Cuando esto sucede, el usuario ve una página web en blanco o incompleta hasta que llega el siguiente conjunto de datos en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-132">When this happens, the user sees a blank or incomplete webpage until the next set of data arrives in the cache.</span></span>

<span data-ttu-id="1c2e9-133">Puede evitar que se muestre una página web en blanco o incompleta mediante la invocación de la dirección URL mediante el script en lugar de permitir que Windows Media Player lo haga automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-133">You can avoid displaying a blank or incomplete webpage by invoking the URL using script instead of letting Windows Media Player do it automatically.</span></span> <span data-ttu-id="1c2e9-134">De este modo, puede omitir la primera dirección URL voltear y, a continuación, invocar las direcciones URL subsiguientes mediante el código de script.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-134">That way, you can ignore the first URL flip and then invoke subsequent URLs by using script code.</span></span>

> [!Note]  
> <span data-ttu-id="1c2e9-135">En esta sección se supone que está transmisiones por secuencias de HTML mediante el SDK de Windows Media Encoder 9 series y que ha configurado la secuencia HTML para que se repita.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-135">This section assumes that you are streaming HTML using the Windows Media Encoder 9 Series SDK and that you have set the HTML stream to repeat.</span></span>

 

<span data-ttu-id="1c2e9-136">En primer lugar, debe crear una página web de conjuntos de marcos que contenga el marco con el reproductor incrustado y el marco que muestra el código HTML de streaming.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-136">First, you must create a frameset webpage to contain the frame with the embedded Player and the frame that displays the streaming HTML.</span></span> <span data-ttu-id="1c2e9-137">Cada uno de estos dos marcos mostrará una página web independiente inicialmente, por lo que creará un total de tres páginas Web.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-137">Each of these two frames will display a separate webpage initially, so you will create a total of three webpages.</span></span> <span data-ttu-id="1c2e9-138">En el ejemplo de código siguiente se muestra la página web FRAMESET:</span><span class="sxs-lookup"><span data-stu-id="1c2e9-138">The following example code demonstrates the frameset webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



<span data-ttu-id="1c2e9-139">En el ejemplo anterior de la página web se incorporan dos fotogramas.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-139">The preceding webpage example incorporates two frames.</span></span> <span data-ttu-id="1c2e9-140">El primer fotograma se muestra en la mitad izquierda de la ventana del explorador y muestra la página web denominada embed \_player.htm.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-140">The first frame displays in the left half of the browser window and displays the webpage named embed\_player.htm.</span></span> <span data-ttu-id="1c2e9-141">En el código de ejemplo siguiente se crea esta página web:</span><span class="sxs-lookup"><span data-stu-id="1c2e9-141">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="1c2e9-142">El segundo fotograma del cuadro de marcos se muestra en la mitad derecha de la ventana del explorador y muestra una página web denominada "blank.htm".</span><span class="sxs-lookup"><span data-stu-id="1c2e9-142">The second frame in the frameset displays in the right half of the browser window and displays a webpage named "blank.htm".</span></span> <span data-ttu-id="1c2e9-143">En el código de ejemplo siguiente se crea esta página web:</span><span class="sxs-lookup"><span data-stu-id="1c2e9-143">The following example code creates this webpage:</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



<span data-ttu-id="1c2e9-144">Cuando se carga la página de conjuntos de marcos en el explorador, el marco de la izquierda muestra el reproductor incrustado y el marco de la derecha muestra el texto "cargando..." para informar al usuario de que hay más datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-144">When the frameset page loads in the browser, the left frame shows the embedded Player and the right frame shows the text "Loading..." to inform the user that more data is forthcoming.</span></span> <span data-ttu-id="1c2e9-145">Cuando el primer comando de script de dirección URL llega de la secuencia HTML, el controlador de eventos simplemente cambia el valor de la marca **booleana** .</span><span class="sxs-lookup"><span data-stu-id="1c2e9-145">When the first URL script command arrives from the HTML stream, the event handler simply changes the value of the **Boolean** flag.</span></span> <span data-ttu-id="1c2e9-146">Cuando el siguiente comando de script de dirección URL llega de la secuencia HTML, el script del controlador de eventos carga la nueva dirección URL en el marco denominado "Content" y se muestra la página web completa en el marco situado en la mitad derecha de la ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-146">When each subsequent URL script command arrives from the HTML stream, the script in the event handler loads the new URL into the frame named "content", and the complete webpage displays in the frame located in the right half of the browser window.</span></span>

<span data-ttu-id="1c2e9-147">Para obtener más información acerca de la transmisión por secuencias de HTML con Windows Media, consulte el SDK de Windows Media Encoder.</span><span class="sxs-lookup"><span data-stu-id="1c2e9-147">For more information about streaming HTML using Windows Media, see the Windows Media Encoder SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c2e9-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c2e9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c2e9-149">**Transmisión por secuencias multimedia enriquecida**</span><span class="sxs-lookup"><span data-stu-id="1c2e9-149">**Rich Media Streaming**</span></span>](rich-media-streaming.md)
</dt> <dt>

[<span data-ttu-id="1c2e9-150">**Volteo de URL**</span><span class="sxs-lookup"><span data-stu-id="1c2e9-150">**URL Flipping**</span></span>](url-flipping.md)
</dt> </dl>

 

 




