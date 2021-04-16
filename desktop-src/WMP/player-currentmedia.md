---
title: Player. currentMedia
description: La propiedad currentMedia especifica o recupera el objeto multimedia actual.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Media Player de Windows Player. currentMedia
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699697"
---
# <a name="playercurrentmedia"></a>Player. currentMedia

La propiedad **currentMedia** especifica o recupera el objeto multimedia actual.

## <a name="syntax"></a>Sintaxis

*reproductor* . **currentMedia**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto multimedia de lectura/escritura.

## <a name="remarks"></a>Observaciones

Es si se trata de la *configuración*. la propiedad **autoStart** es true, la reproducción se inicia automáticamente cada vez que se establece **currentMedia**.

Esta propiedad toma un objeto multimedia, que se puede adquirir mediante la *lista de reproducción*. **elemento**. Para cargar un elemento **multimedia** con un nombre de archivo, establezca la propiedad URL o use **newMedia**.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se recupera el primer elemento multimedia de la biblioteca. A continuación, usa **currentMedia** para convertir el elemento multimedia recuperado en el elemento multimedia actual y, después, para mostrar el nombre del elemento multimedia actual. El objeto **Player** se creó con ID = "Player".


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player. newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Configuración. Inicio automático**](settings-autostart.md)
</dt> </dl>

 

 





