---
title: Listas de reproducción y el objeto PlaylistCollection
description: Listas de reproducción y el objeto PlaylistCollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Reproductor de Windows Media,listas de reproducción
- Reproductor de Windows Media de objetos, listas de reproducción
- object model,playlists
- Reproductor de Windows Media Móvil, listas de reproducción
- Reproductor de Windows Media ActiveX control,listas de reproducción
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción
- ActiveX control,listas de reproducción
- objeto playlists,PlaylistCollection
- metarchivo playlists,Objeto PlaylistCollection
- Windows Listas de reproducción de metarchivo multimedia, objeto PlaylistCollection
- Objeto PlaylistCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e57b11f29c259b3e4174f53fe4ef75d688475d8a42df595f89a0e72fe6f06b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862035"
---
# <a name="playlists-and-the-playlistcollection-object"></a>Listas de reproducción y el objeto PlaylistCollection

El **objeto PlaylistCollection** proporciona acceso a las listas de reproducción de la biblioteca y tiene métodos para crear nuevas listas de reproducción vacías y nuevas listas de reproducción a partir de metarchivos.

## <a name="working-with-existing-playlists"></a>Trabajar con listas de reproducción existentes

*PlaylistCollection*. **getAll** y *PlaylistCollection*. **Los métodos getByName** devuelven un **objeto PlaylistArray,** que puede contener varias listas de reproducción.

*PlaylistCollection*. **El método getAll** devuelve todas las listas de reproducción existentes que se encuentran en la biblioteca. Por ejemplo, puede llamar a este método y, a continuación, recuperar las listas de reproducción en el objeto **PlaylistArray** para determinar si ya se ha usado un nombre de lista de reproducción determinado o para mostrar todas las listas de reproducción al usuario. El código de ejemplo de [Atributos de lista de reproducción](playlist-attributes.md) usa el método **getAll.**

*PlaylistCollection*. **El método getByName** devuelve todas las listas de reproducción con un nombre determinado. Puede usar este método para controlar cada una de esas listas de reproducción por separado.

También puede usar el método **getByName para** recuperar una lista de reproducción única por nombre. En ese caso, el **objeto PlaylistArray** solo tiene un elemento. En el siguiente ejemplo de C# se muestra esta técnica.


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a>Trabajar con nuevas listas de reproducción

Puede usar *PlaylistCollection*. **Método newPlaylist** para crear una nueva lista de reproducción vacía. El método devuelve una referencia al nuevo objeto **Playlist.** A continuación, puede llamar a la lista *de reproducción*. **Método appendItem** para agregar elementos multimedia a la lista de reproducción.

También puede crear una nueva lista de reproducción basada en un metarchivo de lista de reproducción. En primer lugar, pase el nombre de la lista de reproducción y la ruta de acceso al metarchivo al *reproductor*. **Método newPlaylist.** Ese método devuelve una referencia al nuevo objeto **Playlist.** A continuación, pase el **nuevo objeto Playlist** a *PlaylistCollection*. **Método importPlaylist** para agregarlo a la biblioteca.

Observe la diferencia entre *PlaylistCollection*. **Método newPlaylist** y *Player*. **Método newPlaylist.** El **método PlaylistCollection** crea una nueva lista de reproducción vacía y la agrega a la biblioteca. El **método Player** crea un nuevo objeto **Playlist** rellenado, pero no lo agrega a la biblioteca.

A lo largo de este tema, **el objeto Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



En el siguiente ejemplo de C# se muestra cómo importar una lista de reproducción desde un metarchivo. El *argumento strPListName* especifica el nombre de la nueva lista de reproducción. *StrMetaFileName especifica* el nombre del metarchivo desde el que se importa la lista de reproducción.


```C++
private IWMPPlaylist importPlaylist(string strPlaylistName, string strMetaFileName)
{
    IWMPPlaylist  NewPlaylist;
    IWMPPlaylist  ImportPlaylist;

    NewPlaylist = Player.newPlaylist(strPlaylistName, strMetaFileName);
    ImportPlaylist = Player.playlistCollection.importPlaylist(NewPlaylist);

    return ImportPlaylist;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Player.newPlaylist**](player-newplaylist.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Listas de reproducción y elementos multimedia**](playlists-and-media-items.md)
</dt> </dl>

 

 




