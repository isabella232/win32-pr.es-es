---
title: Usar script para controlar el volteo de URL
description: Usar script para controlar el volteo de URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Windows Media Player, presentaciones basadas en Web
- Modelo de objetos de Windows Media Player, presentaciones basadas en Web
- modelo de objetos, presentaciones basadas en Web
- Windows Media Player presentaciones móviles y basadas en Web
- Control ActiveX de Windows Media Player, presentaciones basadas en Web
- Control ActiveX móvil de Windows Media Player, presentaciones basadas en Web
- Control ActiveX, presentaciones basadas en Web
- Media Player de Windows, volteo de URL
- Modelo de objetos de Windows Media Player, volteo de direcciones URL
- modelo de objetos, volteo de URL
- Windows Media Player Mobile, volteo de direcciones URL
- Control ActiveX de Windows Media Player, volteo de direcciones URL
- Control ActiveX móvil de Windows Media Player, volteo de direcciones URL
- Control ActiveX, volteo de direcciones URL
- Presentaciones basadas en Web, volteo de direcciones URL
- crear presentaciones basadas en Web, volteo de direcciones URL
- Volteo de URL
- Windows Media Player, transmisión por secuencias multimedia enriquecida
- Modelo de objetos de Windows Media Player, transmisión por secuencias multimedia enriquecida
- modelo de objetos, streaming multimedia enriquecido
- Windows Media Player Mobile, streaming multimedia enriquecido
- Control ActiveX de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX móvil de Windows Media Player, transmisión por secuencias multimedia enriquecida
- Control ActiveX, transmisión por secuencias multimedia enriquecida
- Presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- crear presentaciones basadas en Web, transmisión por secuencias multimedia enriquecida
- transmisión por secuencias multimedia enriquecida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "104419233"
---
# <a name="using-script-to-control-url-flipping"></a>Usar script para controlar el volteo de URL

Cuando un usuario se conecta a una secuencia multimedia enriquecida mientras la secuencia ya está en curso, es posible que la página web transmitida se muestre antes de que todos los elementos hayan llegado y estén almacenados en caché si Windows Media Player invoca automáticamente la dirección URL. Cuando esto sucede, el usuario ve una página web en blanco o incompleta hasta que llega el siguiente conjunto de datos en la memoria caché.

Puede evitar que se muestre una página web en blanco o incompleta mediante la invocación de la dirección URL mediante el script en lugar de permitir que Windows Media Player lo haga automáticamente. De este modo, puede omitir la primera dirección URL voltear y, a continuación, invocar las direcciones URL subsiguientes mediante el código de script.

> [!Note]  
> En esta sección se supone que está transmisiones por secuencias de HTML mediante el SDK de Windows Media Encoder 9 series y que ha configurado la secuencia HTML para que se repita.

 

En primer lugar, debe crear una página web de conjuntos de marcos que contenga el marco con el reproductor incrustado y el marco que muestra el código HTML de streaming. Cada uno de estos dos marcos mostrará una página web independiente inicialmente, por lo que creará un total de tres páginas Web. En el ejemplo de código siguiente se muestra la página web FRAMESET:


```HTML
<HTML>
<HEAD>
</HEAD>

<FRAMESET cols = "350, *">
  <FRAME  name = "player" src = "embed_player.htm">
  <FRAME  name = "content" src = "blank.htm">

  <NOFRAMES>
  <BODY>

  <P>This page uses frames, but your browser doesn't support them.</P>

  </BODY>
  </NOFRAMES>

</FRAMESET>
</HTML>

```



En el ejemplo anterior de la página web se incorporan dos fotogramas. El primer fotograma se muestra en la mitad izquierda de la ventana del explorador y muestra la página web denominada embed \_player.htm. En el código de ejemplo siguiente se crea esta página web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

<!-- Embed Windows Media Player and disable the invokeURLs parameter -->
<OBJECT CLASSID = "CLSID:6BF52A52-394A-11D3-B153-00C04F79FAA6" ID = "Player">
  <PARAM name = "URL"  value = "https://www.proseware.com/Media/video.wmv">
  <PARAM name = "invokeURLs"  value = "false">
</OBJECT>

<SCRIPT LANGUAGE = "JScript">
  var bFirstURL = true; // Global flag for first URL flip.
</SCRIPT>

<!-- Create an event handler for script commands. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player" EVENT = "ScriptCommand(scType, scParam)">

  if("URL" == scType)
  {
    if ( bFirstURL == false )
    {
      // Show the next URL flip.
      parent.content.location = scParam;
    }
    else
    {
      bFirstURL = false; // Set the flag.
    }
  }

</SCRIPT>

</BODY>
</HTML>

```



El segundo fotograma del cuadro de marcos se muestra en la mitad derecha de la ventana del explorador y muestra una página web denominada "blank.htm". En el código de ejemplo siguiente se crea esta página web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Cuando se carga la página de conjuntos de marcos en el explorador, el marco de la izquierda muestra el reproductor incrustado y el marco de la derecha muestra el texto "cargando..." para informar al usuario de que hay más datos disponibles. Cuando el primer comando de script de dirección URL llega de la secuencia HTML, el controlador de eventos simplemente cambia el valor de la marca **booleana** . Cuando el siguiente comando de script de dirección URL llega de la secuencia HTML, el script del controlador de eventos carga la nueva dirección URL en el marco denominado "Content" y se muestra la página web completa en el marco situado en la mitad derecha de la ventana del explorador.

Para obtener más información acerca de la transmisión por secuencias de HTML con Windows Media, consulte el SDK de Windows Media Encoder.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Transmisión por secuencias multimedia enriquecida**](rich-media-streaming.md)
</dt> <dt>

[**Volteo de URL**](url-flipping.md)
</dt> </dl>

 

 




