---
title: Objeto de lista de reproducción
description: El objeto Lista de reproducción proporciona una manera de organizar los elementos multimedia en una lista para facilitar la manipulación mediante las siguientes propiedades y métodos.
ms.assetid: c2d2f265-b207-4b82-bb76-aee467f00659
keywords:
- Lista de reproducción de objetos Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Playlist Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0709b24779d3aac90d496b38b4654596479ad7a9122660158b53b4b2e75ba622
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336723"
---
# <a name="playlist-object"></a>Objeto de lista de reproducción

El **objeto Lista** de reproducción proporciona una manera de organizar los elementos multimedia en una lista para facilitar la manipulación mediante las siguientes propiedades y métodos.

El **objeto Playlist** admite las siguientes propiedades.



| Propiedad                                      | Descripción                                                      |
|-----------------------------------------------|------------------------------------------------------------------|
| [attributeCount](playlist-attributecount.md) | Recupera el número de atributos asociados a la lista de reproducción. |
| [attributeName](playlist-attributename.md)   | Recupera el nombre de un atributo especificado por un índice.        |
| [count](playlist-count.md)                   | Recupera el número de elementos de la lista de reproducción.                   |
| [name](playlist-name.md)                     | Especifica o recupera el nombre de la lista de reproducción.                 |



 

El **objeto Playlist** admite los métodos siguientes.



| Método                                  | Descripción                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------|
| [appendItem](playlist-appenditem.md)   | Agrega un elemento multimedia al final de la lista de reproducción.                                                          |
| **clear**                               | Reservado para uso futuro.                                                                               |
| [getItemInfo](playlist-getiteminfo.md) | Recupera el valor de un atributo de lista de reproducción.                                                           |
| [insertItem](playlist-insertitem.md)   | Inserta un elemento multimedia en la lista de reproducción en la ubicación especificada.                                      |
| [isIdentical](playlist-isidentical.md) | Recupera un valor que indica si el objeto **Playlist** proporcionado es idéntico al actual. |
| [item](playlist-item.md)               | Recupera el elemento multimedia en el índice especificado.                                                       |
| [moveItem](playlist-moveitem.md)       | Cambia la ubicación de un elemento en la lista de reproducción.                                                       |
| [removeItem](playlist-removeitem.md)   | Quita el elemento especificado de la lista de reproducción.                                                          |
| [setItemInfo](playlist-setiteminfo.md) | Especifica el valor de un atributo de lista de reproducción.                                                           |



 

Se **tiene acceso** al objeto Playlist a través de las siguientes propiedades y métodos.



| Object                                              | Propiedad o método                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cdrom](cdrom-object.md)                           | [Reproducción](cdrom-playlist.md)                                                                                                                                                                                                                                                     |
| [MediaCollection](mediacollection-object.md)       | [getAll](mediacollection-getall.md), [getByAlbum](mediacollection-getbyalbum.md), [getByAttribute](mediacollection-getbyattribute.md), [getByAuthor](mediacollection-getbyauthor.md), [getByGenre](mediacollection-getbygenre.md), [getByName](mediacollection-getbyname.md) |
| [Reproductor](player-object.md)                         | [currentPlaylist](player-currentplaylist.md), [newPlaylist](player-newplaylist.md)                                                                                                                                                                                               |
| [PlaylistArray](playlistarray-object.md)           | [item](playlistarray-item.md)                                                                                                                                                                                                                                                     |
| [PlaylistCollection](playlistcollection-object.md) | [newPlaylist](playlistcollection-newplaylist.md)                                                                                                                                                                                                                                  |



 

Dado que es el medio de acceso más común, el *reproductor .* **currentPlaylist** se usa para fines ilustrativos en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




