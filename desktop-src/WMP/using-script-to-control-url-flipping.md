---
title: Usar script para controlar el volteo de direcciones URL
description: Usar script para controlar el volteo de direcciones URL
ms.assetid: ec504ecf-10ef-4b90-bee6-8d149c251ee5
keywords:
- Reproductor de Windows Media, presentaciones basadas en web
- Reproductor de Windows Media de objetos, presentaciones basadas en web
- modelo de objetos, presentaciones basadas en web
- Reproductor de Windows Media Presentaciones móviles basadas en web
- Reproductor de Windows Media ActiveX control, presentaciones basadas en web
- Reproductor de Windows Media Control de ActiveX móviles, presentaciones basadas en web
- control ActiveX, presentaciones basadas en web
- Reproductor de Windows Media,cambio de dirección URL
- Reproductor de Windows Media de objetos, cambio de dirección URL
- object model,URL fliping
- Reproductor de Windows Media Móvil, cambio de dirección URL
- Reproductor de Windows Media ActiveX control, volteo de dirección URL
- Reproductor de Windows Media Control de ActiveX móvil, cambio de dirección URL
- ActiveX control de direcciones URL, volteo de direcciones URL
- Presentaciones basadas en web, cambio de dirección URL
- creación de presentaciones basadas en web, cambio de dirección URL
- Cambio de dirección URL
- Reproductor de Windows Media, streaming multimedia enriquecido
- Reproductor de Windows Media de objetos enriquecidos, streaming multimedia enriquecido
- modelo de objetos, streaming multimedia enriquecido
- Reproductor de Windows Media Móvil, streaming multimedia enriquecido
- Reproductor de Windows Media ActiveX, streaming multimedia enriquecido
- Reproductor de Windows Media Control de ActiveX móvil, streaming multimedia enriquecido
- control ActiveX, streaming multimedia enriquecido
- Presentaciones basadas en web, streaming multimedia enriquecido
- crear presentaciones basadas en web, streaming multimedia enriquecido
- streaming multimedia enriquecido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4815562bba92d67bb4b02ea0317d6c29accd9262
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476165"
---
# <a name="using-script-to-control-url-flipping"></a>Usar script para controlar el volteo de direcciones URL

Cuando un usuario se conecta a un flujo multimedia enriquecido mientras la secuencia ya está en curso, es posible que la página web de streaming se muestre antes de que todos los elementos hayan llegado y se hayan almacenado en caché si Reproductor de Windows Media invoca automáticamente la dirección URL. Cuando esto sucede, el usuario ve una página web en blanco o incompleta hasta que el siguiente conjunto de datos llega a la memoria caché.

Puede evitar mostrar una página web en blanco o incompleta invocando la dirección URL mediante el script en lugar Reproductor de Windows Media hacerlo automáticamente. De este modo, puede omitir el primer cambio de dirección URL y, a continuación, invocar las direcciones URL posteriores mediante el código de script.

> [!Note]  
> En esta sección se da por supuesto que está transmitiendo HTML mediante el SDK de la serie Windows Media Encoder 9 y que ha establecido la secuencia HTML para que se repita.

 

En primer lugar, debe crear una página web de conjunto de fotogramas que contenga el fotograma con el Reproductor insertado y el marco que muestra el CÓDIGO HTML de streaming. Cada uno de estos dos fotogramas mostrará una página web independiente inicialmente, por lo que creará un total de tres páginas web. En el código de ejemplo siguiente se muestra la página web del conjunto de marcos:


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



El ejemplo de página web anterior incorpora dos fotogramas. El primer marco se muestra en la mitad izquierda de la ventana del explorador y muestra la página web denominada insertar \_player.htm. El código de ejemplo siguiente crea esta página web:


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



El segundo marco del conjunto de marcos se muestra en la mitad derecha de la ventana del explorador y muestra una página web denominada "blank.htm". El código de ejemplo siguiente crea esta página web:


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>

Loading...
</BODY>
</HTML>

```



Cuando se carga la página del conjunto de marcos en el explorador, el marco izquierdo muestra el reproductor incrustado y el marco derecho muestra el texto "Cargando...". para informar al usuario de que hay más datos próximamente. Cuando el primer comando de script de dirección URL llega de la secuencia HTML, el controlador de eventos simplemente cambia el valor de la **marca booleana.** Cuando cada comando de script de dirección URL posterior llega de la secuencia HTML, el script del controlador de eventos carga la nueva dirección URL en el marco denominado "contenido" y la página web completa se muestra en el marco ubicado en la mitad derecha de la ventana del explorador.

Para obtener más información sobre el streaming HTML mediante Windows Media, consulte el sdk Windows Media Encoder.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Rich Media Streaming**](rich-media-streaming.md)
</dt> <dt>

[**Volteo de direcciones URL**](url-flipping.md)
</dt> </dl>

 

 




