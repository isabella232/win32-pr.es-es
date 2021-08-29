---
title: Método Controls.playItem
description: El método playItem reproduce el elemento multimedia especificado. | Método Controls.playItem
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- Método playItem Reproductor de Windows Media
- método playItem Reproductor de Windows Media , clase Controls
- Controla la clase Reproductor de Windows Media método , playItem
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
ms.openlocfilehash: c6ea371b2e2593ccf9b16d555c60a150ddb6229a2fd884b894d7be41eb61830c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135728"
---
# <a name="controlsplayitem-method"></a>Método Controls.playItem

El **método playItem** reproduce el elemento multimedia especificado.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*theMediaItem* \[ En\]
</dt> <dd>

**Objeto** multimedia que se va a reproducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El elemento multimedia se cargará y reproducirá automáticamente, independientemente del valor de la *Configuración*. **propiedad autoStart.** Para cargar un elemento sin reproducirlo automáticamente, *establezca Configuración*. **autoStart** a false y asigna un valor al *reproductor*. **Dirección URL**, después **de** la cual se puede llamar a play para empezar a reproducir el elemento.

Nota

**playItem solo** funciona con elementos de *currentPlaylist.* No se admite la llamada a **playItem** con una referencia a un elemento multimedia guardado.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se **usa playItem** para reproducir un elemento multimedia de la lista de reproducción actual. El elemento que se va a reproducir se elige en función de su posición en la lista de reproducción. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> </dl>

 

 





