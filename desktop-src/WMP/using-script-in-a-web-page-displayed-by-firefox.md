---
title: Usar script en una página web mostrada por Firefox
description: Usar script en una página web mostrada por Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Reproductor de Windows Media, insertar ActiveX control
- Reproductor de Windows Media modelo de objetos, insertar ActiveX control
- object model,embedding ActiveX control
- Reproductor de Windows Media Mobile,embedding ActiveX control
- Reproductor de Windows Media ActiveX control, inserción
- Reproductor de Windows Media Control de ActiveX móvil, inserción
- ActiveX control, inserción
- Reproductor de Windows Media ActiveX control,Páginas web
- Reproductor de Windows Media Control de ActiveX móviles,páginas web
- ActiveX control,Páginas web
- Reproductor de Windows Media ActiveX control, ejemplo de scripting
- Reproductor de Windows Media Control de ActiveX móvil, ejemplo de scripting
- ActiveX control, ejemplo de scripting
- embedding,Web pages
- Inserción de páginas web, ejemplo de scripting
- Reproductor de Windows Media,Firefox
- Reproductor de Windows Media modelo de objetos,Firefox
- object model,Firefox
- Reproductor de Windows Media Mobile,Firefox
- Reproductor de Windows Media ActiveX control,Firefox
- Reproductor de Windows Media Control de ActiveX móvil,Firefox
- ActiveX control, Firefox
- Firefox, ejemplo de scripting
- Inserción de páginas web, Firefox
- ejemplo de scripting para la inserción de páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450b03f7adefca1a887fb31207f0a3280e1925c9d3e1f1066df370d87f0a7779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762065"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Usar script en una página web mostrada por Firefox

El script de una página web puede usar el modelo de objetos Player para controlar el reproductor a medida que el usuario interactúa con la página. Por ejemplo, el siguiente elemento INPUT tiene un script que establece el volumen Player.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Muchos de los objetos del Reproductor de Windows Media modelo de objetos son compatibles con Internet Explorer y el complemento firefox. Sin embargo, hay algunos objetos que no son compatibles con el complemento firefox. En la tabla siguiente se enumeran todos los objetos del modelo de objetos player y se muestran los objetos admitidos por el complemento firefox.



| Object                                              | Compatibilidad con Firefox |
|-----------------------------------------------------|-----------------|
| [Cdrom](cdrom-object.md)                           | No              |
| [CdromCollection](cdromcollection-object.md)       | No              |
| [ClosedCaption](closedcaption-object.md)           | Sí             |
| [Controles](controls-object.md)                     | No              |
| [Dvd](dvd-object.md)                               | No              |
| [Error](error-object.md)                           | Sí             |
| [ErrorItem](erroritem-object.md)                   | Sí             |
| [Elementos multimedia](media-object.md)                           | Sí             |
| [MediaCollection](mediacollection-object.md)       | No              |
| [MetadataPicture](metadatapicture-object.md)       | No              |
| [MetadataText](metadatatext-object.md)             | No              |
| [Red](network-object.md)                       | Sí             |
| [Reproductor](player-object.md)                         | Sí             |
| [PlayerApplication](playerapplication-object.md)   | No              |
| [Lista de reproducción](playlist-object.md)                     | Sí             |
| [PlaylistArray](playlistarray-object.md)           | No              |
| [PlaylistCollection](playlistcollection-object.md) | No              |
| [Consultar](query-object.md)                           | No              |
| [Configuración](settings-object.md)                     | Sí             |
| [StringCollection](stringcollection-object.md)     | No              |



 

El complemento Firefox admite el objeto **Player,** pero ciertas propiedades del **objeto Player** **devuelven NULL** en un explorador Firefox. Por ejemplo, la [propiedad cdromCollection](player-cdromcollection.md) del objeto **Player** devuelve **NULL** porque el complemento Firefox no admite el **objeto Cdrom.** De forma similar, las [propiedades dvd](player-dvd.md), [mediaCollection,](player-mediacollection.md) [playerApplication](player-playerapplication.md)y [playlistCollection](player-playlistcollection.md) del objeto **Player** **devuelven NULL** en un explorador Firefox.

El complemento Firefox admite la propiedad **Player.pluginVersionInfo,** pero no Internet Explorer. Esta propiedad devuelve la versión del complemento firefox.

El complemento Firefox admite el **objeto Media,** incluida [la propiedad getItemInfoByType.](media-getiteminfobytype.md) Sin embargo, en un explorador Firefox, la **propiedad getItemInfoByType** no admite los tipos de valor devuelto **MetadataText** y **MetadataPicture.**

El complemento Firefox admite el [objeto Configuración](settings-object.md) excepto para el método [setMode](settings-setmode.md) y la [propiedad requestMediaAccessRights.](settings-requestmediaaccessrights.md) En un explorador Firefox, la **propiedad requestMediaAccessRight** siempre devuelve false.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso del Reproductor de Windows Media Control con Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




