---
title: Evento Player. PlaylistCollectionPlaylistRemoved
description: El evento PlaylistCollectionPlaylistRemoved se produce cuando se quita una lista de reproducción de la colección de listas de reproducción. | Evento Player. PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Media Player PlaylistCollectionPlaylistRemoved de eventos de Windows
- Evento PlaylistCollectionPlaylistRemoved de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento PlaylistCollectionPlaylistRemoved
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a449a7b00516f4fee613722d1cc126eb74227948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709225"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Evento Player. PlaylistCollectionPlaylistRemoved

El evento **PlaylistCollectionPlaylistRemoved** se produce cuando se quita una lista de reproducción de la colección de listas de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Cadena** que especifica el nombre de la lista de reproducción que se ha quitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





