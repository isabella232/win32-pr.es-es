---
title: Método playlist. appendItem
description: El método appendItem agrega un elemento multimedia al final de la lista de reproducción.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- método appendItem de Windows Media Player
- método appendItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método appendItem
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
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708781"
---
# <a name="playlistappenditem-method"></a>Método playlist. appendItem

El método **appendItem** agrega un elemento multimedia al final de la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*elemento* \[ de de\]
</dt> <dd>

Objeto **multimedia** que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa la *lista de reproducción*. **appendItem** para agregar el elemento multimedia actual a la lista de reproducción denominada "ThreeList". El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





