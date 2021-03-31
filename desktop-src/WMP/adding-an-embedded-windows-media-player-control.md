---
title: Agregar un control de Media Player de Windows incrustado
description: Agregar un control de Media Player de Windows incrustado
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Listas de reproducción de metarchivos de Windows Media, agregar controles de Media Player de Windows incrustados
- listas de reproducción, agregar controles de Media Player de Windows incrustados
- listas de reproducción de metarchivos, agregar controles de Media Player de Windows incrustados
- Listas de reproducción de metarchivo de Windows Media, controles de Media Player de Windows incrustados
- listas de reproducción, controles de Media Player de Windows incrustados
- listas de reproducción de metarchivos, controles de Media Player de Windows incrustados
- Agregar controles de Media Player de Windows incrustados
- controles de Media Player de Windows incrustados
- Windows Media Player, agregar controles incrustados
- Windows Media Player, controles incrustados
- HTMLView, agregar controles de Media Player de Windows incrustados
- HTMLView, controles de Windows Media Player insertados
- HTMLView, modelo de objetos de Windows Media Player
- HTMLView, modelo de objetos de Player
- Modelo de objetos de Windows Media Player, acerca de
- modelo de objetos, acerca de
- Objeto Player
- Windows Media, modelo de objetos de reproductor
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418904"
---
# <a name="adding-an-embedded-windows-media-player-control"></a><span data-ttu-id="586a8-121">Agregar un control de Media Player de Windows incrustado</span><span class="sxs-lookup"><span data-stu-id="586a8-121">Adding an Embedded Windows Media Player Control</span></span>

<span data-ttu-id="586a8-122">Hay dos razones por las que podría considerar la posibilidad de agregar una instancia incrustada de Windows Media Player a la presentación de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="586a8-122">There are two reasons you might consider adding an embedded instance of Windows Media Player to your HTMLView presentation.</span></span> <span data-ttu-id="586a8-123">En primer lugar, si desea mostrar el contenido de vídeo, debe utilizar el control ActiveX de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="586a8-123">First, if you want to display video content, you need to use the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="586a8-124">En segundo lugar, si desea sacar partido de las características del modelo de objetos de Windows Media Player desde la Página Web de HTMLView, debe usar una instancia del control del reproductor para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="586a8-124">Second, if you want to take advantage of features of the Windows Media Player object model from within your HTMLView webpage, you must use an instance the Player control to do so.</span></span>

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a><span data-ttu-id="586a8-125">Usar el control Player para mostrar vídeo en el contenido de HTMLView</span><span class="sxs-lookup"><span data-stu-id="586a8-125">Using the Player control to display video in HTMLView content</span></span>

<span data-ttu-id="586a8-126">Normalmente, Windows Media Player muestra vídeo con el panel de vídeo y visualización de la característica de **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="586a8-126">Usually, Windows Media Player displays video using the Video and Visualization pane of the **Now Playing** feature.</span></span> <span data-ttu-id="586a8-127">Puesto que HTMLView usa esta área para mostrar la página web, debe proporcionar un área de presentación de vídeo adicional si desea que el reproductor Reproduzca vídeo.</span><span class="sxs-lookup"><span data-stu-id="586a8-127">Since HTMLView uses this area to display your webpage, you must supply an additional video display area if you want the Player to play video.</span></span> <span data-ttu-id="586a8-128">Esto es fácil de hacer mediante el control ActiveX de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="586a8-128">This is easy to do by using the Windows Media Player ActiveX control.</span></span>

<span data-ttu-id="586a8-129">Para usar el control de reproducción para mostrar vídeo, inserte el control en la Página Web de HTMLView mediante la etiqueta de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="586a8-129">To use the Player control to display video, embed the control in your HTMLView webpage by using the **OBJECT** tag.</span></span> <span data-ttu-id="586a8-130">Se trata de la misma técnica que se usa para incrustar el control de reproductor en cualquier página web en la que desee mostrar vídeo.</span><span class="sxs-lookup"><span data-stu-id="586a8-130">This is the same technique you use to embed the Player control into any webpage in which you want to display video.</span></span> <span data-ttu-id="586a8-131">En el ejemplo de código siguiente se muestra la sintaxis básica para insertar el control Player en Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="586a8-131">The following example code shows the basic syntax for embedding the Player control in Internet Explorer:</span></span>


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



<span data-ttu-id="586a8-132">El parámetro de *Inicio automático* garantiza que el contenido se reproduzca automáticamente cada vez que se especifique una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="586a8-132">The *autoStart* parameter ensures that content plays automatically whenever a new URL is specified.</span></span> <span data-ttu-id="586a8-133">El valor que especifique para *uiMode* depende de usted, pero normalmente querrá especificar "none" al crear contenido para las presentaciones de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="586a8-133">The value you specify for *uiMode* is up to you, but you will usually want to specify "none" when creating content for HTMLView presentations.</span></span> <span data-ttu-id="586a8-134">Al incrustar el control Media Player de Windows para mostrar vídeo de esta manera, el usuario puede controlar la reproducción mediante los controles del reproductor en modo completo, por lo que no es necesario proporcionar controles de transporte adicionales en la Página Web.</span><span class="sxs-lookup"><span data-stu-id="586a8-134">When you embed the Windows Media Player control to display video in this manner, the user can control playback using the controls of the full-mode Player, so there's no need to provide additional transport controls in the webpage.</span></span> <span data-ttu-id="586a8-135">Puede usar el espacio que normalmente asignaría a los controles de transporte para mostrar más texto, gráficos o vínculos a otro contenido.</span><span class="sxs-lookup"><span data-stu-id="586a8-135">You can use the space you would usually allocate for transport controls to display more text, graphics, or links to other content.</span></span>

<span data-ttu-id="586a8-136">No especifique un parámetro de *dirección URL* al insertar el control Media Player de Windows en una página web diseñada para mostrarse en una presentación de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="586a8-136">Do not specify a *URL* parameter when embedding the Windows Media Player control in a webpage designed to display in an HTMLView presentation.</span></span> <span data-ttu-id="586a8-137">En su lugar, especifique los archivos multimedia digitales en el archivo. ASX que abre el contenido.</span><span class="sxs-lookup"><span data-stu-id="586a8-137">Instead, specify the digital media files in the .asx file that opens the content.</span></span>

<span data-ttu-id="586a8-138">Dado que proporciona la región de presentación de vídeo en la Página Web de HTMLView, puede decidir dónde colocar el vídeo y el tamaño que desea que tenga la región de visualización.</span><span class="sxs-lookup"><span data-stu-id="586a8-138">Because you provide the video display region in your HTMLView webpage, you can decide where to position the video and how large you want the display region to be.</span></span> <span data-ttu-id="586a8-139">Por ejemplo, puede contener el objeto **Player** dentro de un elemento HTML **div** y, a continuación, especificar la posición del **div** para situar la presentación de vídeo en la Página Web.</span><span class="sxs-lookup"><span data-stu-id="586a8-139">For example, you can contain the **Player** object within an HTML **DIV** element and then specify the position for the **DIV** to situate the video display on the webpage.</span></span> <span data-ttu-id="586a8-140">Puede cambiar las dimensiones de la presentación de vídeo especificando los valores de los atributos de alto y ancho del elemento de **objeto** .</span><span class="sxs-lookup"><span data-stu-id="586a8-140">You can change the dimensions of the video display by specifying values for the height and width attributes of the **OBJECT** element.</span></span> <span data-ttu-id="586a8-141">También puede especificar estos valores mediante el código de script.</span><span class="sxs-lookup"><span data-stu-id="586a8-141">You can also specify these values using script code.</span></span>

## <a name="using-the-player-object-model"></a><span data-ttu-id="586a8-142">Usar el modelo de objetos Player</span><span class="sxs-lookup"><span data-stu-id="586a8-142">Using the Player object model</span></span>

<span data-ttu-id="586a8-143">El modelo de objetos de Windows Media Player expone propiedades, métodos y eventos que se pueden usar en las páginas web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="586a8-143">The Windows Media Player object model exposes properties, methods, and events that you can use in your HTMLView webpages.</span></span> <span data-ttu-id="586a8-144">Al incrustar el control ActiveX de Windows Media Player en la Página Web de HTMLView, tiene acceso automáticamente al modelo de objetos de Player.</span><span class="sxs-lookup"><span data-stu-id="586a8-144">When you embed the Windows Media Player ActiveX control in your HTMLView webpage, you automatically have access to the Player object model.</span></span>

<span data-ttu-id="586a8-145">Si incrusta el control Media Player de Windows en la Página Web de HTMLView, no use el modelo de objetos del reproductor para especificar el archivo multimedia digital que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="586a8-145">If you embed the Windows Media Player control in your HTMLView webpage, do not use the Player object model to specify the digital media file to be played.</span></span> <span data-ttu-id="586a8-146">Por ejemplo, si utiliza código de script para especificar un valor para la propiedad **URL** del control incrustado, la Página Web de HTMLView se descargará de la característica **reproducción en curso** cuando se reproduzca el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="586a8-146">For example, if you use script code to specify a value for the **URL** property of the embedded control, your HTMLView webpage will be unloaded from the **Now Playing** feature when the digital media file plays.</span></span> <span data-ttu-id="586a8-147">Para evitar que esto suceda, abra siempre los archivos. ASX que incluyen los parámetros HTMLView cuando necesite usar el script para abrir el contenido multimedia digital de la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="586a8-147">To prevent this from happening, always open .asx files that include HTMLView parameters when you need to use script to open digital media content from your HTMLView webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="586a8-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="586a8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="586a8-149">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="586a8-149">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="586a8-150">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="586a8-150">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="586a8-151">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="586a8-151">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="586a8-152">**Configuración. Inicio automático**</span><span class="sxs-lookup"><span data-stu-id="586a8-152">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 




