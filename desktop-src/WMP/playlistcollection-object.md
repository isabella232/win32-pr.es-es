---
title: Objeto PlaylistCollection
description: El objeto PlaylistCollection proporciona una manera de organizar las listas de reproducción.
ms.assetid: 9ea61954-d185-4a77-9016-4d58340a96fc
keywords:
- Objeto PlaylistCollection Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PlaylistCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2266537e0df9fc0ba5527784c254b27313d636d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359469"
---
# <a name="playlistcollection-object"></a>Objeto PlaylistCollection

El **objeto PlaylistCollection** proporciona una manera de organizar las listas de reproducción.

El **objeto PlaylistCollection** admite los métodos siguientes.



| Método                                                  | Descripción                                                                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [getAll](playlistcollection-getall.md)                 | Recupera un objeto [PlaylistArray](playlistarray-object.md) que contiene todas las listas de reproducción de la biblioteca.                |
| [getByName](playlistcollection-getbyname.md)           | Recupera un objeto [PlaylistArray](playlistarray-object.md) que contiene listas de reproducción con el nombre especificado, si existe alguna. |
| [importPlaylist](playlistcollection-importplaylist.md) | Agrega una lista de reproducción estática a la biblioteca.                                                                                   |
| [isDeleted](playlistcollection-isdeleted.md)           | Recupera un valor que indica si la lista de reproducción especificada está en la carpeta de elementos eliminados.                              |
| [newPlaylist](playlistcollection-newplaylist.md)       | Crea una nueva lista de reproducción en la biblioteca.                                                                                   |
| [remove](playlistcollection-remove.md)                 | Quita una lista de reproducción de la biblioteca.                                                                                     |
| [setDeleted](playlistcollection-setdeleted.md)         | Mueve una lista de reproducción a la carpeta de elementos eliminados.                                                                            |



 

Se tiene acceso al objeto **PlaylistCollection** a través de la propiedad siguiente.



| Object                      | Propiedad                                            |
|-----------------------------|-----------------------------------------------------|
| [Reproductor](player-object.md) | [playlistCollection](player-playlistcollection.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




