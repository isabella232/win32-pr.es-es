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
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Uso de la propiedad invokeURLs en una página web que se muestra en Firefox

Algunos archivos multimedia contienen direcciones URL incrustadas en las que Windows Media Player muestra las páginas web en una ventana o un marco del explorador Web a medida que se reproduce el archivo multimedia. En Windows Internet Explorer, puede usar la propiedad [Settings. invokeURLs](settings-invokeurls.md) para especificar si las páginas se muestran para las direcciones URL incrustadas, y puede usar la propiedad [Settings. defaultFrame](settings-defaultframe.md) para especificar un marco para mostrar dichas páginas.

En Firefox, se necesitan algunas soluciones alternativas para establecer la propiedad **invokeURLs** y especificar un marco para mostrar las páginas de las direcciones URL incrustadas.

## <a name="setting-the-invokeurls-property"></a>Establecimiento de la propiedad invokeURLs

El valor predeterminado de la propiedad **Settings. invokeURLs** es true, por lo que si desea que el valor sea false, debe establecerlo explícitamente. En Internet Explorer, puede establecer **invokeURLs** en false en un elemento Param dentro del elemento de objeto del control Player.

El complemento de Firefox no admite el establecimiento de la propiedad **invokeURLs** en un elemento Param.

Para solucionar esta limitación, puede establecer la propiedad **invokeURLs** en el script. En el código siguiente se muestra cómo establecer la propiedad **invokeURLs** en false en una página web que se puede mostrar con Internet Explorer y Firefox.


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



## <a name="displaying-webpages-in-a-frame"></a>Mostrar páginas web en un marco

Un archivo multimedia puede contener direcciones URL que muestren páginas web en una ventana o marco del explorador cuando se reproduzca el archivo multimedia. En Internet Explorer, puede usar la propiedad [Settings. defaultFrame](settings-defaultframe.md) para especificar el marco en el que se muestran esas páginas. Si no establece la propiedad **defaultFrame** , las direcciones URL se muestran en una ventana independiente del explorador predeterminado. Sin embargo, el complemento de Firefox no admite la propiedad **Settings. defaultFrame** . Para evitar esta limitación, establezca la propiedad **Settings. invokeURLs** en false y escriba un controlador de eventos [comando](player-player-scriptcommand.md) que establezca la ubicación del marco de destino. En el ejemplo siguiente, que funciona en Internet Explorer y Firefox, se ilustra esta técnica. Supongamos que la página web que se muestra en el ejemplo está en los marcos \[ 0 \] y desea que la página de la dirección URL se muestre en los marcos \[ 1 \] .


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del control de Media Player de Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




