---
title: Evento Player. CurrentPlaylistItemAvailable
description: El evento CurrentPlaylistItemAvailable se produce cuando la lista de reproducción actual está disponible. | Evento Player. CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Media Player CurrentPlaylistItemAvailable de eventos de Windows
- Evento CurrentPlaylistItemAvailable de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CurrentPlaylistItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708925"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Evento Player. CurrentPlaylistItemAvailable

El evento **CurrentPlaylistItemAvailable** se produce cuando la lista de reproducción actual está disponible.

## <a name="syntax"></a>Sintaxis


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Cadena** que contiene el nombre del elemento de lista de reproducción actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El nombre de la lista de reproducción actual se puede usar para recuperar el objeto de **lista de reproducción** correspondiente mediante *PlaylistCollection*. método **getByName** .

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

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





