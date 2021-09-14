---
title: Player.PlaylistCollectionPlaylist Evento agregado
description: El evento PlaylistCollectionPlaylistAdded tiene lugar cuando se agrega una lista de reproducción a la colección de listas de reproducción. | Player.PlaylistCollectionPlaylist Evento agregado
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- PlaylistCollectionPlaylist Se ha agregado un evento Reproductor de Windows Media
- PlaylistCollectionPlaylist Se ha agregado un evento Reproductor de Windows Media clase , Player
- Clase player Reproductor de Windows Media , Evento PlaylistCollectionPlaylistAdded
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359053"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Player.PlaylistCollectionPlaylist Evento agregado

El **evento PlaylistCollectionPlaylistAdded** tiene lugar cuando se agrega una lista de reproducción a la colección de listas de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Cadena** que especifica el nombre de la lista de reproducción que se agregó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El nombre de la lista de reproducción que se agregó se puede usar para recuperar el objeto **Playlist** correspondiente mediante *PlaylistCollection*. **Método getByName.**

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





