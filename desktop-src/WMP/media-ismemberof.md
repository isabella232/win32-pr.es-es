---
title: Método media. isMemberOf
description: El método isMemberOf devuelve un valor que indica si el elemento multimedia es un miembro de la lista de reproducción especificada.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- método isMemberOf de Windows Media Player
- método isMemberOf Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699363"
---
# <a name="mediaismemberof-method"></a>Método media. isMemberOf

El método **isMemberOf** devuelve un valor que indica si el elemento multimedia es un miembro de la lista de reproducción especificada.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de reproducción* \[ de\]
</dt> <dd>

Objeto de **lista de reproducción** que puede contener el elemento multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Este método no puede comprobar las listas de reproducción recuperadas a través del objeto **MediaCollection** . Para probar si un elemento multimedia es miembro de una lista de reproducción con nombre determinada, recupere la lista de reproducción con el *reproductor*. *playlistCollection*. **getByName**(*nombre*). **elemento**(0). Este método también se puede utilizar con listas de reproducción de CD y listas de reproducción de metarchivo.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **isMemberOf** para comprobar si el elemento multimedia actual es un miembro de la lista de reproducción denominada lista de reproducción de ejemplo. Si no es así, el elemento multimedia actual se anexa a la lista de reproducción de ejemplo. El objeto **Player** se creó con ID = "Player".


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

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

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





