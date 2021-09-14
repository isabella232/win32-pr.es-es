---
title: Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray
description: Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Reproductor de Windows Media,objeto Playlist
- Reproductor de Windows Media objeto, objeto De lista de reproducción
- object model,Objeto de lista de reproducción
- Reproductor de Windows Media ActiveX control,Objeto De lista de reproducción
- control ActiveX lista de reproducción, objeto
- Reproductor de Windows Media Control de ActiveX móvil,objeto Lista de reproducción
- Reproductor de Windows Media Mobile,Objeto De lista de reproducción
- Objeto de lista de reproducción
- Reproductor de Windows Media,Objeto PlaylistCollection
- Reproductor de Windows Media de objetos, objeto PlaylistCollection
- object model,Objeto PlaylistCollection
- Reproductor de Windows Media ActiveX control,Objeto PlaylistCollection
- ActiveX control,Objeto PlaylistCollection
- Reproductor de Windows Media Control de ActiveX móvil,objeto PlaylistCollection
- Reproductor de Windows Media Objeto Mobile,PlaylistCollection
- Objeto PlaylistCollection
- Reproductor de Windows Media,Objeto PlaylistArray
- Reproductor de Windows Media de objetos, objeto PlaylistArray
- object model,Objeto PlaylistArray
- Reproductor de Windows Media ActiveX control,objeto PlaylistArray
- ActiveX control,objeto PlaylistArray
- Reproductor de Windows Media Control de ActiveX móvil,objeto PlaylistArray
- Reproductor de Windows Media Objeto Mobile,PlaylistArray
- Objeto PlaylistArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890228"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray

Los **objetos Playlist**, **PlaylistCollection** y **PlaylistArray** rigen las listas de reproducción Reproductor de Windows Media pueden usar para especificar el orden en el que se reproducirá el contenido. El objeto **PlaylistCollection se** obtiene de la **propiedad playlistCollection** del **objeto Player.** La **propiedad playlistCollection** devuelve el **objeto PlaylistCollection.** Solo puede acceder a las propiedades del objeto **PlaylistCollection** después de crearlo. Por ejemplo, para crear una nueva lista de reproducción, primero debe obtener el objeto **PlaylistCollection** y, a continuación, usar un método en ese objeto.


```C++
player.playlistcollection.newplaylist('myplaylist');
```



Puede obtener la lista de reproducción actual mediante la **propiedad currentPlaylist.** Por ejemplo, para obtener el nombre de la lista de reproducción actual, use el código siguiente:


```C++
myname = player.currentplaylist.name;
```



Los métodos **getAll** y **getByName** del objeto **PlaylistCollection** devuelven el objeto **PlaylistArray.** Para obtener el número de listas de reproducción, por ejemplo, use el código siguiente:


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

 

 




