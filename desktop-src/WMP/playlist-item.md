---
title: Método Playlist.item
description: El método item recupera el elemento multimedia en el índice especificado.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- método item Reproductor de Windows Media
- método item Reproductor de Windows Media , clase Playlist
- Clase playlist Reproductor de Windows Media método , item
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466171"
---
# <a name="playlistitem-method"></a>Método Playlist.item

El **método** item recupera el elemento multimedia en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice del elemento que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto** Media.

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Lista de reproducción*. **elemento para** recuperar un elemento multimedia de la lista de reproducción actual en función de una selección de usuario. Se creó un elemento HTML SELECT con el nombre "weblist" y se rellena con los títulos de la lista de reproducción actual. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





