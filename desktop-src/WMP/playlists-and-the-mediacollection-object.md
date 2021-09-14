---
title: Listas de reproducción y el objeto MediaCollection
description: Listas de reproducción y el objeto MediaCollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Reproductor de Windows Media,listas de reproducción
- Reproductor de Windows Media modelo de objetos, listas de reproducción
- modelo de objetos, listas de reproducción
- Reproductor de Windows Media Móvil, listas de reproducción
- Reproductor de Windows Media ActiveX control,listas de reproducción
- Reproductor de Windows Media Control de ActiveX móviles, listas de reproducción
- ActiveX control,listas de reproducción
- playlists,objeto MediaCollection
- listas de reproducción de metarchivo, objeto MediaCollection
- Windows Listas de reproducción de metarchivos multimedia, objeto MediaCollection
- Objeto MediaCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359456"
---
# <a name="playlists-and-the-mediacollection-object"></a>Listas de reproducción y el objeto MediaCollection

El **objeto MediaCollection** proporciona acceso a una variedad de listas de reproducción especiales e incluye un método para crear una nueva lista de reproducción a partir de un metarchivo.

Los métodos siguientes recuperan listas de reproducción especiales:

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Como sugieren sus nombres, estos métodos recuperan listas de reproducción que contienen todos los elementos multimedia de la biblioteca que coinciden con determinados criterios.

Tenga cuidado de no confundir *MediaCollection.* **Método getByName** con *PlaylistCollection*. **Método getByName.** El **método MediaCollection** devuelve un objeto **Playlist** que contiene todos los elementos multimedia que tienen el nombre especificado. El **método PlaylistCollection** devuelve un **objeto PlaylistArray** que contiene todas las listas de reproducción que tienen el nombre especificado.

Puede usar *MediaCollection*. **Agregar** método para agregar listas de reproducción, así como elementos multimedia a la biblioteca. Para agregar una lista de reproducción, pase al método la ruta de acceso al metarchivo que define la lista de reproducción. El método siempre devuelve un **objeto** Media. No se puede convertir entre **objetos Multimedia** y **Lista de** reproducción. Para trabajar con la lista de reproducción que agregó, recupere el objeto **Lista de** reproducción que tiene el mismo nombre que el **objeto** Multimedia.

En el siguiente ejemplo de C# se muestra cómo recuperar medios por tipo mediante **MediaCollection**. **Método getByAttribute.** Este código recupera los nombres de todos los atributos asociados a un tipo determinado, así como el estado de lectura/escritura o de solo lectura de esos atributos. Genera un único archivo que contiene listas de atributos para los tipos Audio, Vídeo, Radio, Lista de reproducción, Otros, Música y Foto.


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



En el siguiente ejemplo de C# se muestra cómo agregar una lista de reproducción de un metarchivo a la biblioteca.


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



Las listas de reproducción estáticas incluyen elementos multimedia específicos. Las listas de reproducción automáticas buscan en la biblioteca cada vez que se abren y pueden contener diferentes elementos multimedia en momentos diferentes. Puede agregar listas de reproducción estáticas y automáticas a la biblioteca mediante *MediaCollection*. **add** method. También puede agregar listas de reproducción estáticas mediante *PlaylistCollection*. **Método importPlaylist.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Listas de reproducción y el objeto PlaylistCollection**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Listas de reproducción estáticas y automáticas**](static-and-auto-playlists.md)
</dt> </dl>

 

 




