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
# <a name="embedding-the-player-control-in-a-web-page-displayed-by-firefox"></a>Incrustar el control Player en una página web que se muestra en Firefox

Para insertar el control de Media Player de Windows en una página web que se puede mostrar en un explorador Firefox, cree un elemento de objeto o un elemento EMBED que tenga uno de los siguientes tipos MIME como su atributo de **tipo** :

-   application/x-MS-WMP
-   aplicación/ASX
-   vídeo/x-MS-ASF-complemento
-   application/x-Mplayer2
-   vídeo/x-MS-ASF
-   vídeo/x-MS-WM
-   audio/x-MS-WMA
-   audio/x-MS-Wax
-   vídeo/x-MS-WMV
-   vídeo/x-MS-wvx

El tipo MIME preferido es application/x-MS-wmp.

En los siguientes ejemplos se muestra cómo incrustar el control Player mediante un elemento OBJECT o un elemento EMBED.


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



Los ejemplos anteriores funcionan en Firefox pero no en Internet Explorer. Para insertar el control Player en una página web que puede mostrarse en Internet Explorer, debe crear un elemento de objeto que tenga un atributo **ClassID** establecido en el identificador de clase del control Media Player de Windows.

En el ejemplo siguiente se muestra cómo insertar el control Media Player de Windows en una página web que se puede mostrar correctamente en Internet Explorer y Firefox. El script de la página detecta el tipo de explorador y genera la etiqueta de objeto adecuada.


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

[**Uso del control de Media Player de Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




