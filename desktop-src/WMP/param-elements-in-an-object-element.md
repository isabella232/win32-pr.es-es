---
title: Elementos PARAM de un elemento OBJECT
description: Elementos PARAM de un elemento OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Windows Media Player, elementos PARAM en el elemento OBJECT
- Modelo de objetos de Windows Media Player, elementos PARAM en el elemento OBJECT
- modelo de objetos, elementos PARAM en el elemento OBJECT
- Windows Media Player Mobile, elementos PARAM en el elemento OBJECT
- Control ActiveX de Windows Media Player, elementos PARAM en el elemento OBJECT
- Control ActiveX móvil de Windows Media Player, elementos PARAM en el elemento OBJECT
- Control ActiveX, elementos PARAM en el elemento OBJECT
- incrustación, páginas web
- Incrustación de páginas web, elementos PARAM en el elemento OBJECT
- Elementos PARAM en el elemento OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "103903925"
---
# <a name="param-elements-in-an-object-element"></a>Elementos PARAM de un elemento OBJECT

Windows Media Player usa el elemento PARAM para definir condiciones de inicio específicas para el control. El elemento PARAM se incrusta dentro del elemento OBJECT.

Por ejemplo, si desea definir si la propiedad **autoStart** es true, debe incrustar el elemento Param dentro del elemento de objeto.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



Puede tener tantos elementos de parámetro en un elemento de objeto como desee. PARAM tiene dos atributos, Name y Value. Ambos atributos se deben establecer.

Los atributos de parámetro admitidos varían ligeramente entre los exploradores y los tipos MIME. En la tabla siguiente se muestran los atributos que admiten los exploradores de Internet Explorer y Firefox. El tipo MIME preferido para el explorador Firefox es application/x-MS-WMP; sin embargo, hay otros tipos MIME que puede usar para insertar el control Player en una página web hospedada por el explorador Firefox. La cuarta columna de la tabla muestra los atributos que se admiten cuando se usa un tipo MIME distinto de application/x-MS-wmp.



| Nombre de parámetro                                            | Internet Explorer | Firefox con aplicación de tipo MIME/x-MS-WMP | Firefox con cualquier otro tipo MIME |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Automáticamente](settings-autostart.md)                   | sí               | sí                                         | sí                              |
| [balancea](settings-balance.md)                       | sí               | sí                                         | sí                              |
| [baseURL](settings-baseurl.md)                       | sí               | sí                                         | sí                              |
| [captioningID](closedcaption-captioningid.md)        | sí               | sí                                         | sí                              |
| [currentMarker](controls-currentmarker.md)           | sí               | sí                                         | sí                              |
| [currentPosition](controls-currentposition.md)       | sí               | sí                                         | sí                              |
| [defaultFrame](settings-defaultframe.md)             | sí               | no                                          | no                               |
| [enableContextMenu](player-enablecontextmenu.md)     | sí               | sí                                         | sí                              |
| [enabled](player-enabled.md)                         | sí               | sí                                         | sí                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | sí               | sí                                         | no                               |
| **fileName**                                          | no                | sí                                         | sí                              |
| [Completa](player-fullscreen.md)                   | sí               | no                                          | no                               |
| [invokeURLs](settings-invokeurls.md)                 | sí               | no                                          | no                               |
| [silenciar](settings-mute.md)                             | sí               | sí                                         | sí                              |
| [playCount](settings-playcount.md)                   | sí               | sí                                         | no                               |
| [Rate](settings-rate.md)                             | sí               | sí                                         | sí                              |
| [SAMIFileName](closedcaption-samifilename.md)        | sí               | sí                                         | sí                              |
| [SAMILang](closedcaption-samilang.md)                | sí               | sí                                         | sí                              |
| [SAMIStyle](closedcaption-samistyle.md)              | sí               | sí                                         | sí                              |
| **DIEZ**                                               | no                | sí                                         | sí                              |
| [stretchToFit](player-stretchtofit.md)               | sí               | sí                                         | no                               |
| [URL](player-url.md)                                 | sí               | sí                                         | sí                              |
| [volume](settings-volume.md)                         | sí               | sí                                         | sí                              |
| [windowlessVideo](player-windowlessvideo.md)         | sí               | sí                                         | sí                              |



 

> [!Note]  
> Los elementos de parámetro **filename** y **src** son compatibles con el complemento de Firefox, pero no con Internet Explorer. Ambos realizan la misma función que el elemento de parámetro de **dirección URL** .

 

Vea la [Referencia del modelo de objetos para scripting](object-model-reference-for-scripting.md) para obtener más detalles sobre los valores de cada atributo de nombre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar el control Media Player de Windows en una página web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




