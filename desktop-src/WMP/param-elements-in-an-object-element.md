---
title: Elementos PARAM en un elemento OBJECT
description: Elementos PARAM en un elemento OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Reproductor de Windows Media,PARAM en el elemento OBJECT
- Reproductor de Windows Media modelo de objetos, elementos PARAM en el elemento OBJECT
- object model,PARAM elements in OBJECT element
- Reproductor de Windows Media Elementos Mobile,PARAM en el elemento OBJECT
- Reproductor de Windows Media ActiveX control, elementos PARAM en el elemento OBJECT
- Reproductor de Windows Media Control ActiveX móvil, elementos PARAM en el elemento OBJECT
- ActiveX control, elementos PARAM en el elemento OBJECT
- embedding,Web pages
- Inserción de páginas web, elementos PARAM en el elemento OBJECT
- Elementos PARAM del elemento OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da684a39739703038793abb2f4fdd32b924f35cdffc0c0f9d796fb7dbb5532b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054433"
---
# <a name="param-elements-in-an-object-element"></a>Elementos PARAM en un elemento OBJECT

Reproductor de Windows Media el elemento PARAM para definir condiciones de inicio específicas para el control. El elemento PARAM se incrusta dentro del elemento OBJECT.

Por ejemplo, si desea definir si la propiedad **autoStart** es True, insertaría el elemento PARAM dentro del elemento OBJECT.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



Puede tener tantos elementos PARAM en un elemento OBJECT como desee. PARAM tiene dos atributos, nombre y valor. Ambos atributos deben establecerse.

Los atributos de PARAM admitidos varían ligeramente entre exploradores y tipos MIME. En la tabla siguiente se muestran los atributos admitidos por los exploradores Internet Explorer y Firefox. El tipo mime preferido para el explorador Firefox es application/x-ms-wmp; sin embargo, hay otros tipos mime que puede usar para insertar el control Player en una página web hospedada por el explorador Firefox. La cuarta columna de la tabla muestra los atributos que se admiten cuando se usa un tipo mime distinto de application/x-ms-wmp.



| Nombre de PARAM                                            | Internet Explorer | Firefox con tipo mime application/x-ms-wmp | Firefox con cualquier otro tipo mime |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Autostart](settings-autostart.md)                   | Sí               | Sí                                         | Sí                              |
| [equilibrar](settings-balance.md)                       | Sí               | Sí                                         | Sí                              |
| [Baseurl](settings-baseurl.md)                       | Sí               | Sí                                         | Sí                              |
| [captioningID](closedcaption-captioningid.md)        | Sí               | Sí                                         | Sí                              |
| [currentMarker](controls-currentmarker.md)           | Sí               | Sí                                         | Sí                              |
| [currentPosition](controls-currentposition.md)       | Sí               | Sí                                         | Sí                              |
| [defaultFrame](settings-defaultframe.md)             | Sí               | No                                          | No                               |
| [enableContextMenu](player-enablecontextmenu.md)     | Sí               | Sí                                         | Sí                              |
| [enabled](player-enabled.md)                         | Sí               | Sí                                         | Sí                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | Sí               | Sí                                         | No                               |
| **fileName**                                          | No                | sí                                         | Sí                              |
| [Fullscreen](player-fullscreen.md)                   | Sí               | No                                          | No                               |
| [invokeURLs](settings-invokeurls.md)                 | Sí               | No                                          | No                               |
| [Mudo](settings-mute.md)                             | Sí               | Sí                                         | Sí                              |
| [playCount](settings-playcount.md)                   | Sí               | Sí                                         | No                               |
| [Tasa](settings-rate.md)                             | Sí               | Sí                                         | Sí                              |
| [SAMIFileName](closedcaption-samifilename.md)        | Sí               | Sí                                         | Sí                              |
| [SAMILang](closedcaption-samilang.md)                | Sí               | Sí                                         | Sí                              |
| [SAMIStyle](closedcaption-samistyle.md)              | Sí               | Sí                                         | Sí                              |
| **Fuente**                                               | No                | sí                                         | Sí                              |
| [stretchToFit](player-stretchtofit.md)               | Sí               | Sí                                         | No                               |
| [URL](player-url.md)                                 | Sí               | Sí                                         | Sí                              |
| [volume](settings-volume.md)                         | Sí               | Sí                                         | Sí                              |
| [windowlessVideo](player-windowlessvideo.md)         | Sí               | Sí                                         | Sí                              |



 

> [!Note]  
> Los **elementos fileName** y **SRC** PARAM son compatibles con el complemento Firefox, pero no con Internet Explorer. Ambos realizan la misma función que el elemento **URL** PARAM.

 

Consulte referencia [del modelo de objetos para scripting](object-model-reference-for-scripting.md) para obtener más detalles sobre los valores de cada atributo de nombre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Reproductor de Windows Media en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




