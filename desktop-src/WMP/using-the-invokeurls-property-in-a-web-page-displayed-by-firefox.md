---
title: Uso de la propiedad invokeURLs en una página web mostrada por Firefox
description: Uso de la propiedad invokeURLs en una página web mostrada por Firefox
ms.assetid: cec2ba89-b08f-4c83-bcb2-a4df1ce6f179
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- Reproductor de Windows Media ActiveX control,Páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- Reproductor de Windows Media ActiveX control,invokeURLs, propiedad
- Reproductor de Windows Media Control de ActiveX móvil, propiedad invokeURLs
- embedding,Web pages
- Inserción de páginas web, propiedad invokeURLs
- Reproductor de Windows Media,Firefox
- Reproductor de Windows Media modelo de objetos,Firefox
- object model,Firefox
- Reproductor de Windows Media ActiveX control,Firefox
- ActiveX control, Firefox
- Firefox, propiedad invokeURLs
- Inserción de páginas web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2487ebba1ff5664537dbaf0b0abad02a98acecf3c5985f1c09ffe9f8bbb743c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117114"
---
# <a name="using-the-invokeurls-property-in-a-web-page-displayed-by-firefox"></a>Uso de la propiedad invokeURLs en una página web mostrada por Firefox

Algunos archivos multimedia contienen direcciones URL insertadas para las que Reproductor de Windows Media páginas web en una ventana o marco del explorador web a medida que se reproduce el archivo multimedia. En Windows Internet Explorer, puede usar la propiedad [Configuración.invokeURLs](settings-invokeurls.md) para especificar si las páginas se muestran para las direcciones URL insertadas, y puede usar la propiedad [Configuración.defaultFrame](settings-defaultframe.md) para especificar un marco para mostrar dichas páginas.

En Firefox, se requieren algunas soluciones alternativas para establecer la propiedad **invokeURLs** y para especificar un marco para mostrar páginas para direcciones URL insertadas.

## <a name="setting-the-invokeurls-property"></a>Establecimiento de la propiedad invokeURLs

El valor predeterminado de **la propiedad Configuración.invokeURLs** es true, por lo que si desea que el valor sea false, debe establecerlo explícitamente. En Internet Explorer, puede establecer **invokeURLs** en false en un elemento PARAM dentro del elemento OBJECT del control Player.

El complemento firefox no admite el establecimiento de la **propiedad invokeURLs** en un elemento PARAM.

Puede evitar esta limitación estableciendo la **propiedad invokeURLs** en el script. En el código siguiente se muestra cómo establecer la propiedad **invokeURLs** en false en una página web que se puede mostrar tanto en Internet Explorer como en Firefox.


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

Un archivo multimedia puede contener direcciones URL que muestran páginas web en una ventana o marco del explorador a medida que se reproduce el archivo multimedia. En Internet Explorer, puede usar la [propiedad Configuración.defaultFrame](settings-defaultframe.md) para especificar el marco en el que se muestran esas páginas. Si no establece la propiedad **defaultFrame,** las direcciones URL se muestran en una ventana independiente del explorador predeterminado. Sin embargo, el complemento firefox no admite la **propiedad Configuración.defaultFrame.** Para evitar esta limitación, establezca la propiedad **Configuración.invokeURLs** en false y escriba un controlador de eventos [ScriptCommand](player-player-scriptcommand.md) que establezca la ubicación del marco de destino. En el ejemplo siguiente, que funciona en Internet Explorer y Firefox, se ilustra esta técnica. Suponga que la página web que se muestra en el ejemplo está en fotogramas 0 y desea que la página de la dirección URL se muestre \[ \] en los fotogramas \[ \] 1.


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

[**Uso del Reproductor de Windows Media Control con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




