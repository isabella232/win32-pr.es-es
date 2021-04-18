---
title: Objeto MediaCollection
description: El objeto MediaCollection proporciona una manera de organizar una colección grande de elementos multimedia. Se puede consultar para que genere listas de reproducción automáticamente.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Objeto MediaCollection Media Player de Windows
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685650"
---
# <a name="mediacollection-object"></a>Objeto MediaCollection

El objeto **MediaCollection** proporciona una manera de organizar una colección grande de elementos multimedia. Se puede consultar para que genere listas de reproducción automáticamente.

El objeto **MediaCollection** admite los siguientes métodos.



| Método                                                                           | Descripción                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.                                                                                                              |
| [createQuery](mediacollection-createquery.md)                                   | Crea un nuevo objeto de [consulta](query-object.md) .                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene todos los elementos multimedia de la biblioteca.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Recupera un objeto [StringCollection](stringcollection-object.md) que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado. |
| [getByAlbum](mediacollection-getbyalbum.md)                                     | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia del álbum especificado.                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia con el atributo especificado que tiene el valor especificado.                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene objetos [multimedia](media-object.md) que tienen el atributo y el tipo de medio especificados.                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia por el autor especificado.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia con el género especificado.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene elementos multimedia con el nombre especificado.                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | Recupera el índice en el que una propiedad especificada reside en el conjunto de propiedades disponibles.                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | Recupera un objeto de [lista de reproducción](playlist-object.md) que contiene objetos [multimedia](media-object.md) que coinciden con las condiciones de la consulta.                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | Recupera un objeto [StringCollection](stringcollection-object.md) que contiene cadenas que coinciden con las condiciones de la consulta.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Recupera un valor que indica si el elemento multimedia especificado está en la carpeta de elementos eliminados.                                                                  |
| [remove](mediacollection-remove.md)                                             | Quita un elemento de la colección de medios.                                                                                                                     |
| [setDeleted](mediacollection-setdeleted.md)                                     | Mueve el elemento multimedia especificado a la carpeta elementos eliminados.                                                                                                    |



 

Se tiene acceso al objeto **MediaCollection** a través de la propiedad siguiente.



| Object                      | Propiedad                                      |
|-----------------------------|-----------------------------------------------|
| [Reproductor](player-object.md) | [mediaCollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




