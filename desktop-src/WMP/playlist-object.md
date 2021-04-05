---
title: Objeto Playlist
description: El objeto Playlist proporciona una manera de organizar los elementos multimedia de una lista para facilitar su manipulación mediante el uso de las siguientes propiedades y métodos.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Objeto de lista de reproducción Windows Media Player
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d517e13f8da103b1f9cee9498cce58a62eaf6462
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076522"
---
# <a name="playlist-object"></a>Objeto Playlist

El objeto **playlist** proporciona una manera de organizar los elementos multimedia de una lista para facilitar su manipulación mediante el uso de las siguientes propiedades y métodos.

El objeto de **lista de reproducción** admite las siguientes propiedades.



| Propiedad                                      | Descripción                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | Recupera el número de atributos asociados a la lista de reproducción. |
| [attributeName](playlist-attributename.md)   | Recupera el nombre de un atributo especificado por un índice.        |
| [count](playlist-count.md)                   | Recupera el número de elementos de la lista de reproducción.                   |
| [name](playlist-name.md)                     | Especifica o recupera el nombre de la lista de reproducción.                 |



 

El objeto de **lista de reproducción** admite los métodos siguientes.



| Método                                  | Descripción                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Agrega un elemento multimedia al final de la lista de reproducción.                                                          |
| **clear**                               | Reservado para uso futuro.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Recupera el valor de un atributo de lista de reproducción.                                                           |
| [insertItem](playlist-insertitem.md)   | Inserta un elemento multimedia en la lista de reproducción de la ubicación especificada.                                      |
| [isIdentical](playlist-isidentical.md) | Recupera un valor que indica si el objeto de **lista de reproducción** proporcionado es idéntico al actual. |
| [item](playlist-item.md)               | Recupera el elemento multimedia en el índice especificado.                                                       |
| [moveItem](playlist-moveitem.md)       | Cambia la ubicación de un elemento en la lista de reproducción.                                                       |
| [removeItem](playlist-removeitem.md)   | Quita el elemento especificado de la lista de reproducción.                                                          |
| [setItemInfo](playlist-setiteminfo.md) | Especifica el valor de un atributo de lista de reproducción.                                                           |



 

Se tiene acceso al objeto de **lista de reproducción** a través de las siguientes propiedades y métodos.



| Object                                              | Propiedad o método                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [-](cdrom-object.md)                           | [automáticas](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [MediaCollection](mediacollection-object.md)       | [getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md) |
| [Reproductor](player-object.md)                         | [currentPlaylist](player-currentplaylist.md), [reproducción](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [PlaylistCollection](playlistcollection-object.md) | [Reproducción](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Dado que es el medio de acceso más común, *Player*. **currentPlaylist** se usa con fines ilustrativos en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




