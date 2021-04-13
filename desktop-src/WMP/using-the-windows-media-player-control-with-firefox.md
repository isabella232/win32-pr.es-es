---
title: Uso del control de Media Player de Windows con Firefox
description: Uso del control de Media Player de Windows con Firefox
ms.assetid: a95529d6-7508-4e27-adfe-bbbf4dcaffce
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
ms.openlocfilehash: 253dd21312409fe2c97bf94c36397efed8353bdb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421531"
---
# <a name="using-the-windows-media-player-control-with-firefox"></a><span data-ttu-id="b113b-123">Uso del control de Media Player de Windows con Firefox</span><span class="sxs-lookup"><span data-stu-id="b113b-123">Using the Windows Media Player Control with Firefox</span></span>

<span data-ttu-id="b113b-124">Microsoft proporciona un complemento que le permite incrustar el control ActiveX de Windows Media Player en una página web para que se muestre correctamente en un explorador Firefox.</span><span class="sxs-lookup"><span data-stu-id="b113b-124">Microsoft provides a plug-in that enables you to embed the Windows Media Player ActiveX control in a webpage so that it will be displayed correctly by a Firefox browser.</span></span> <span data-ttu-id="b113b-125">El complemento, que se debe instalar en el equipo cliente, se puede descargar desde el [sitio web de Microsoft Port25](https://www.mozilla.org/).</span><span class="sxs-lookup"><span data-stu-id="b113b-125">The plug-in, which must be installed on the client computer, can be downloaded from the [Microsoft Port25 website](https://www.mozilla.org/).</span></span>

<span data-ttu-id="b113b-126">Para obtener información sobre el explorador Firefox, consulte el [sitio web de Firefox](https://www.mozilla.org/).</span><span class="sxs-lookup"><span data-stu-id="b113b-126">For information about the Firefox browser, see the [Firefox website](https://www.mozilla.org/).</span></span>

<span data-ttu-id="b113b-127">Para obtener más información sobre el uso de Windows Media Player con Firefox, consulte la sección Media Player de Windows del [sitio web de mozillaZine](http://kb.mozillazine.org/Windows_Media_Player).</span><span class="sxs-lookup"><span data-stu-id="b113b-127">For more information about using Windows Media Player with Firefox, see the Windows Media Player section of the [mozillaZine website](http://kb.mozillazine.org/Windows_Media_Player).</span></span>

<span data-ttu-id="b113b-128">En los temas siguientes se describe cómo insertar el control Media Player de Windows en una página web que se puede mostrar correctamente en Internet Explorer y Firefox.</span><span class="sxs-lookup"><span data-stu-id="b113b-128">The following topics describe how to embed the Windows Media Player control in a webpage that can be displayed correctly by both Internet Explorer and Firefox.</span></span>



| <span data-ttu-id="b113b-129">Tema</span><span class="sxs-lookup"><span data-stu-id="b113b-129">Topic</span></span>                                                                                                                                    | <span data-ttu-id="b113b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b113b-130">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b113b-131">Incrustar el control Player en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="b113b-131">Embedding the Player Control in a Web Page Displayed by Firefox</span></span>](embedding-the-player-control-in-a-web-page-displayed-by-firefox.md)   | <span data-ttu-id="b113b-132">Describe cómo escribir el script que crea un elemento de objeto que es compatible con Internet Explorer y Firefox.</span><span class="sxs-lookup"><span data-stu-id="b113b-132">Describes how write script that creates an OBJECT element that is compatible with both Internet Explorer and Firefox.</span></span> |
| [<span data-ttu-id="b113b-133">Usar elementos PARAM en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="b113b-133">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>](using-param-elements-in-a-web-page-displayed-by-firefox.md)                   | <span data-ttu-id="b113b-134">Describe los elementos de parámetro admitidos por el complemento de Firefox.</span><span class="sxs-lookup"><span data-stu-id="b113b-134">Describes the PARAM elements that are supported by the Firefox plug-in.</span></span>                                               |
| [<span data-ttu-id="b113b-135">Uso de scripts en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="b113b-135">Using Script in a Web Page Displayed by Firefox</span></span>](using-script-in-a-web-page-displayed-by-firefox.md)                                   | <span data-ttu-id="b113b-136">Describe los objetos de Media Player de Windows compatibles con el complemento de Firefox.</span><span class="sxs-lookup"><span data-stu-id="b113b-136">Describes the Windows Media Player objects that are supported by the Firefox plug-in.</span></span>                                 |
| [<span data-ttu-id="b113b-137">Control de eventos en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="b113b-137">Handling Events in a Web Page Displayed by Firefox</span></span>](handling-events-in-a-web-page-displayed-by-firefox.md)                             | <span data-ttu-id="b113b-138">Describe cómo escribir un script, en una página web que se muestra en Firefox, que controla los eventos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b113b-138">Describes how to write script, in a webpage displayed by Firefox, that handles Windows Media Player events.</span></span>           |
| [<span data-ttu-id="b113b-139">Uso de la propiedad invokeURLs en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="b113b-139">Using the invokeURLs Property in a Web Page Displayed by Firefox</span></span>](using-the-invokeurls-property-in-a-web-page-displayed-by-firefox.md) | <span data-ttu-id="b113b-140">Describe cómo responder a los comandos de script de tipo URL en una página web que se muestra en Firefox.</span><span class="sxs-lookup"><span data-stu-id="b113b-140">Describes how to respond to URL-type script commands in a webpage displayed by Firefox.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="b113b-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b113b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b113b-142">**Usar el control Media Player de Windows en una página web**</span><span class="sxs-lookup"><span data-stu-id="b113b-142">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




