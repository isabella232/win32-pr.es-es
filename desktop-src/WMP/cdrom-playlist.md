---
title: CDROM. Playlist
description: La propiedad de lista de reproducción recupera un objeto de lista de reproducción que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- CDROM. Playlist Windows Media Player
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
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695936"
---
# <a name="cdromplaylist"></a>CDROM. Playlist

La propiedad de **lista de reproducción** recupera un objeto de **lista de reproducción** que representa las pistas del CD que se encuentran actualmente en la unidad de CD o en las entradas de título de nivel de raíz de DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto de **lista de reproducción** de solo lectura.

## <a name="remarks"></a>Observaciones

Normalmente, los DVDs se organizan en títulos. Cada título contiene uno o varios capítulos. Cada DVD se crea de forma diferente, por lo que la forma de usar títulos y capítulos depende del autor del contenido.

En el caso de DVD, este método recupera una lista de reproducción que contiene como primer elemento un objeto **multimedia** que representa el DVD. Reproducir el elemento hace que el DVD se reproduzca desde el principio si es el primer juego después de insertar un DVD nuevo o reanudar la reproducción si el DVD es el mismo que el último DVD visualizado. Al establecer este elemento como el actual durante la reproducción, el DVD se reproduce desde el principio.

Los elementos adicionales (objetos **multimedia** ) de la lista de reproducción son títulos de DVD que se representan mediante listas de reproducción anidadas. Al especificar *controles*. **CurrentItem** es igual a uno de estos elementos de lista de reproducción anidados, Windows Media Player establece automáticamente la lista de reproducción anidada como *reproductor*. **currentPlaylist** después del inicio de la reproducción del capítulo. A continuación, puede usar las propiedades, los métodos y los eventos del objeto **currentPlaylist** para trabajar con capítulos de DVD, que también son elementos de lista de reproducción.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Esta propiedad no se admite.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa *CDROM*. **lista de reproducción** para rellenar un elemento de texto HTML, denominado mi texto, con los títulos del CD de audio actualmente en la primera unidad de CD. Use *CdromCollection*. **recuento** para determinar el número de unidades de CD disponibles. El objeto **Player** se creó con ID = "Player".


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDROM (objeto)**](cdrom-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





