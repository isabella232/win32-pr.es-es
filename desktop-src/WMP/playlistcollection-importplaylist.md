---
title: PlaylistCollection. importPlaylist, método
description: El método importPlaylist agrega una lista de reproducción estática a la biblioteca. | PlaylistCollection. importPlaylist, método
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- método importPlaylist de Windows Media Player
- método importPlaylist de Windows Media Player, clase PlaylistCollection
- Clase PlaylistCollection Windows Media Player, método importPlaylist
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718816"
---
# <a name="playlistcollectionimportplaylist-method"></a>PlaylistCollection. importPlaylist, método

El método **importPlaylist** agrega una lista de reproducción estática a la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de reproducción* \[ de\]
</dt> <dd>

Objeto de **lista de reproducción** que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve el objeto de la **lista de reproducción** que se agregó.

## <a name="remarks"></a>Observaciones

Las listas de reproducción que no contienen elementos multimedia no se pueden agregar a la biblioteca mediante este método. Para crear una lista de reproducción vacía en la biblioteca, use el método **reproducción** . A continuación, puede rellenar la lista de reproducción resultante con elementos multimedia mediante la *lista de reproducción*. **appendItem** o *lista de reproducción*. **insertItem**.

Si pasa este método a una lista de reproducción automática, la consulta se ejecuta una vez y el resultado se agrega a la biblioteca como una lista de reproducción estática. Para agregar una lista de reproducción automática a la biblioteca y conservar su comportamiento automático, use *MediaCollection*. **Agregar**. Para obtener más información, vea [listas de reproducción estáticas y automáticas](static-and-auto-playlists.md).

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Administrar listas de reproducción**](managing-playlists.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Lista de reproducción. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Lista de reproducción. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection. reproducción**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





