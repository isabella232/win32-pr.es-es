---
title: Playlist. Item (método)
description: El método Item recupera el elemento multimedia en el índice especificado.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método Item
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709216"
---
# <a name="playlistitem-method"></a>Playlist. Item (método)

El método **Item** recupera el elemento multimedia en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice del elemento que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **multimedia** .

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa la *lista de reproducción*. **elemento** para recuperar un elemento multimedia de la lista de reproducción actual en función de la selección del usuario. Se ha creado un elemento SELECT de HTML con el nombre "weblist" y se ha rellenado con los títulos de la lista de reproducción actual. El objeto **Player** se creó con ID = "Player".


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

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

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Lista de reproducción. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Lista de reproducción. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





