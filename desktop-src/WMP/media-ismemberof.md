---
title: Método Media.isMemberOf
description: El método isMemberOf devuelve un valor que indica si el elemento multimedia es miembro de la lista de reproducción especificada.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- Método isMemberOf Reproductor de Windows Media
- Método isMemberOf Reproductor de Windows Media , Clase Media
- Clase media Reproductor de Windows Media método , isMemberOf
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068407"
---
# <a name="mediaismemberof-method"></a>Método Media.isMemberOf

El **método isMemberOf** devuelve un valor que indica si el elemento multimedia es miembro de la lista de reproducción especificada.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de reproducción* \[ En\]
</dt> <dd>

**Objeto de** lista de reproducción que puede contener el elemento multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Este método no puede comprobar las listas de reproducción recuperadas a través del **objeto MediaCollection.** Para probar si un elemento multimedia es miembro de una lista de reproducción con nombre determinada, recupere la lista de reproducción con el *reproductor*. *playlistCollection*. **getByName**(*name*). **item**(0). Este método también se puede usar con listas de reproducción de CD y listas de reproducción de metarchivo.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **isMemberOf para** probar si el elemento multimedia actual es miembro de la lista de reproducción denominada Lista de reproducción de ejemplo. Si no es así, el elemento multimedia actual se anexa a la lista de reproducción de ejemplo. El **objeto Player** se creó con id. = "Player".


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
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





