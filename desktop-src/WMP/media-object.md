---
title: Objeto multimedia
description: El objeto Media proporciona una manera de especificar o recuperar las propiedades de un elemento multimedia mediante las siguientes propiedades y métodos.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Objeto multimedia Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c1dbcb3dc662a431f279e03697620b80c242c99eb32e3bbcdc26d71796f7e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123315"
---
# <a name="media-object"></a>Objeto multimedia

El **objeto** Media proporciona una manera de especificar o recuperar las propiedades de un elemento multimedia mediante las siguientes propiedades y métodos.

El **objeto Media** admite las siguientes propiedades.



| Propiedad                                         | Descripción                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [attributeCount](media-attributecount.md)       | Recupera el número de atributos que se pueden consultar o establecer para el elemento multimedia.              |
| [duration](media-duration.md)                   | Recupera la duración en segundos del elemento multimedia actual.                                       |
| [durationString](media-durationstring.md)       | Recupera un valor **String** que indica la duración del elemento multimedia actual en formato HH:MM:SS. |
| [error](media-error.md)                         | Recupera un [objeto ErrorItem](erroritem-object.md) si el elemento multimedia tiene una condición de error.    |
| [imageSourceHeight](media-imagesourceheight.md) | Recupera el alto del elemento multimedia actual en píxeles.                                          |
| [imageSourceWidth](media-imagesourcewidth.md)   | Recupera el ancho del elemento multimedia actual en píxeles.                                           |
| [markerCount](media-markercount.md)             | Recupera el número de marcadores del elemento multimedia.                                                 |
| [name](media-name.md)                           | Especifica o recupera el nombre del elemento multimedia.                                                 |
| [sourceURL](media-sourceurl.md)                 | Recupera la dirección URL del elemento multimedia.                                                               |



 

El **objeto Media** admite los métodos siguientes.



| Método                                                       | Descripción                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](media-getattributecountbytype.md) | Recupera el número de atributos asociados con el nombre de atributo y el idioma especificados.            |
| [getAttributeName](media-getattributename.md)               | Recupera el nombre del atributo correspondiente al índice especificado.                                |
| [getItemInfo](media-getiteminfo.md)                         | Recupera el valor del atributo especificado para el elemento multimedia.                                       |
| [getItemInfoByAtom](media-getiteminfobyatom.md)             | Recupera el valor del atributo con el número de índice especificado.                                    |
| [getItemInfoByType](media-getiteminfobytype.md)             | Recupera el valor del atributo correspondiente al nombre de atributo, idioma e índice especificados. |
| [getMarkerName](media-getmarkername.md)                     | Recupera el nombre del marcador en el índice especificado.                                                 |
| [getMarkerTime](media-getmarkertime.md)                     | Recupera la hora del marcador en el índice especificado.                                                 |
| [isIdentical](media-isidentical.md)                         | Recupera un valor que indica si el objeto proporcionado es el mismo que el actual.                 |
| [isMemberOf](media-ismemberof.md)                           | Recupera un valor que indica si el elemento multimedia especificado es miembro de la lista de reproducción especificada.     |
| [isReadOnlyItem](media-isreadonlyitem.md)                   | Recupera un valor que indica si se pueden editar los atributos del elemento multimedia especificado.           |
| [setItemInfo](media-setiteminfo.md)                         | Establece el valor del atributo especificado para el elemento multimedia.                                            |



 

Se **tiene acceso** al objeto Multimedia a través de las siguientes propiedades y métodos.



| Object                          | Propiedad o método                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [Controles](controls-object.md) | [Currentitem](controls-currentitem.md)                                  |
| [Reproductor](player-object.md)     | [currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md) |
| [Lista de reproducción](playlist-object.md) | [item](playlist-item.md)                                                |



 

Dado que es el medio de acceso más común, el *reproductor .* **currentMedia se** usa para fines ilustrativos en las secciones de sintaxis de referencia.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




