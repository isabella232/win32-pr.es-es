---
title: Incrustar el control Player en una página web que se muestra en Firefox
description: Incrustar el control Player en una página web que se muestra en Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- Windows Media Player, Firefox
- Modelo de objetos de Windows Media Player, Firefox
- modelo de objetos, Firefox
- Windows Media Player Mobile, Firefox
- Control ActiveX de Windows Media Player, Firefox
- Control ActiveX móvil de Windows Media Player, Firefox
- Control ActiveX, Firefox
- Firefox, acerca de la inserción de páginas web
- incrustación, páginas web
- Incrustación de páginas web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105695491"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="5b141-123">Incrustar el control Player en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="5b141-123">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="5b141-124">Para insertar el control de Media Player de Windows en una página web que se puede mostrar en un explorador Firefox, cree un elemento de objeto o un elemento EMBED que tenga uno de los siguientes tipos MIME como su atributo de **tipo** :</span><span class="sxs-lookup"><span data-stu-id="5b141-124">To embed the Windows Media Player control in a webpage that can be displayed by a Firefox browser, create an OBJECT element or an EMBED element that has one of the following mime types as its **type** attribute:</span></span>

-   <span data-ttu-id="5b141-125">application/x-MS-WMP</span><span class="sxs-lookup"><span data-stu-id="5b141-125">application/x-ms-wmp</span></span>
-   <span data-ttu-id="5b141-126">aplicación/ASX</span><span class="sxs-lookup"><span data-stu-id="5b141-126">application/asx</span></span>
-   <span data-ttu-id="5b141-127">vídeo/x-MS-ASF-complemento</span><span class="sxs-lookup"><span data-stu-id="5b141-127">video/x-ms-asf-plugin</span></span>
-   <span data-ttu-id="5b141-128">application/x-Mplayer2</span><span class="sxs-lookup"><span data-stu-id="5b141-128">application/x-mplayer2</span></span>
-   <span data-ttu-id="5b141-129">vídeo/x-MS-ASF</span><span class="sxs-lookup"><span data-stu-id="5b141-129">video/x-ms-asf</span></span>
-   <span data-ttu-id="5b141-130">vídeo/x-MS-WM</span><span class="sxs-lookup"><span data-stu-id="5b141-130">video/x-ms-wm</span></span>
-   <span data-ttu-id="5b141-131">audio/x-MS-WMA</span><span class="sxs-lookup"><span data-stu-id="5b141-131">audio/x-ms-wma</span></span>
-   <span data-ttu-id="5b141-132">audio/x-MS-Wax</span><span class="sxs-lookup"><span data-stu-id="5b141-132">audio/x-ms-wax</span></span>
-   <span data-ttu-id="5b141-133">vídeo/x-MS-WMV</span><span class="sxs-lookup"><span data-stu-id="5b141-133">video/x-ms-wmv</span></span>
-   <span data-ttu-id="5b141-134">vídeo/x-MS-wvx</span><span class="sxs-lookup"><span data-stu-id="5b141-134">video/x-ms-wvx</span></span>

<span data-ttu-id="5b141-135">El tipo MIME preferido es application/x-MS-wmp.</span><span class="sxs-lookup"><span data-stu-id="5b141-135">The preferred mime type is application/x-ms-wmp.</span></span>

<span data-ttu-id="5b141-136">En los siguientes ejemplos se muestra cómo incrustar el control Player mediante un elemento OBJECT o un elemento EMBED.</span><span class="sxs-lookup"><span data-stu-id="5b141-136">The following examples show how to embed the Player control using an OBJECT element or an EMBED element.</span></span>


```HTML
<OBJECT id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320">
  <PARAM name="autostart" value="false"/>
</OBJECT>

<EMBED id="Player"
  type="application/x-ms-wmp" 
  width="320" height="320"
  autostart="false"/>

```



<span data-ttu-id="5b141-137">Los ejemplos anteriores funcionan en Firefox pero no en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b141-137">The preceeding examples work in Firefox but not in Internet Explorer.</span></span> <span data-ttu-id="5b141-138">Para insertar el control Player en una página web que puede mostrarse en Internet Explorer, debe crear un elemento de objeto que tenga un atributo **ClassID** establecido en el identificador de clase del control Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="5b141-138">To embed the Player control in a webpage that can be displayed by Internet Explorer, you must create an OBJECT element that has a **classid** attribute set to the class ID of the Windows Media Player control.</span></span>

<span data-ttu-id="5b141-139">En el ejemplo siguiente se muestra cómo insertar el control Media Player de Windows en una página web que se puede mostrar correctamente en Internet Explorer y Firefox.</span><span class="sxs-lookup"><span data-stu-id="5b141-139">The following example shows how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span> <span data-ttu-id="5b141-140">El script de la página detecta el tipo de explorador y genera la etiqueta de objeto adecuada.</span><span class="sxs-lookup"><span data-stu-id="5b141-140">Script on the page detects the browser type and generates the appropriate OBJECT tag.</span></span>


```HTML
<HTML>
  <BODY>
    <SCRIPT type="text/javascript">
      if(-1 != navigator.userAgent.indexOf("MSIE"))
      {
        document.write('<OBJECT id="Player"');
        document.write(' classid="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"');
        document.write(' width=300 height=200></OBJECT>');
      }
      else if(-1 != navigator.userAgent.indexOf("Firefox"))
      {
        document.write('<OBJECT id="Player"'); 
        document.write(' type="application/x-ms-wmp"'); 
        document.write(' width=300 height=200></OBJECT>');
      }         
    </SCRIPT>
  </BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="5b141-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b141-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b141-142">**Uso del control de Media Player de Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="5b141-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




