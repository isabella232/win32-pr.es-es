---
title: Uso de la propiedad invokeURLs en una página web que se muestra en Firefox
description: Uso de la propiedad invokeURLs en una página web que se muestra en Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX de Windows Media Player, propiedad invokeURLs
- Control ActiveX móvil de Windows Media Player, propiedad invokeURLs
- incrustación, páginas web
- Incrustación de páginas web, propiedad invokeURLs
- Windows Media Player, Firefox
- Modelo de objetos de Windows Media Player, Firefox
- modelo de objetos, Firefox
- Control ActiveX de Windows Media Player, Firefox
- Control ActiveX, Firefox
- Firefox, propiedad invokeURLs
- Incrustación de páginas web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0a2eb96e65d8fa6d2758669e3c844b2d13c0bc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105704822"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="6fcda-122">Uso de la propiedad invokeURLs en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="6fcda-122">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="6fcda-123">Algunos archivos multimedia contienen direcciones URL incrustadas en las que Windows Media Player muestra las páginas web en una ventana o un marco del explorador Web a medida que se reproduce el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="6fcda-123">Some media files contain embedded URLs for which Windows Media Player displays webpages in a Web browser window or frame as the media file plays.</span></span> <span data-ttu-id="6fcda-124">En Windows Internet Explorer, puede usar la propiedad [Settings. invokeURLs](settings-invokeurls.md) para especificar si las páginas se muestran para las direcciones URL incrustadas, y puede usar la propiedad [Settings. defaultFrame](settings-defaultframe.md) para especificar un marco para mostrar dichas páginas.</span><span class="sxs-lookup"><span data-stu-id="6fcda-124">In Windows Internet Explorer, you can use the [Settings.invokeURLs](settings-invokeurls.md) property to specify whether pages are displayed for embedded URLs, and you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify a frame for displaying such pages.</span></span>

<span data-ttu-id="6fcda-125">En Firefox, se necesitan algunas soluciones alternativas para establecer la propiedad **invokeURLs** y especificar un marco para mostrar las páginas de las direcciones URL incrustadas.</span><span class="sxs-lookup"><span data-stu-id="6fcda-125">In Firefox, some workarounds are required to set the **invokeURLs** property and to specify a frame for displaying pages for embedded URLs.</span></span>

## <a name="setting-the-invokeurls-property"></a><span data-ttu-id="6fcda-126">Establecimiento de la propiedad invokeURLs</span><span class="sxs-lookup"><span data-stu-id="6fcda-126">Setting the invokeURLs property</span></span>

<span data-ttu-id="6fcda-127">El valor predeterminado de la propiedad **Settings. invokeURLs** es true, por lo que si desea que el valor sea false, debe establecerlo explícitamente.</span><span class="sxs-lookup"><span data-stu-id="6fcda-127">The default value of the **Settings.invokeURLs** property is true, so if you want the value to be false, you must set it explicitly.</span></span> <span data-ttu-id="6fcda-128">En Internet Explorer, puede establecer **invokeURLs** en false en un elemento Param dentro del elemento de objeto del control Player.</span><span class="sxs-lookup"><span data-stu-id="6fcda-128">In Internet Explorer, you can set **invokeURLs** to false in a PARAM element inside the Player control's OBJECT element.</span></span>

<span data-ttu-id="6fcda-129">El complemento de Firefox no admite el establecimiento de la propiedad **invokeURLs** en un elemento Param.</span><span class="sxs-lookup"><span data-stu-id="6fcda-129">The Firefox plug-in does not support setting the **invokeURLs** property in a PARAM element.</span></span>

<span data-ttu-id="6fcda-130">Para solucionar esta limitación, puede establecer la propiedad **invokeURLs** en el script.</span><span class="sxs-lookup"><span data-stu-id="6fcda-130">You can work around this limitation by setting the **invokeURLs** property in script.</span></span> <span data-ttu-id="6fcda-131">En el código siguiente se muestra cómo establecer la propiedad **invokeURLs** en false en una página web que se puede mostrar con Internet Explorer y Firefox.</span><span class="sxs-lookup"><span data-stu-id="6fcda-131">The following code shows how to set the **invokeURLs** property to false in a webpage that can be displayed by both Internet Explorer and Firefox.</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

  </BODY>
</HTML>

```



## <a name="displaying-webpages-in-a-frame"></a><span data-ttu-id="6fcda-132">Mostrar páginas web en un marco</span><span class="sxs-lookup"><span data-stu-id="6fcda-132">Displaying webpages in a frame</span></span>

<span data-ttu-id="6fcda-133">Un archivo multimedia puede contener direcciones URL que muestren páginas web en una ventana o marco del explorador cuando se reproduzca el archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="6fcda-133">A media file can contain URLs that display webpages in a browser window or frame as the media file is played.</span></span> <span data-ttu-id="6fcda-134">En Internet Explorer, puede usar la propiedad [Settings. defaultFrame](settings-defaultframe.md) para especificar el marco en el que se muestran esas páginas.</span><span class="sxs-lookup"><span data-stu-id="6fcda-134">In Internet Explorer, you can use the [Settings.defaultFrame](settings-defaultframe.md) property to specify the frame in which those pages are displayed.</span></span> <span data-ttu-id="6fcda-135">Si no establece la propiedad **defaultFrame** , las direcciones URL se muestran en una ventana independiente del explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6fcda-135">If you do not set the **defaultFrame** property, URLs are displayed in a separate window of the default browser.</span></span> <span data-ttu-id="6fcda-136">Sin embargo, el complemento de Firefox no admite la propiedad **Settings. defaultFrame** .</span><span class="sxs-lookup"><span data-stu-id="6fcda-136">However, the Firefox plug-in does not support the **Settings.defaultFrame** property.</span></span> <span data-ttu-id="6fcda-137">Para evitar esta limitación, establezca la propiedad **Settings. invokeURLs** en false y escriba un controlador de eventos [comando](player-player-scriptcommand.md) que establezca la ubicación del marco de destino.</span><span class="sxs-lookup"><span data-stu-id="6fcda-137">To work around this limitation, set the **Settings.invokeURLs** property to false and write a [ScriptCommand](player-player-scriptcommand.md) event handler that sets the location of the target frame.</span></span> <span data-ttu-id="6fcda-138">En el ejemplo siguiente, que funciona en Internet Explorer y Firefox, se ilustra esta técnica.</span><span class="sxs-lookup"><span data-stu-id="6fcda-138">The following example, which works in Internet Explorer and Firefox, illustrates this technique.</span></span> <span data-ttu-id="6fcda-139">Supongamos que la página web que se muestra en el ejemplo está en los marcos \[ 0 \] y desea que la página de la dirección URL se muestre en los marcos \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="6fcda-139">Assume that the webpage shown in the example is in frames\[0\] and you want the URL's page to be displayed in frames\[1\].</span></span>


```HTML
<HTML>
  <BODY OnLoad="Initialize()">

    <SCRIPT type="text/javascript">

      document.write('<OBJECT id="Player"'); 

      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {               
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');       
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {      
        document.write(' type="application/x-ms-wmp"');        
      }  

      document.write(' width=300 height=200>');
      document.write('<PARAM name="autoStart" value="false"/>');
      document.write('<PARAM name="url" value="c:\\MediaFiles\\Glass.wmv"/>');
      document.write('</OBJECT>'); 
      
    </SCRIPT>

    <SCRIPT>
      function Initialize()
      {
        Player.settings.invokeURLs = false;
        Player.controls.play();
      }
    </SCRIPT>

    <SCRIPT for="Player" event="ScriptCommand(scType, scParam)">
      if( scType == "URL" )
      {
        parent.frames[1].location = scParam;
      }
    </script>

  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="6fcda-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fcda-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fcda-141">**Uso del control de Media Player de Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="6fcda-141">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




