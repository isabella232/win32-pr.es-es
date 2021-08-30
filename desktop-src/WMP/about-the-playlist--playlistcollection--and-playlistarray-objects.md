---
title: Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray
description: Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Reproductor de Windows Media,objeto Playlist
- Reproductor de Windows Media modelo de objetos, objeto De lista de reproducción
- object model,Playlist object
- control Reproductor de Windows Media ActiveX lista de reproducción, objeto Playlist
- ActiveX control, objeto Lista de reproducción
- Reproductor de Windows Media Control de ActiveX móvil, objeto Lista de reproducción
- Reproductor de Windows Media Mobile,Objeto De lista de reproducción
- Objeto de lista de reproducción
- Reproductor de Windows Media,objeto PlaylistCollection
- Reproductor de Windows Media modelo de objetos, objeto PlaylistCollection
- object model,PlaylistCollection object
- Reproductor de Windows Media ActiveX control, objeto PlaylistCollection
- ActiveX control, objeto PlaylistCollection
- Reproductor de Windows Media Control de ActiveX móvil, objeto PlaylistCollection
- Reproductor de Windows Media Objeto Mobile,PlaylistCollection
- Objeto PlaylistCollection
- Reproductor de Windows Media,objeto PlaylistArray
- Reproductor de Windows Media de objetos, objeto PlaylistArray
- object model,PlaylistArray object
- Reproductor de Windows Media ActiveX control, objeto PlaylistArray
- ActiveX control, objeto PlaylistArray
- Reproductor de Windows Media Control de ActiveX móvil, objeto PlaylistArray
- Reproductor de Windows Media Objeto Mobile,PlaylistArray
- Objeto PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37a20bca66d8d1ff592b71d1f6555641625b4688b7791475a85f7b9a39fa91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956725"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray

Los **objetos Playlist**, **PlaylistCollection** y **PlaylistArray** rigen las listas de reproducción Reproductor de Windows Media pueden usar para especificar el orden en el que se reproducirá el contenido. Obtiene el objeto **PlaylistCollection** de la **propiedad playlistCollection** del **objeto Player.** La **propiedad playlistCollection** devuelve el **objeto PlaylistCollection.** Solo puede acceder a las propiedades del objeto **PlaylistCollection** después de crearlo. Por ejemplo, para crear una nueva lista de reproducción, primero debe obtener el objeto **PlaylistCollection** y, a continuación, usar un método en ese objeto.


```C++
player.playlistcollection.newplaylist('myplaylist');
```



Puede obtener la lista de reproducción actual mediante la **propiedad currentPlaylist.** Por ejemplo, para obtener el nombre de la lista de reproducción actual, use el código siguiente:


```C++
myname = player.currentplaylist.name;
```



Los métodos **getAll** y **getByName** devuelven el objeto **PlaylistArray** del **objeto PlaylistCollection.** Para obtener el número de listas de reproducción, por ejemplo, use el código siguiente:


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

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> </dl>

 

 




