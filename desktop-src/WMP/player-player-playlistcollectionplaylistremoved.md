---
title: Evento Player.PlaylistCollectionPlaylistRemoved
description: El evento PlaylistCollectionPlaylistRemoved tiene lugar cuando se quita una lista de reproducción de la colección de listas de reproducción. | Evento Player.PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Evento PlaylistCollectionPlaylistRemoved Reproductor de Windows Media
- Evento PlaylistCollectionPlaylistRemoved Reproductor de Windows Media clase , Player
- Clase player Reproductor de Windows Media evento , PlaylistCollectionPlaylistRemoved
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068364"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Evento Player.PlaylistCollectionPlaylistRemoved

El **evento PlaylistCollectionPlaylistRemoved** tiene lugar cuando se quita una lista de reproducción de la colección de listas de reproducción.

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

**Cadena** que especifica el nombre de la lista de reproducción que se quitó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





