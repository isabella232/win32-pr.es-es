---
title: Controls. playItem (método)
description: El método playItem reproduce el elemento multimedia especificado. | Controls. playItem (método)
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- método playItem de Windows Media Player
- método playItem Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método playItem
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700145"
---
# <a name="controlsplayitem-method"></a>Controls. playItem (método)

El método **playItem** reproduce el elemento multimedia especificado.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*theMediaItem* \[ de\]
</dt> <dd>

Objeto **multimedia** que se va a reproducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El elemento multimedia se cargará y reproducirá automáticamente, independientemente del valor de la *configuración*. propiedad **autoStart** . Para cargar un elemento sin reproducirlo automáticamente, establezca la *configuración*. Inicie **automáticamente** en false y asigne un valor a *Player*. **URL**, después del cual se puede llamar a **Play** para empezar a reproducir el elemento.

Nota

**playItem** solo funciona con elementos de *currentPlaylist*. No se admite la llamada a **playItem** con una referencia a un elemento multimedia guardado.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa **playItem** para reproducir un elemento multimedia de la lista de reproducción actual. El elemento que se va a reproducir se elige en función de su posición en la lista de reproducción. El objeto **Player** se creó con ID = "Player".


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> </dl>

 

 





