---
title: Volteo de URL
description: Volteo de URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "103780257"
---
# <a name="url-flipping"></a>Volteo de URL

El uso de páginas web para presentaciones de diapositivas se denomina volteo de direcciones URL y Windows Media Player administra automáticamente cuando encuentra comandos de scripts de URL insertados en la secuencia de medios digitales que se está reproduciendo. Puede especificar un marco de destino para las páginas en cada comando de script o puede especificarlo estableciendo la propiedad **Settings. defaultFrame** . Puede establecer esta propiedad en el código de script o mediante un elemento PARAM dentro del elemento de objeto que incrusta el control Media Player de Windows.

Puede controlar los comandos de script de dirección URL en el código JScript del mismo modo que administraría los comandos de script personalizados. Si desea que el control de Media Player de Windows omita los comandos de script de dirección URL para que pueda controlarlos completamente, establezca la *configuración*. la propiedad **invokeURLs** en false en el código de script o mediante un elemento Param como se ha descrito anteriormente.

En el ejemplo siguiente se muestra un FRAMESET típico para el volteo de direcciones URL. En primer lugar, cree una página que describa el frameset:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



A continuación, cree el archivo player.html al que se hace referencia en el frameset mediante el código siguiente (se supone que el archivo video. wmv existe en el mismo directorio que los archivos HTML):


```HTML
<HTML>
<BODY>
<OBJECT ID="Player" CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
  <PARAM name="URL" value="https://www.proseware.com/Media/video.wmv"/>
  <PARAM name="defaultFrame" value="content"/>
</OBJECT>
</BODY>
</HTML>

```



Si las páginas web son lo suficientemente pequeñas para cargarse rápidamente, puede que esta configuración sea suficiente para sus necesidades. Por otro lado, si las páginas web son complejas, el streaming multimedia enriquecido puede ser más eficaz en función de la velocidad de conexión de la audiencia.

> [!Note]  
> El volteo de direcciones URL no funciona correctamente con las páginas que se ven en Netscape Navigator. En lugar de aparecer en el marco especificado por **defaultFrame**, cada comando de script de dirección URL recibido en el navegador muestra la dirección URL en una nueva ventana del explorador.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear Web-Based presentaciones**](creating-web-based-presentations.md)
</dt> <dt>

[**Usar script para controlar el volteo de URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




