---
title: Objeto MediaCollection
description: El objeto MediaCollection proporciona una manera de organizar una gran colección de elementos multimedia. Se puede consultar para generar listas de reproducción automáticamente.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Objeto MediaCollection Reproductor de Windows Media
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e529bec203b836f1f1022793a18320a7612cb242de58407ddb998c7410a47cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996255"
---
# <a name="mediacollection-object"></a>Objeto MediaCollection

El **objeto MediaCollection** proporciona una manera de organizar una gran colección de elementos multimedia. Se puede consultar para generar listas de reproducción automáticamente.

El **objeto MediaCollection** admite los métodos siguientes.



| Método                                                                           | Descripción                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.                                                                                                              |
| [createQuery](mediacollection-createquery.md)                                   | Crea un nuevo [objeto Query.](query-object.md)                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | Recupera un objeto [Playlist que](playlist-object.md) contiene todos los elementos multimedia de la biblioteca.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Recupera un objeto [StringCollection que](stringcollection-object.md) representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado. |
| [getByAlbum](mediacollection-getbyalbum.md)                                     | Recupera un objeto [Lista de](playlist-object.md) reproducción que contiene elementos multimedia del álbum especificado.                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | Recupera un objeto [Playlist](playlist-object.md) que contiene elementos multimedia con el atributo especificado con el valor especificado.                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | Recupera un objeto [Playlist que](playlist-object.md) contiene objetos [Media](media-object.md) que tienen el atributo y el tipo de medio especificados.                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | Recupera un objeto [Playlist](playlist-object.md) que contiene elementos multimedia del autor especificado.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Recupera un objeto [Playlist](playlist-object.md) que contiene elementos multimedia con el género especificado.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Recupera un objeto [Playlist](playlist-object.md) que contiene elementos multimedia con el nombre especificado.                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | Recupera el índice en el que reside una propiedad especificada dentro del conjunto de propiedades disponibles.                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | Recupera un objeto [Playlist que](playlist-object.md) contiene objetos [Media](media-object.md) que coinciden con las condiciones de consulta.                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | Recupera un objeto [StringCollection](stringcollection-object.md) que contiene cadenas que coinciden con las condiciones de consulta.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Recupera un valor que indica si el elemento multimedia especificado está en la carpeta de elementos eliminados.                                                                  |
| [remove](mediacollection-remove.md)                                             | Quita un elemento de la colección de medios.                                                                                                                     |
| [setDeleted](mediacollection-setdeleted.md)                                     | Mueve el elemento multimedia especificado a la carpeta de elementos eliminados.                                                                                                    |



 

Se tiene acceso al objeto **MediaCollection** a través de la propiedad siguiente.



| Object                      | Propiedad                                      |
|-----------------------------|-----------------------------------------------|
| [Reproductor](player-object.md) | [mediaCollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




