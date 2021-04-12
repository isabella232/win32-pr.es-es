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
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Control de eventos en una página web que se muestra en Firefox

Al incrustar el control Media Player de Windows en una página web, puede escribir un script que controle los eventos. Para obtener una lista de eventos generados por el control Player, consulte [objeto Player](player-object.md).

Si el tipo MIME asociado a un control de reproductor incrustado es application/x-MS-WMP, puede escribir controladores de eventos con el siguiente formato:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



donde *eventName* es el nombre de un evento de Windows Media Player y *params* es una lista de los parámetros del evento. Por ejemplo, el código siguiente tiene un controlador para el evento [PlayStateChange](player-player-playstatechange.md) .


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Si tiene varias instancias del control Player en una página web y usa el formato que se muestra en el ejemplo anterior, cada controlador de eventos está asociado a una instancia específica del control Player. En el ejemplo anterior, solo se llama al controlador de eventos cuando el estado de reproducción cambia para el control que tiene ID = "Player".

Si el tipo MIME asociado a un control de reproductor incrustado no es application/x-MS-WMP, puede escribir controladores de eventos con el siguiente formato:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



donde *eventName* es el nombre de un evento de Windows Media Player y *params* es una lista de los parámetros del evento. Por ejemplo, el código siguiente tiene un controlador para el evento **PlayStateChange** .


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



Si tiene varias instancias del control Player en una página web y usa el formato que se muestra en el ejemplo anterior, cada controlador de eventos está asociado a todas las instancias del control Player y se llama al controlador de eventos cuando cambia el estado de reproducción para cualquier control de reproductor en la página.

> [!Note]  
> Si el tipo MIME no es application/x-MS-WMP, el evento **DoubleClick** se envía como OnDSDblClickEvt (no OnDSDoubleClickEvt) por compatibilidad con la versión 6,4 del control Player.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del control de Media Player de Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




