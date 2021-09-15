---
title: Método PlaylistCollection.importPlaylist
description: El método importPlaylist agrega una lista de reproducción estática a la biblioteca. | Método PlaylistCollection.importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- Método importPlaylist Reproductor de Windows Media
- Método importPlaylist Reproductor de Windows Media , clase PlaylistCollection
- Clase PlaylistCollection Reproductor de Windows Media método importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466142"
---
# <a name="playlistcollectionimportplaylist-method"></a>Método PlaylistCollection.importPlaylist

El **método importPlaylist** agrega una lista de reproducción estática a la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de reproducción* \[ En\]
</dt> <dd>

**Objeto de** lista de reproducción que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve el objeto **Playlist** que se agregó.

## <a name="remarks"></a>Observaciones

Las listas de reproducción que no contienen elementos multimedia no se pueden agregar a la biblioteca mediante este método. Para crear una lista de reproducción vacía en la biblioteca, use el **método newPlaylist.** A continuación, puede rellenar la lista de reproducción resultante con elementos multimedia mediante lista *de reproducción*. **appendItem o** *Lista de reproducción.* **insertItem**.

Si pasa este método a una lista de reproducción automática, la consulta se ejecuta una vez y el resultado se agrega a la biblioteca como una lista de reproducción estática. Para agregar una lista de reproducción automática a la biblioteca y conservar su comportamiento automático, use *MediaCollection*. **agregue**. Para obtener más información, vea [Listas de reproducción estáticas y automáticas.](static-and-auto-playlists.md)

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Administración de listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection.remove**](playlistcollection-remove.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





