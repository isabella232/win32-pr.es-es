---
title: Uso de scripts en una página web que se muestra en Firefox
description: Uso de scripts en una página web que se muestra en Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- Control ActiveX de Windows Media Player, ejemplo de scripting
- Control ActiveX móvil de Windows Media Player, ejemplo de scripting
- Control ActiveX, ejemplo de scripting
- incrustación, páginas web
- Incrustación de páginas web, ejemplo de scripting
- Windows Media Player, Firefox
- Modelo de objetos de Windows Media Player, Firefox
- modelo de objetos, Firefox
- Windows Media Player Mobile, Firefox
- Control ActiveX de Windows Media Player, Firefox
- Control ActiveX móvil de Windows Media Player, Firefox
- Control ActiveX, Firefox
- Firefox, ejemplo de scripting
- Incrustación de páginas web, Firefox
- ejemplo de scripting para la inserción de páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105704821"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Uso de scripts en una página web que se muestra en Firefox

El script de una página web puede usar el modelo de objetos del reproductor para controlar el reproductor a medida que el usuario interactúa con la página. Por ejemplo, el siguiente elemento de entrada tiene un script que establece el volumen del reproductor.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Muchos de los objetos del modelo de objetos de Windows Media Player se admiten en Internet Explorer y en el complemento de Firefox. Sin embargo, hay algunos objetos que no son compatibles con el complemento de Firefox. En la tabla siguiente se enumeran todos los objetos del modelo de objetos del reproductor y se muestran los objetos que admite el complemento de Firefox.



| Object                                              | Compatibilidad con Firefox |
|-----------------------------------------------------|-----------------|
| [-](cdrom-object.md)                           | no              |
| [CdromCollection](cdromcollection-object.md)       | no              |
| [ClosedCaption](closedcaption-object.md)           | sí             |
| [Controles](controls-object.md)                     | no              |
| [DISCOS](dvd-object.md)                               | no              |
| [Error](error-object.md)                           | sí             |
| [ErrorItem](erroritem-object.md)                   | sí             |
| [Elementos multimedia](media-object.md)                           | sí             |
| [MediaCollection](mediacollection-object.md)       | no              |
| [MetadataPicture](metadatapicture-object.md)       | no              |
| [MetadataText](metadatatext-object.md)             | no              |
| [Network](network-object.md)                       | sí             |
| [Reproductor](player-object.md)                         | sí             |
| [PlayerApplication](playerapplication-object.md)   | no              |
| [Lista de reproducción](playlist-object.md)                     | sí             |
| [PlaylistArray](playlistarray-object.md)           | no              |
| [PlaylistCollection](playlistcollection-object.md) | no              |
| [Consultar](query-object.md)                           | no              |
| [Configuración](settings-object.md)                     | sí             |
| [StringCollection](stringcollection-object.md)     | no              |



 

El complemento de Firefox admite el objeto **Player** , pero algunas propiedades del objeto **Player** devuelven **null** en un explorador Firefox. Por ejemplo, la propiedad [cdromCollection](player-cdromcollection.md) del objeto **Player** devuelve **null** porque el complemento Firefox no admite el objeto **CDROM** . Del mismo modo, las propiedades [DVD](player-dvd.md), [mediaCollection](player-mediacollection.md), [PlayerApplication](player-playerapplication.md)y [PlaylistCollection](player-playlistcollection.md) del objeto **Player** devuelven **null** en un explorador Firefox.

La propiedad **Player. pluginVersionInfo** es compatible con el complemento de Firefox, pero no con Internet Explorer. Esta propiedad devuelve la versión del complemento de Firefox.

El complemento de Firefox admite el objeto **multimedia** , incluida la propiedad [getItemInfoByType](media-getiteminfobytype.md) . Sin embargo, en un explorador Firefox, la propiedad **getItemInfoByType** no admite los tipos de valor devuelto **MetadataText** y **MetadataPicture** .

El complemento de Firefox admite el objeto de [configuración](settings-object.md) , excepto el método [setMode](settings-setmode.md) y la propiedad [requestMediaAccessRights](settings-requestmediaaccessrights.md) . En un explorador Firefox, la propiedad **requestMediaAccessRight** siempre devuelve false.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del control de Media Player de Windows con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




