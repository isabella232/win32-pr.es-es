---
title: Controlar eventos en una página web mostrada por Firefox
description: Controlar eventos en una página web mostrada por Firefox
ms.assetid: 361c46ff-36e2-4497-a511-86b0439e9437
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media ActiveX control, páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- ActiveX control, páginas web
- Reproductor de Windows Media ActiveX control de eventos, control de eventos
- Reproductor de Windows Media Control de ActiveX móviles, control de eventos
- ActiveX control, control de eventos
- embedding,Web pages
- Inserción de páginas web, control de eventos
- Reproductor de Windows Media,Firefox
- Reproductor de Windows Media modelo de objetos,Firefox
- modelo de objetos, Firefox
- Reproductor de Windows Media Mobile,Firefox
- Reproductor de Windows Media ActiveX control, Firefox
- Reproductor de Windows Media Control de ActiveX móvil,Firefox
- ActiveX control, Firefox
- Firefox, control de eventos
- Inserción de páginas web, Firefox
- events,Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e971caef18114b670678fc76d0515858bee77a94a5e3f8b5c24ca5322177b8e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748420"
---
# <a name="handling-events-in-a-web-page-displayed-by-firefox"></a>Controlar eventos en una página web mostrada por Firefox

Al insertar el control Reproductor de Windows Media en una página web, puede escribir un script que controle los eventos. Para obtener una lista de los eventos que genera el control Player, vea [Player Object](player-object.md).

Si el tipo mime asociado a un control Player incrustado es application/x-ms-wmp, puede escribir controladores de eventos que tengan el formato siguiente:


```HTML
<SCRIPT for="Player" language="jscript" event="EventName(Params)">
  ...
</SCRIPT>
```



donde *EventName* es el nombre de un Reproductor de Windows Media evento y *Params* es una lista de los parámetros del evento. Por ejemplo, el código siguiente tiene un controlador para el [evento PlayStateChange.](player-player-playstatechange.md)


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="URL" value="c:\MediaFiles\Seattle.wmv"/>
</OBJECT>

<P id="p1">...</P>

<SCRIPT for="Player" event="PlayStateChange(NewState)">
  document.getElementById("p1").innerHTML = "Play state: " + NewState;
</SCRIPT>
```



Si tiene varias instancias del control Player en una página web y usa el formato que se muestra en el ejemplo anterior, cada controlador de eventos está asociado a una instancia específica del control Player. En el ejemplo anterior, solo se llama al controlador de eventos cuando cambia el estado de reproducción para el control que tiene id="Player".

Si el tipo mime asociado a un control Player incrustado no es application/x-ms-wmp, puede escribir controladores de eventos que tengan el formato siguiente:


```HTML
<SCRIPT language="jscript">
  function OnDSEventNameEvt(Params)
  {...}
</SCRIPT>
```



donde *EventName* es el nombre de un Reproductor de Windows Media evento y *Params* es una lista de los parámetros del evento. Por ejemplo, el código siguiente tiene un controlador para el **evento PlayStateChange.**


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



Si tiene varias instancias del control Player en una página web y usa el formato que se muestra en el ejemplo anterior, cada controlador de eventos está asociado a todas las instancias del control Player y se llama al controlador de eventos cuando cambia el estado de reproducción de cualquier control Player de la página.

> [!Note]  
> Si el tipo mime no es application/x-ms-wmp, el evento **DoubleClick** se envía como OnDSDblClickEvt (no OnDSDoubleClickEvt) por compatibilidad con la versión 6.4 del control Player.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del Reproductor de Windows Media control con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




