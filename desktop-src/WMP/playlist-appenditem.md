---
title: Método Playlist.appendItem
description: El método appendItem agrega un elemento multimedia al final de la lista de reproducción.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- Método appendItem Reproductor de Windows Media
- método appendItem Reproductor de Windows Media , clase Playlist
- Clase playlist Reproductor de Windows Media , método appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79361ebcf2ea23b754a7bc86cb6fa4a0af465e4e6619ed692c027bc28eb7aa87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747124"
---
# <a name="playlistappenditem-method"></a>Método Playlist.appendItem

El **método appendItem** agrega un elemento multimedia al final de la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*item* \[ En\]
</dt> <dd>

**Objeto** multimedia que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Lista de reproducción*. **appendItem para** agregar el elemento multimedia actual a la lista de reproducción denominada "ThreeList". El **objeto Player** se creó con ID="Player".


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





