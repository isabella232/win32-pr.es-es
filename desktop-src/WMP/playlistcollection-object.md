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
ms.openlocfilehash: 73f1d9df153aea39880728619787e334430eeccf494b6757a59509ec2df2a6b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862215"
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

 

 




