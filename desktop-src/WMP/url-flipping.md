---
title: Volteo de direcciones URL
description: Volteo de direcciones URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Reproductor de Windows Media, presentaciones basadas en web
- Reproductor de Windows Media de objetos, presentaciones basadas en web
- modelo de objetos, presentaciones basadas en web
- Reproductor de Windows Media Presentaciones móviles basadas en web
- Reproductor de Windows Media ActiveX, presentaciones basadas en web
- Reproductor de Windows Media Control de ActiveX móviles, presentaciones basadas en web
- ActiveX, presentaciones basadas en web
- Reproductor de Windows Media,cambio de dirección URL
- Reproductor de Windows Media de objetos, cambio de dirección URL
- object model,URL fliping
- Reproductor de Windows Media Móvil, cambio de dirección URL
- Reproductor de Windows Media ActiveX control de direcciones URL, volteo de direcciones URL
- Reproductor de Windows Media Control de ActiveX móvil, cambio de dirección URL
- ActiveX control de direcciones URL, volteo de direcciones URL
- Presentaciones basadas en web, cambio de dirección URL
- crear presentaciones basadas en web, volteo de direcciones URL
- Cambio de dirección URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4471045506447b93621578f27e2f156bb214016b3fa8ec114a689b919314d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134528"
---
# <a name="url-flipping"></a>Volteo de direcciones URL

El uso de páginas web para las diapositivas se denomina volteo de direcciones URL y se controla automáticamente mediante Reproductor de Windows Media cuando encuentra comandos de script de dirección URL insertados en la secuencia de medios digitales que está reproduciendo. Puede especificar un marco de destino para las páginas en cada comando de script, o bien puede especificarlo estableciendo la **propiedad Configuración.defaultFrame.** Puede establecer esta propiedad en código de script o mediante un elemento PARAM dentro del elemento OBJECT que inserta el control Reproductor de Windows Media control .

Puede controlar los comandos de script de dirección URL en el código JScript igual que controlaría los comandos de script personalizados. Si desea que el control Reproductor de Windows Media omitir los comandos de script de dirección URL para que pueda controlarlos completamente por sí mismo, establezca *el Configuración*. **Propiedad invokeURLs** en false en código de script o mediante un elemento PARAM como se describió anteriormente.

En el ejemplo siguiente se muestra un conjunto de fotogramas típico para el volteo de direcciones URL. En primer lugar, cree una página que describa el conjunto de fotogramas:


```HTML
<HTML>
<FRAMESET cols="300,*">
  <FRAME name="player" src="player.html">
  <FRAME name="content">
</FRAMESET>
</HTML>

```



A continuación, cree el archivo player.html al que se hace referencia en el conjunto de fotogramas mediante el código siguiente (se supone que el archivo video.wmv existe en el mismo directorio que los archivos HTML):


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



Si las páginas web son lo suficientemente pequeñas como para cargarse rápidamente, esta configuración puede ser suficiente para sus necesidades. Por otro lado, si las páginas web son complejas, el streaming multimedia enriquecido puede ser más eficaz en función de la velocidad de conexión de la audiencia.

> [!Note]  
> El cambio de dirección URL no funciona correctamente con las páginas que se ven en Netscape Navigator. En lugar de aparecer en el marco especificado por **defaultFrame,** cada comando de script de dirección URL recibido en navegador muestra la dirección URL en una nueva ventana del explorador.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de Web-Based presentación**](creating-web-based-presentations.md)
</dt> <dt>

[**Usar script para controlar el volteo de direcciones URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




