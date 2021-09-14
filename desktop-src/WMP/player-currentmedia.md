---
title: Player.currentMedia
description: La propiedad currentMedia especifica o recupera el objeto Media actual.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player.currentMedia Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242439"
---
# <a name="playercurrentmedia"></a>Player.currentMedia

La **propiedad currentMedia** especifica o recupera el objeto Media actual.

## <a name="syntax"></a>Sintaxis

*player* . **currentMedia**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto Multimedia de lectura y escritura.

## <a name="remarks"></a>Observaciones

Si el *Configuración*. **La propiedad autoStart** es true, la reproducción se inicia automáticamente cada vez que se establece **currentMedia.**

Esta propiedad toma un objeto Media, que se puede adquirir mediante la lista de *reproducción*. **elemento**. Para cargar un **elemento Multimedia** con un nombre de archivo, establezca la propiedad URL o use **newMedia**.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se recupera el primer elemento multimedia de la biblioteca. A continuación, usa **currentMedia** para convertir el elemento multimedia recuperado en el elemento multimedia actual y, a continuación, para mostrar el nombre del elemento multimedia actual. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.newMedia**](player-newmedia.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Configuración.autoStart**](settings-autostart.md)
</dt> </dl>

 

 





