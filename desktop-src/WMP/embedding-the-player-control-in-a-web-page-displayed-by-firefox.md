---
title: Inserción del control Player en una página web mostrada por Firefox
description: Inserción del control Player en una página web mostrada por Firefox
ms.assetid: 57e725dc-6430-43ec-a39c-c17854a7d8db
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media ActiveX control,Páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- ActiveX control,Páginas web
- Reproductor de Windows Media,Firefox
- Reproductor de Windows Media modelo de objetos,Firefox
- modelo de objetos, Firefox
- Reproductor de Windows Media Mobile,Firefox
- control Reproductor de Windows Media ActiveX, Firefox
- Reproductor de Windows Media Control de ActiveX móvil,Firefox
- ActiveX control, Firefox
- Firefox, acerca de la inserción de páginas web
- embedding,Web pages
- Inserción de páginas web,Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16063ea07a0262ab798e58ed02e4d5a5b6b5d65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249692"
---
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Inserción del control Player en una página web mostrada por Firefox

Para insertar el control Reproductor de Windows Media en una página web que puede mostrar un explorador Firefox, cree un elemento OBJECT o un elemento EMBED que tenga uno de los siguientes tipos mime como atributo **de** tipo:

-   application/x-ms-wmp
-   application/asx
-   video/x-ms-asf-plugin
-   application/x-mplayer2
-   video/x-ms-asf
-   video/x-ms-wm
-   audio/x-ms-wma
-   audio/x-ms-suba
-   video/x-ms-wmv
-   video/x-ms-wvx

El tipo mime preferido es application/x-ms-wmp.

En los ejemplos siguientes se muestra cómo insertar el control Player mediante un elemento OBJECT o un elemento EMBED.


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



Los ejemplos anteriores funcionan en Firefox, pero no en Internet Explorer. Para insertar el control Player en una página web que puede mostrar Internet Explorer, debe crear un elemento OBJECT que tenga un atributo **classid** establecido en el identificador de clase del control Reproductor de Windows Media.

En el ejemplo siguiente se muestra cómo insertar el control Reproductor de Windows Media en una página web que se puede mostrar correctamente tanto en Internet Explorer como en Firefox. El script de la página detecta el tipo de explorador y genera la etiqueta OBJECT adecuada.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del control Reproductor de Windows Media con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




