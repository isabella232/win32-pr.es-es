---
title: Control de eventos en una página web que se muestra en Firefox
description: Control de eventos en una página web que se muestra en Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
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
- Control ActiveX de Windows Media Player, control de eventos
- Control ActiveX de Windows Media Player Mobile, control de eventos
- Control ActiveX, control de eventos
- incrustación, páginas web
- Incrustación de páginas web, control de eventos
- Windows Media Player, Firefox
- Modelo de objetos de Windows Media Player, Firefox
- modelo de objetos, Firefox
- Windows Media Player Mobile, Firefox
- Control ActiveX de Windows Media Player, Firefox
- Control ActiveX móvil de Windows Media Player, Firefox
- Control ActiveX, Firefox
- Firefox, control de eventos
- Incrustación de páginas web, Firefox
- eventos, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9659d1920ffc4d5e39f4cd44e15e24b08f6ddc
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104357822"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="64810-128">Control de eventos en una página web que se muestra en Firefox</span><span class="sxs-lookup"><span data-stu-id="64810-128">Handling Events in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="64810-129">Al incrustar el control Media Player de Windows en una página web, puede escribir un script que controle los eventos.</span><span class="sxs-lookup"><span data-stu-id="64810-129">When you embed the Windows Media Player control in a webpage, you can write script that handles events.</span></span> <span data-ttu-id="64810-130">Para obtener una lista de eventos generados por el control Player, consulte [objeto Player](player-object.md).</span><span class="sxs-lookup"><span data-stu-id="64810-130">For a list of events raised by the Player control, see [Player Object](player-object.md).</span></span>

<span data-ttu-id="64810-131">Si el tipo MIME asociado a un control de reproductor incrustado es application/x-MS-WMP, puede escribir controladores de eventos con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="64810-131">If the mime type associated with an embedded Player control is application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



<span data-ttu-id="64810-132">donde *eventName* es el nombre de un evento de Windows Media Player y *params* es una lista de los parámetros del evento.</span><span class="sxs-lookup"><span data-stu-id="64810-132">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="64810-133">Por ejemplo, el código siguiente tiene un controlador para el evento [PlayStateChange](player-player-playstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="64810-133">For example, the following code has a handler for the [PlayStateChange](player-player-playstatechange.md) event.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



<span data-ttu-id="64810-134">Si tiene varias instancias del control Player en una página web y usa el formato que se muestra en el ejemplo anterior, cada controlador de eventos está asociado a una instancia específica del control Player.</span><span class="sxs-lookup"><span data-stu-id="64810-134">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to a specific instance of the Player control.</span></span> <span data-ttu-id="64810-135">En el ejemplo anterior, solo se llama al controlador de eventos cuando el estado de reproducción cambia para el control que tiene ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="64810-135">In the preceeding example, the event handler is called only when the play state changes for the control that has id="Player".</span></span>

<span data-ttu-id="64810-136">Si el tipo MIME asociado a un control de reproductor incrustado no es application/x-MS-WMP, puede escribir controladores de eventos con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="64810-136">If the mime type associated with an embedded Player control is not application/x-ms-wmp, you can write event handlers that have the following format:</span></span>


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



<span data-ttu-id="64810-137">donde *eventName* es el nombre de un evento de Windows Media Player y *params* es una lista de los parámetros del evento.</span><span class="sxs-lookup"><span data-stu-id="64810-137">where *EventName* is the name of a Windows Media Player event, and *Params* is a list of the event's parameters.</span></span> <span data-ttu-id="64810-138">Por ejemplo, el código siguiente tiene un controlador para el evento **PlayStateChange** .</span><span class="sxs-lookup"><span data-stu-id="64810-138">For example, the following code has a handler for the **PlayStateChange** event.</span></span>


```HTML
<OBJECT id="Player" type="application/asx" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Test.asx"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT>
  function OnDSPlayStateChangeEvt(NewState)
  {
    p1.innerHTML = "Play state: " + NewState;
  }
</SCRIPT>

```



<span data-ttu-id="64810-139">Si tiene varias instancias del control Player en una página web y usa el formato que se muestra en el ejemplo anterior, cada controlador de eventos está asociado a todas las instancias del control Player y se llama al controlador de eventos cuando cambia el estado de reproducción para cualquier control de reproductor en la página.</span><span class="sxs-lookup"><span data-stu-id="64810-139">If you have several instances of the Player control on a webpage and if you use the format shown in the preceeding example, then each event handler is tied to all instances of the Player control and the event handler is called when the play state changes for any Player control on the page.</span></span>

> [!Note]  
> <span data-ttu-id="64810-140">Si el tipo MIME no es application/x-MS-WMP, el evento **DoubleClick** se envía como OnDSDblClickEvt (no OnDSDoubleClickEvt) por compatibilidad con la versión 6,4 del control Player.</span><span class="sxs-lookup"><span data-stu-id="64810-140">If the mime type is not application/x-ms-wmp, the **DoubleClick** event is sent as OnDSDblClickEvt (not OnDSDoubleClickEvt) for compatibility with version 6.4 of the Player control.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="64810-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64810-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64810-142">**Uso del control de Media Player de Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="64810-142">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




