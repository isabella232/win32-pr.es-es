---
title: Método PlaylistCollection.newPlaylist
description: El método newPlaylist crea una nueva lista de reproducción en la biblioteca.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- Método newPlaylist Reproductor de Windows Media
- Método newPlaylist Reproductor de Windows Media , clase PlaylistCollection
- Clase PlaylistCollection Reproductor de Windows Media método , newPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af40d4de424997cb943711d84bf62805f2036afeb551c5d397ce82ae0975e812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334634"
---
# <a name="playlistcollectionnewplaylist-method"></a>Método PlaylistCollection.newPlaylist

El **método newPlaylist** crea una nueva lista de reproducción en la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre de la lista de reproducción que se va a crear.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Comentarios

Este método crea una lista de reproducción vacía en la biblioteca. Para rellenar la lista de reproducción con elementos multimedia, use Lista *de reproducción*. **appendItem o** *Lista de reproducción.* **insertItem**.

Se permiten varias listas de reproducción con el mismo nombre en la biblioteca. Para evitar crear un nombre de lista de reproducción duplicado con este método, use **getByName** y *PlaylistArray*. **count** para determinar si ya existe una lista de reproducción con un nombre determinado.

Los espacios iniciales y finales no se permiten en los nombres de lista de reproducción y se quitan automáticamente del valor especificado para el *parámetro name.*

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se crea una nueva lista de reproducción vacía denominada "ThreeList". El **objeto Player** se creó con ID="Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**PlaylistArray.count**](playlistarray-count.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection.remove**](playlistcollection-remove.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





