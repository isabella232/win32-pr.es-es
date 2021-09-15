---
title: Acceso a la biblioteca mediante programación
description: Acceso a la biblioteca mediante programación
ms.assetid: f48fbb49-5b79-4a78-af72-8509c460a149
keywords:
- Reproductor de Windows Media,library
- Reproductor de Windows Media modelo de objetos,library
- object model,library
- Reproductor de Windows Media ActiveX control,library para el modelo de objetos
- ActiveX control,library para el modelo de objetos
- Reproductor de Windows Media Control de ActiveX móvil,biblioteca para el modelo de objetos
- Reproductor de Windows Media Mobile,library para el modelo de objetos
- Reproductor de Windows Media, acceder mediante programación
- library,accessing
- acceso a Reproductor de Windows Media biblioteca mediante programación
- Reproductor de Windows Media, agregar elementos multimedia
- library,adding media items
- Reproductor de Windows Media, recuperar elementos multimedia
- library,retrieving media items
- Reproductor de Windows Media, quitar elementos multimedia
- library,removing media items
- agregar elementos multimedia a Reproductor de Windows Media biblioteca
- recuperar elementos multimedia de Reproductor de Windows Media biblioteca
- quitar elementos multimedia de Reproductor de Windows Media biblioteca
- recuperar metadatos
- Reproductor de Windows Media, recuperar metadatos de elementos multimedia
- library,retrieving metadata from media items
- metadata,retrieving
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40e03e91b2a67a24cb49b0ac1810ceb7b9544c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473344"
---
# <a name="accessing-the-library-programmatically"></a>Acceso a la biblioteca mediante programación

En el código, la biblioteca se representa mediante el **objeto MediaCollection** (o la **interfaz IWMPMediaCollection).** Los elementos multimedia se representan como **objetos** multimedia (o mediante la **interfaz IWMPMedia).** Los elementos de lista de reproducción se **representan como** objetos de lista de reproducción (o mediante la **interfaz IWMPPlaylist).** Para simplificar, esta sección simplemente hará referencia a los nombres de objeto, siempre que sea posible.

Mediante el uso del **objeto MediaCollection,** puede trabajar con elementos multimedia y listas de reproducción. La biblioteca también expone el objeto **PlaylistCollection** (o la interfaz **IWMPPlaylistCollection),** que proporciona cierta funcionalidad específica para trabajar con listas de reproducción. La mayoría de las veces, el **objeto MediaCollection** le proporcionará la funcionalidad que necesita, incluso cuando se trabaja con listas de reproducción. Para obtener más información sobre cómo trabajar con elementos multimedia, vea [Administrar elementos multimedia.](managing-media-items.md) Para obtener más información sobre cómo trabajar con listas de reproducción, vea [Administración de listas de reproducción.](managing-playlists.md)

## <a name="adding-media-items-to-the-library"></a>Agregar elementos multimedia a la biblioteca

Agregar contenido multimedia digital a la biblioteca es sencillo. Simplemente llame al [método MediaCollection.add](mediacollection-add.md) y proporcione la ruta de acceso al archivo multimedia como argumento.

## <a name="retrieving-media-items-from-the-library"></a>Recuperar elementos multimedia de la biblioteca

Cuando se recuperan elementos multimedia de la biblioteca, lo que realmente se recupera es una lista de reproducción. Incluso si espera recuperar solo un elemento multimedia, recibirá un objeto **Lista** de reproducción que contiene un único elemento, que se asociará con el índice cero. Por ejemplo, si desea recuperar un objeto **Media** que representa la canción denominada "Juana", puede usar el código JScript siguiente:


```C++
// Retrieve media named Jeanne from the library.
var playlist = player.mediaCollection.getByName("Jeanne");

```



El código anterior recupera una lista de reproducción que contiene todos los elementos multimedia que tienen el nombre "Juanne" como título. En este ejemplo, suponga que sabe que solo hay una canción por ese nombre en la biblioteca (tenga en cuenta que la biblioteca admite varias canciones con el mismo nombre). Esto significa que podría esperar que el recuento de elementos de la lista de reproducción que recuperó sea igual a uno y el elemento multimedia se representaría mediante el índice cero. El código de ejemplo siguiente continúa el ejemplo anterior para mostrar cómo recuperaría el elemento multimedia de la lista de reproducción mediante el [método Playlist.item.](playlist-item.md)


```C++
// Retrieve the individual media item from the playlist.
var media = playlist.item(0);

```



Para obtener más información sobre cómo recuperar elementos multimedia de listas de reproducción, vea [Listas](playlists-and-media-items.md) de reproducción y elementos multimedia en la Guía de control [del reproductor](player-control-guide.md).

## <a name="retrieving-metadata-from-a-media-item"></a>Recuperar metadatos de un elemento multimedia

Después de recuperar un **objeto Media,** puede leer los valores de atributo asociados al contenido. En el caso más sencillo, es posible que simplemente quiera conocer un solo valor, como el nombre del intérprete que realizó una pista de música. En el JScript siguiente se muestra cómo usar el método [Media.getItemInfo](media-getiteminfo.md) para recuperar el nombre del intérprete del medio recuperado en el ejemplo anterior:


```C++
// Retrieve the artist name string.
var author = media.getItemInfo("Artist");

```



Un elemento multimedia puede tener muchos atributos diferentes y trabajar con metadatos no siempre es tan sencillo como el caso simple que se muestra en el ejemplo anterior. Por ejemplo, algunos atributos pueden contener varios valores o tener valores en más de un idioma. Para obtener más información sobre cómo trabajar con metadatos, vea [Atributos de elementos multimedia](media-item-attributes.md). Para obtener más información sobre los distintos atributos, sus significados y la compatibilidad con tipos de archivo, vea la Referencia [de atributos](attribute-reference.md).

## <a name="removing-media-items-from-the-library"></a>Quitar elementos multimedia de la biblioteca

La eliminación de contenido multimedia digital de la biblioteca también es sencilla. Simplemente llame **a MediaCollection.remove**, proporcionando el **objeto Media** que representa el elemento como primer argumento y el valor **true** como segundo. En el JScript siguiente se quita de la biblioteca el archivo llamado Juanne (recuperado en el ejemplo anterior):


```C++
// Remove Jeanne from the library.
playst.mediaCollection.remove(media, true);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la biblioteca**](about-the-library.md)
</dt> <dt>

[**Acerca de Los objetos MediaCollection y Media**](about-the-mediacollection-and-media-objects.md)
</dt> <dt>

[**Acerca de los objetos Playlist, PlaylistCollection y PlaylistArray**](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
</dt> <dt>

[**Trabajar con la biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




