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
- Incrustación de páginas web, elementos PARAM en el elemento OBJECT
- Elementos PARAM del elemento OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243219"
---
# <a name="param-elements-in-an-object-element"></a>Elementos PARAM en un elemento OBJECT

Reproductor de Windows Media usa el elemento PARAM para definir condiciones de inicio específicas para el control. El elemento PARAM se incrusta dentro del elemento OBJECT.

Por ejemplo, si desea definir si la propiedad **autoStart** es True, insertaría el elemento PARAM dentro del elemento OBJECT.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



Puede tener tantos elementos PARAM en un elemento OBJECT como desee. PARAM tiene dos atributos, nombre y valor. Ambos atributos deben establecerse.

Los atributos PARAM admitidos varían ligeramente entre exploradores y tipos MIME. En la tabla siguiente se muestran los atributos admitidos por los exploradores Internet Explorer y Firefox. El tipo mime preferido para el explorador Firefox es application/x-ms-wmp; sin embargo, hay otros tipos mime que puede usar para insertar el control Player en una página web hospedada por el explorador Firefox. La cuarta columna de la tabla muestra los atributos que se admiten cuando se usa un tipo mime distinto de application/x-ms-wmp.



| Nombre de PARAM                                            | Internet Explorer | Firefox con tipo mime application/x-ms-wmp | Firefox con cualquier otro tipo mime |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Autostart](settings-autostart.md)                   | sí               | sí                                         | sí                              |
| [equilibrar](settings-balance.md)                       | sí               | sí                                         | sí                              |
| [Baseurl](settings-baseurl.md)                       | sí               | sí                                         | sí                              |
| [captioningID](closedcaption-captioningid.md)        | sí               | sí                                         | sí                              |
| [currentMarker](controls-currentmarker.md)           | sí               | sí                                         | sí                              |
| [currentPosition](controls-currentposition.md)       | sí               | sí                                         | sí                              |
| [defaultFrame](settings-defaultframe.md)             | sí               | no                                          | no                               |
| [enableContextMenu](player-enablecontextmenu.md)     | sí               | sí                                         | sí                              |
| [enabled](player-enabled.md)                         | sí               | sí                                         | sí                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | sí               | sí                                         | no                               |
| **fileName**                                          | no                | sí                                         | sí                              |
| [Fullscreen](player-fullscreen.md)                   | sí               | no                                          | no                               |
| [invokeURLs](settings-invokeurls.md)                 | sí               | no                                          | no                               |
| [Mudo](settings-mute.md)                             | sí               | sí                                         | sí                              |
| [playCount](settings-playcount.md)                   | sí               | sí                                         | no                               |
| [Tasa](settings-rate.md)                             | sí               | sí                                         | sí                              |
| [SAMIFileName](closedcaption-samifilename.md)        | sí               | sí                                         | sí                              |
| [SAMILang](closedcaption-samilang.md)                | sí               | sí                                         | sí                              |
| [SAMIStyle](closedcaption-samistyle.md)              | sí               | sí                                         | sí                              |
| **FUENTE**                                               | no                | sí                                         | sí                              |
| [stretchToFit](player-stretchtofit.md)               | sí               | sí                                         | no                               |
| [URL](player-url.md)                                 | sí               | sí                                         | sí                              |
| [volume](settings-volume.md)                         | sí               | sí                                         | sí                              |
| [windowlessVideo](player-windowlessvideo.md)         | sí               | sí                                         | sí                              |



 

> [!Note]  
> Los **elementos fileName** y **SRC** PARAM son compatibles con el complemento Firefox, pero no con Internet Explorer. Ambos realizan la misma función que el elemento **URL** PARAM.

 

Consulte referencia [del modelo de objetos para scripting](object-model-reference-for-scripting.md) para obtener más detalles sobre los valores de cada atributo de nombre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Reproductor de Windows Media en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




