---
title: Acerca de los objetos playlist, PlaylistCollection y PlaylistArray
description: Acerca de los objetos playlist, PlaylistCollection y PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player, objeto Playlist
- Modelo de objetos de Windows Media Player, objeto Playlist
- modelo de objetos, objeto Playlist
- Control ActiveX de Windows Media Player, objeto Playlist
- Control ActiveX, objeto Playlist
- Control ActiveX móvil de Windows Media Player, objeto Playlist
- Windows Media Player Mobile, objeto de lista de reproducción
- Objeto Playlist
- Media Player de Windows, objeto PlaylistCollection
- Modelo de objetos de Media Player de Windows, objeto PlaylistCollection
- modelo de objetos, PlaylistCollection (objeto)
- Control ActiveX de Windows Media Player, objeto PlaylistCollection
- Control ActiveX, objeto PlaylistCollection
- Control ActiveX de Windows Media Player Mobile, objeto PlaylistCollection
- Windows Media Player Mobile, objeto PlaylistCollection
- Objeto PlaylistCollection
- Media Player de Windows, objeto PlaylistArray
- Modelo de objetos de Media Player de Windows, objeto PlaylistArray
- modelo de objetos, PlaylistArray (objeto)
- Control ActiveX de Windows Media Player, objeto PlaylistArray
- Control ActiveX, objeto PlaylistArray
- Control ActiveX de Windows Media Player Mobile, objeto PlaylistArray
- Windows Media Player Mobile, objeto PlaylistArray
- Objeto PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695316"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>Acerca de los objetos playlist, PlaylistCollection y PlaylistArray

Los objetos **playlist**, **PlaylistCollection** y **PlaylistArray** rigen las listas de reproducción que Windows Media Player puede usar para especificar el orden en el que se reproducirá el contenido. Obtiene el objeto **PlaylistCollection** de la propiedad **PlaylistCollection** del objeto **Player** . La propiedad **playlistCollection** devuelve el objeto **playlistCollection** . Solo puede acceder a las propiedades del objeto **PlaylistCollection** una vez creado. Por ejemplo, para crear una nueva lista de reproducción, primero debe obtener el objeto **PlaylistCollection** y, a continuación, usar un método en ese objeto.


```C++
player.playlistcollection.newplaylist('myplaylist');
```



Puede obtener la lista de reproducción actual mediante la propiedad **currentPlaylist** . Por ejemplo, para obtener el nombre de la lista de reproducción actual, use el código siguiente:


```C++
myname = player.currentplaylist.name;
```



Los métodos **getAll** y **GetByName** del objeto **PlaylistCollection** devuelven el objeto **PlaylistArray** . Para obtener el número de listas de reproducción, por ejemplo, use el código siguiente:


```C++
howmany = player.playlistcollection.getAll().count;
```



Para recuperar una lista de reproducción conocida por nombre, use el código siguiente:


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Modelo de objetos del reproductor para lenguajes de scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 




