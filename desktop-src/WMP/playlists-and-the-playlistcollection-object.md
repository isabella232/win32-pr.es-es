---
title: Listas de reproducción y el objeto PlaylistCollection
description: Listas de reproducción y el objeto PlaylistCollection
ms.assetid: 63c8955b-34ad-447b-b734-657207bcecbb
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, objeto PlaylistCollection
- listas de reproducción de metarchivos, objeto PlaylistCollection
- Listas de reproducción de metarchivo de Windows Media, objeto PlaylistCollection
- Objeto PlaylistCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98744c2c5b97129db2824c42567802a374f90b6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704615"
---
# <a name="playlists-and-the-playlistcollection-object"></a>Listas de reproducción y el objeto PlaylistCollection

El objeto **PlaylistCollection** proporciona acceso a las listas de reproducción de la biblioteca y tiene métodos para crear listas de reproducción nuevas y vacías, así como nuevas listas de reproducción de los metaarchivos.

## <a name="working-with-existing-playlists"></a>Trabajar con listas de reproducción existentes

*PlaylistCollection*. **getAll** y *PlaylistCollection*. cada método de **getByName** devuelve un objeto **PlaylistArray** , que puede contener varias listas de reproducción.

*PlaylistCollection*. **getAll** (método) devuelve todas las listas de reproducción existentes que se encuentran en la biblioteca. Por ejemplo, puede llamar a este método y, a continuación, recuperar las listas de reproducción en el objeto **PlaylistArray** para determinar si ya se ha utilizado un nombre de lista de reproducción determinado, o para mostrar todas las listas de reproducción al usuario. El código de ejemplo de [los atributos](playlist-attributes.md) de la lista de reproducción utiliza el método **getAll** .

*PlaylistCollection*. el método **getByName** devuelve todas las listas de reproducción con un nombre determinado. Puede usar este método para controlar cada una de esas listas de reproducción por separado.

También puede usar el método **getByName** para recuperar una lista de reproducción única por nombre. En ese caso, el objeto **PlaylistArray** tiene solo un elemento. En el siguiente ejemplo de C# se muestra esta técnica.


```C++
IWMPPlaylistArray PlayListArray;
IWMPPlaylist Playlist;
// Store the playlist named "BluesTest" in the array
PlayListArray = Player.playlistCollection.getByName("BluesTest");
// Retrieve the first playlist in the collection.
Playlist = PlaylistArray.Item(0);

```



## <a name="working-with-new-playlists"></a>Trabajar con nuevas listas de reproducción

Puede usar *PlaylistCollection*. método **reproducción** para crear una nueva lista de reproducción vacía. El método devuelve una referencia al nuevo objeto de **lista de reproducción** . Después, puede llamar a la *lista de reproducción*. método **appendItem** para agregar elementos multimedia a la lista de reproducción.

También puede crear una nueva lista de reproducción basada en un metarchivo de lista de reproducción. En primer lugar, pase el nombre de la lista de reproducción y la ruta de acceso al metarchivo al *reproductor*. método **reproducción** . Ese método devuelve una referencia al nuevo objeto de **lista de reproducción** . A continuación, pase el nuevo objeto de **lista de reproducción** a *PlaylistCollection*. método **importPlaylist** para agregarlo a la biblioteca.

Observe la diferencia entre *PlaylistCollection*. método **reproducción** y el *reproductor*. método **reproducción** . El método **PlaylistCollection** crea una lista de reproducción nueva y vacía y la agrega a la biblioteca. El método **Player** crea un nuevo objeto de **lista de reproducción** rellenado, pero no lo agrega a la biblioteca.

A lo largo de este tema, el objeto **Player** se definió de la siguiente manera:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



En el siguiente ejemplo de C# se muestra cómo importar una lista de reproducción de un metarchivo. El argumento *strPListName* especifica el nombre de la nueva lista de reproducción. *StrMetaFileName* especifica el nombre del metarchivo del que se importa la lista de reproducción.


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

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Player. reproducción**](player-newplaylist.md)
</dt> <dt>

[**Lista de reproducción. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Listas de reproducción y elementos multimedia**](playlists-and-media-items.md)
</dt> </dl>

 

 




