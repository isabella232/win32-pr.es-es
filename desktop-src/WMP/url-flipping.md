---
title: Volteo de URL
description: Volteo de URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "103780257"
---
# <a name="url-flipping"></a><span data-ttu-id="85b90-120">Volteo de URL</span><span class="sxs-lookup"><span data-stu-id="85b90-120">URL Flipping</span></span>

<span data-ttu-id="85b90-121">El uso de páginas web para presentaciones de diapositivas se denomina volteo de direcciones URL y Windows Media Player administra automáticamente cuando encuentra comandos de scripts de URL insertados en la secuencia de medios digitales que se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="85b90-121">Using webpages for slide shows is called URL flipping, and is handled automatically by Windows Media Player when it encounters URL script commands embedded in the digital media stream it is playing.</span></span> <span data-ttu-id="85b90-122">Puede especificar un marco de destino para las páginas en cada comando de script o puede especificarlo estableciendo la propiedad **Settings. defaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="85b90-122">You can specify a target frame for your pages in each script command, or you can specify it by setting the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="85b90-123">Puede establecer esta propiedad en el código de script o mediante un elemento PARAM dentro del elemento de objeto que incrusta el control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="85b90-123">You can set this property in script code or by using a PARAM element within the OBJECT element that embeds the Windows Media Player control.</span></span>

<span data-ttu-id="85b90-124">Puede controlar los comandos de script de dirección URL en el código JScript del mismo modo que administraría los comandos de script personalizados.</span><span class="sxs-lookup"><span data-stu-id="85b90-124">You are free to handle the URL script commands in your JScript code just as you would handle custom script commands.</span></span> <span data-ttu-id="85b90-125">Si desea que el control de Media Player de Windows omita los comandos de script de dirección URL para que pueda controlarlos completamente, establezca la *configuración*. la propiedad **invokeURLs** en false en el código de script o mediante un elemento Param como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="85b90-125">If you want the Windows Media Player control to ignore URL script commands so that you can handle them entirely by yourself, set the *Settings*.**invokeURLs** property to false either in script code or using a PARAM element as previously described.</span></span>

<span data-ttu-id="85b90-126">En el ejemplo siguiente se muestra un FRAMESET típico para el volteo de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="85b90-126">The following example illustrates a typical frameset for URL flipping.</span></span> <span data-ttu-id="85b90-127">En primer lugar, cree una página que describa el frameset:</span><span class="sxs-lookup"><span data-stu-id="85b90-127">First, create a page that describes the frameset:</span></span>


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



<span data-ttu-id="85b90-128">A continuación, cree el archivo player.html al que se hace referencia en el frameset mediante el código siguiente (se supone que el archivo video. wmv existe en el mismo directorio que los archivos HTML):</span><span class="sxs-lookup"><span data-stu-id="85b90-128">Next, create the player.html file referenced in the frameset by using the following code (the video.wmv file is assumed to exist in the same directory as the HTML files):</span></span>


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



<span data-ttu-id="85b90-129">Si las páginas web son lo suficientemente pequeñas para cargarse rápidamente, puede que esta configuración sea suficiente para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="85b90-129">If your webpages are small enough to load rapidly, this setup may be sufficient for your needs.</span></span> <span data-ttu-id="85b90-130">Por otro lado, si las páginas web son complejas, el streaming multimedia enriquecido puede ser más eficaz en función de la velocidad de conexión de la audiencia.</span><span class="sxs-lookup"><span data-stu-id="85b90-130">If, on the other hand, your webpages are complex, rich media streaming may be more effective depending on the connection speed of your audience.</span></span>

> [!Note]  
> <span data-ttu-id="85b90-131">El volteo de direcciones URL no funciona correctamente con las páginas que se ven en Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="85b90-131">URL flipping does not work correctly with pages viewed in Netscape Navigator.</span></span> <span data-ttu-id="85b90-132">En lugar de aparecer en el marco especificado por **defaultFrame**, cada comando de script de dirección URL recibido en el navegador muestra la dirección URL en una nueva ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="85b90-132">Instead of appearing in the frame specified by **defaultFrame**, each URL script command received in Navigator displays the URL in a new browser window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="85b90-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85b90-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b90-134">**Crear Web-Based presentaciones**</span><span class="sxs-lookup"><span data-stu-id="85b90-134">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="85b90-135">**Usar script para controlar el volteo de URL**</span><span class="sxs-lookup"><span data-stu-id="85b90-135">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




