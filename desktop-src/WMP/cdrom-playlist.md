---
title: Cdrom.playlist
description: La propiedad de lista de reproducción recupera un objeto Playlist que representa las pistas del CD actualmente en la unidad de CD o las entradas de título de nivel de raíz para DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom.playlist Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29419b68c50718165e49c0fbe9e75487e9154c19243453981ab352f03e8209a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864185"
---
# <a name="cdromplaylist"></a>Cdrom.playlist

La **propiedad de** lista de reproducción recupera un objeto **Playlist** que representa las pistas del CD actualmente en la unidad de CD o las entradas de título de nivel de raíz para DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto Playlist **de** solo lectura.

## <a name="remarks"></a>Comentarios

Normalmente, los DVD se organizan en títulos. Cada título contiene uno o varios capítulos. Cada DVD se ha escrito de forma diferente, por lo que la forma en que se usan los títulos y los capítulos es cosa del autor del contenido.

Para DVD, este método recupera una lista de reproducción que contiene como primer elemento un **objeto Multimedia** que representa el medio de DVD. La reproducción del elemento da como resultado que el DVD se reproduce desde el principio si es la primera reproducción después de insertar un DVD nuevo o reanudar la reproducción si el DVD es el mismo que el último DVD visto. Al establecer este elemento como el actual durante la reproducción, se reproduce el DVD desde el principio.

Los elementos adicionales **(objetos** multimedia) de la lista de reproducción son títulos de DVD representados por listas de reproducción anidadas. Al especificar *Controles*. **currentItem para** que sea igual a uno de estos elementos de lista de reproducción anidados, Reproductor de Windows Media establece automáticamente la lista de reproducción anidada como *Player*. **currentPlaylist después** de que comience la reproducción del capítulo. A continuación, puede usar las propiedades, métodos y eventos del objeto **currentPlaylist** para trabajar con capítulos de DVD, que también son elementos de lista de reproducción.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

**Reproductor de Windows Media 10 Mobile:** Esta propiedad no se admite.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se *usa Cdrom*. **lista** de reproducción para rellenar un elemento de texto HTML, denominado myText, con los títulos del CD de audio que se encuentra actualmente en la primera unidad de CD. Use *CdromCollection*. **count** para determinar el número de unidades de CD disponibles. El **objeto Player** se creó con id. = "Player".


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cdrom (objeto)**](cdrom-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





