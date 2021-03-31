---
title: Listas de reproducción y el objeto MediaCollection
description: Listas de reproducción y el objeto MediaCollection
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- listas de reproducción, objeto MediaCollection
- listas de reproducción de metarchivos, objeto MediaCollection
- Listas de reproducción de metarchivo de Windows Media, objeto MediaCollection
- Objeto MediaCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334b693046e6c78e92a4af901816b57bb9c4cddc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418541"
---
# <a name="playlists-and-the-mediacollection-object"></a>Listas de reproducción y el objeto MediaCollection

El objeto **MediaCollection** proporciona acceso a varias listas de reproducción especiales e incluye un método para crear una nueva lista de reproducción a partir de un metarchivo.

Los métodos siguientes recuperan listas de reproducción especiales:

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

Como sugieren sus nombres, estos métodos recuperan listas de reproducción que contienen todos los elementos multimedia de la biblioteca que coinciden con determinados criterios.

Tenga cuidado de no confundir el *MediaCollection*. método **getByName** con *PlaylistCollection*. método **getByName** . El método **MediaCollection** devuelve un objeto de **lista de reproducción** que contiene todos los elementos multimedia que tienen el nombre especificado. El método **PlaylistCollection** devuelve un objeto **PlaylistArray** que contiene todas las listas de reproducción que tienen el nombre especificado.

Puede usar *MediaCollection*. **agregue** el método para agregar listas de reproducción y elementos multimedia a la biblioteca. Para agregar una lista de reproducción, pase el método a la ruta de acceso al metarchivo que define la lista de reproducción. El método siempre devuelve un objeto **multimedia** . No se puede convertir entre objetos **multimedia** y de **lista de reproducción** . Para trabajar con la lista de reproducción que ha agregado, recupere el objeto de **lista de reproducción** que tiene el mismo nombre que el objeto **multimedia** .

En el siguiente ejemplo de C# se muestra cómo recuperar los elementos multimedia por tipo mediante **MediaCollection**. método **getByAttribute** . Este código recupera los nombres de todos los atributos asociados a un tipo determinado, así como el estado de lectura/escritura o de solo lectura de esos atributos. Genera un único archivo que contiene listas de atributos para los tipos audio, vídeo, radio, lista de reproducción, otros, música y fotografías.


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



Las listas de reproducción estáticas incluyen elementos multimedia específicos. Las listas de reproducción automáticas buscan en la biblioteca cada vez que se abren y pueden contener diferentes elementos multimedia en momentos diferentes. Puede Agregar listas de reproducción estáticas y automáticas a la biblioteca mediante *MediaCollection*. **agregue** el método. También puede Agregar listas de reproducción estáticas mediante *PlaylistCollection*. método **importPlaylist** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Listas de reproducción y el objeto PlaylistCollection**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**Listas de reproducción estáticas y automáticas**](static-and-auto-playlists.md)
</dt> </dl>

 

 




