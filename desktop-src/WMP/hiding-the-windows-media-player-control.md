---
title: Ocultar el control Media Player de Windows
description: Ocultar el control Media Player de Windows
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
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
- incrustación, páginas web
- Windows Media Player, ocultar el control ActiveX
- Modelo de objetos de Windows Media Player, ocultar el control ActiveX
- modelo de objetos, ocultar control ActiveX
- Windows Media Player Mobile, control hidingActiveX
- Control ActiveX de Windows Media Player, ocultar
- Control ActiveX móvil de Windows Media Player, ocultar
- Control ActiveX, ocultar
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- Incrustación de páginas web, ocultar controles ActiveX
- ocultar Windows Media Player control ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357467"
---
# <a name="hiding-the-windows-media-player-control"></a><span data-ttu-id="2485d-126">Ocultar el control Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="2485d-126">Hiding the Windows Media Player Control</span></span>

<span data-ttu-id="2485d-127">El objeto de Windows Media Player ActiveX se incrusta en una página web mediante el elemento de objeto.</span><span class="sxs-lookup"><span data-stu-id="2485d-127">The Windows Media Player ActiveX object is embedded in a webpage using the OBJECT element.</span></span> <span data-ttu-id="2485d-128">A diferencia de las versiones anteriores, el elemento de objeto que define Windows Media Player debe colocarse en la sección de cuerpo de una página web, entre las etiquetas <BODY> y </BODY> .</span><span class="sxs-lookup"><span data-stu-id="2485d-128">Unlike earlier versions, the OBJECT element that defines Windows Media Player must be placed in the BODY section of a webpage, between the <BODY> and </BODY> tags.</span></span> <span data-ttu-id="2485d-129">Colocar el objeto de Windows Media Player ActiveX en la sección de encabezado de una página web para ocultar la interfaz de usuario puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="2485d-129">Placing the Windows Media Player ActiveX object in the HEAD section of a webpage to hide the user interface can produce unexpected results.</span></span>

<span data-ttu-id="2485d-130">Si coloca el control ActiveX de Windows Media Player en la sección de cuerpo de una página web, se mostrará la interfaz de usuario del control.</span><span class="sxs-lookup"><span data-stu-id="2485d-130">If you put the Windows Media Player ActiveX control in the BODY section of a webpage, the control user interface will be displayed.</span></span> <span data-ttu-id="2485d-131">Si no desea que se muestre y desea crear su propia interfaz de usuario, establezca los atributos de alto y ancho del elemento de objeto en cero.</span><span class="sxs-lookup"><span data-stu-id="2485d-131">If you do not want it to be displayed, and wish to create your own user interface, set the height and width attributes of the OBJECT element to zero.</span></span>

<span data-ttu-id="2485d-132">El control también se puede hacer invisible si se establece el *reproductor*. propiedad **uiMode** en "invisible".</span><span class="sxs-lookup"><span data-stu-id="2485d-132">The control can also be made invisible by setting the *Player*.**uiMode** property to "invisible".</span></span> <span data-ttu-id="2485d-133">Esto puede hacerse mediante una etiqueta PARAM, como se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="2485d-133">This can be done using a PARAM tag as discussed in the next section.</span></span> <span data-ttu-id="2485d-134">En este caso, el espacio se reserva para el control con el alto y el ancho, pero no se muestra nada en el espacio reservado hasta que **uiMode** se cambie a un valor distinto de "invisible".</span><span class="sxs-lookup"><span data-stu-id="2485d-134">In this case, space is reserved for the control using height and width, but nothing is displayed in the reserved space until **uiMode** is changed to something other than "invisible".</span></span>

## <a name="related-topics"></a><span data-ttu-id="2485d-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2485d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2485d-136">**Usar el control Media Player de Windows en una página web**</span><span class="sxs-lookup"><span data-stu-id="2485d-136">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




