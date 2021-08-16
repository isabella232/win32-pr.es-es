---
title: Evento Player.PlaylistCollectionPlaylistRemoved
description: El evento PlaylistCollectionPlaylistRemoved tiene lugar cuando se quita una lista de reproducción de la colección de listas de reproducción. | Evento Player.PlaylistCollectionPlaylistRemoved
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- Lista de reproducciónRemoved event Reproductor de Windows Media
- Evento PlaylistCollectionPlaylistRemoved Reproductor de Windows Media , Clase Player
- Clase player Reproductor de Windows Media , Evento PlaylistCollectionPlaylistRemoved
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
ms.openlocfilehash: 456f7598b9e1f1d2c2a6e76e58a0b06142980835c3c6d71d9ab10c2230ac386f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118337979"
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

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





