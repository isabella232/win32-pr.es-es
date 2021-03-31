---
title: Obtener acceso a la biblioteca mediante programación
description: Obtener acceso a la biblioteca mediante programación
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Windows Media Player, biblioteca
- Modelo de objetos de Windows Media Player, biblioteca
- modelo de objetos, biblioteca
- Control ActiveX de Windows Media Player, biblioteca para el modelo de objetos
- Control ActiveX, biblioteca para el modelo de objetos
- Control ActiveX móvil de Windows Media Player, biblioteca para el modelo de objetos
- Windows Media Player Mobile, biblioteca para el modelo de objetos
- Biblioteca de Media Player de Windows, obtener acceso mediante programación
- Biblioteca, acceso
- obtener acceso a la biblioteca de Windows Media Player mediante programación
- Biblioteca de Media Player de Windows, agregar elementos multimedia
- Biblioteca, agregar elementos multimedia
- Biblioteca de Media Player de Windows, recuperar elementos multimedia
- Biblioteca, recuperar elementos multimedia
- Biblioteca de Media Player de Windows, quitar elementos multimedia
- Biblioteca, quitar elementos multimedia
- agregar elementos multimedia a la biblioteca de Windows Media Player
- recuperar elementos multimedia de la biblioteca de Media Player de Windows
- quitar elementos multimedia de la biblioteca de Media Player de Windows
- recuperar metadatos
- Biblioteca de Media Player de Windows, recuperar metadatos de elementos multimedia
- Biblioteca, recuperar metadatos de elementos multimedia
- metadatos, recuperar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418906"
---
# <a name="accessing-the-library-programmatically"></a>Obtener acceso a la biblioteca mediante programación

En el código, la biblioteca se representa mediante el objeto **MediaCollection** (o la interfaz **IWMPMediaCollection** ). Los elementos multimedia se representan como objetos **multimedia** (o mediante la interfaz **IWMPMedia** ). Los elementos de la lista de reproducción se representan como objetos de **lista de reproducción** (o por la interfaz **IWMPPlaylist** ). Para simplificar, esta sección simplemente hará referencia a los nombres de objeto, siempre que sea posible.

Con el objeto **MediaCollection** , puede trabajar con elementos multimedia y listas de reproducción. La biblioteca también expone el objeto **PlaylistCollection** (o la interfaz **IWMPPlaylistCollection** ), que proporciona cierta funcionalidad específica para trabajar con listas de reproducción. La mayoría de las veces, el objeto **MediaCollection** le proporcionará la funcionalidad que necesita, incluso al trabajar con listas de reproducción. Para obtener más información sobre cómo trabajar con elementos multimedia, vea [administrar elementos multimedia](managing-media-items.md). Para obtener más información sobre cómo trabajar con listas de reproducción, consulte [Administración de listas de reproducción](managing-playlists.md).

## <a name="adding-media-items-to-the-library"></a>Agregar elementos multimedia a la biblioteca

Agregar contenido multimedia digital a la biblioteca es sencillo. Simplemente llame al método [MediaCollection. Add](mediacollection-add.md) y proporcione la ruta de acceso al archivo multimedia como un argumento.

## <a name="retrieving-media-items-from-the-library"></a>Recuperar elementos multimedia de la biblioteca

Al recuperar elementos multimedia de la biblioteca, lo que realmente recupera es una lista de reproducción. Incluso si espera recuperar solo un elemento multimedia, obtendrá un objeto de lista de **reproducción** que contiene un solo elemento, que se asociará con el índice cero. Por ejemplo, si desea recuperar un objeto **multimedia** que representa la canción denominada "Jeanne", puede usar el siguiente código JScript:


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



En el código anterior se recupera una lista de reproducción que contiene todos los elementos multimedia que tienen el nombre "Jeanne" como título. En este ejemplo, suponga que sabe que solo hay una canción con ese nombre en la biblioteca (tenga en cuenta que la biblioteca admite varias canciones con el mismo nombre). Esto significa que puede esperar que el número de elementos de la lista de reproducción que recupere sea igual a uno y que el elemento multimedia se represente mediante el índice cero. El código de ejemplo siguiente continúa el ejemplo anterior para mostrar cómo se recuperaría el elemento multimedia de la lista de reproducción mediante el método [playlist. Item](playlist-item.md) .


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Para obtener más información acerca de cómo recuperar elementos multimedia de listas de reproducción, vea [listas de reproducción y elementos multimedia](playlists-and-media-items.md) en la [Guía de control del reproductor](player-control-guide.md).

## <a name="retrieving-metadata-from-a-media-item"></a>Recuperar metadatos de un elemento multimedia

Después de recuperar un objeto **multimedia** , puede leer los valores de atributo asociados con el contenido. En el caso más simple, es posible que solo desee conocer un valor único, como el nombre del artista que realizó una pista de música. En el ejemplo de JScript siguiente se muestra cómo utilizar el método [media. getItemInfo](media-getiteminfo.md) para recuperar el nombre del artista del medio recuperado en el ejemplo anterior:


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Un elemento multimedia puede tener muchos atributos diferentes y trabajar con metadatos no siempre es tan sencillo como el caso simple que se muestra en el ejemplo anterior. Por ejemplo, algunos atributos pueden contener varios valores o tener valores en más de un idioma. Para obtener más información sobre cómo trabajar con metadatos, vea [atributos de elemento multimedia](media-item-attributes.md). Para obtener más información sobre los distintos atributos, su significado y la compatibilidad con tipos de archivo, vea la [referencia de atributo](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Quitar elementos multimedia de la biblioteca

Quitar el contenido multimedia digital de la biblioteca también es sencillo. Simplemente llame a **MediaCollection. Remove**, proporcionando el objeto **multimedia** que representa el elemento como primer argumento y el valor **true** como segundo. En el siguiente ejemplo de JScript se quita el archivo denominado Jeanne (recuperado en el ejemplo anterior) de la biblioteca:


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la biblioteca**](about-the-library.md)
</dt> <dt>

[**Acerca de los objetos MediaCollection y multimedia**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**Acerca de los objetos playlist, PlaylistCollection y PlaylistArray**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




