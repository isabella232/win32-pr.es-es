---
title: Volteo de dirección URL
description: Volteo de dirección URL
ms.assetid: 2921dff1-f740-491c-9b5e-79b7638e2065
keywords:
- Reproductor de Windows Media, presentaciones basadas en web
- Reproductor de Windows Media modelo de objetos, presentaciones basadas en web
- modelo de objetos, presentaciones basadas en web
- Reproductor de Windows Media Presentaciones móviles basadas en web
- Reproductor de Windows Media ActiveX, presentaciones basadas en web
- Reproductor de Windows Media Control de ActiveX móviles, presentaciones basadas en web
- ActiveX, presentaciones basadas en web
- Reproductor de Windows Media, cambio de dirección URL
- Reproductor de Windows Media modelo de objetos, cambio de dirección URL
- modelo de objetos, cambio de dirección URL
- Reproductor de Windows Media Móvil, cambio de dirección URL
- Reproductor de Windows Media ActiveX control, cambio de dirección URL
- Reproductor de Windows Media Control de ActiveX móvil, cambio de dirección URL
- ActiveX control, cambio de dirección URL
- Presentaciones basadas en web, cambio de dirección URL
- crear presentaciones basadas en web, volteo de direcciones URL
- Cambio de dirección URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141fdd6b4a7ffc57288a08ffa2f6760cfb029847
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465796"
---
# <a name="url-flipping"></a>Volteo de dirección URL

El uso de páginas web para las presentaciones de diapositivas se denomina volteo de direcciones URL y Reproductor de Windows Media lo controla automáticamente cuando encuentra comandos de script de dirección URL insertados en la secuencia de medios digitales que está reproduciendo. Puede especificar un marco de destino para las páginas en cada comando de script, o bien puede especificarlo estableciendo la **propiedad Configuración.defaultFrame.** Puede establecer esta propiedad en código de script o mediante un elemento PARAM dentro del elemento OBJECT que inserta el Reproductor de Windows Media control.

Puede controlar los comandos de script de dirección URL en el código JScript igual que controlaría los comandos de script personalizados. Si desea que el control Reproductor de Windows Media omitir los comandos de script de dirección URL para que pueda controlarlos completamente por su cuenta, establezca el *Configuración*. **Propiedad invokeURLs** en false en el código de script o mediante un elemento PARAM como se ha descrito anteriormente.

En el ejemplo siguiente se muestra un conjunto de fotogramas típico para el cambio de dirección URL. En primer lugar, cree una página que describa el conjunto de fotogramas:


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
> El cambio de dirección URL no funciona correctamente con las páginas que se ven en Netscape Navigator. En lugar de aparecer en el marco especificado por **defaultFrame**, cada comando de script de dirección URL recibido en Navegador muestra la dirección URL en una nueva ventana del explorador.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de Web-Based presentaciones**](creating-web-based-presentations.md)
</dt> <dt>

[**Usar script para controlar el volteo de direcciones URL**](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




