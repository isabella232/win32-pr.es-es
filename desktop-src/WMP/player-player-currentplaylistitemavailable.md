---
title: Evento Player.CurrentPlaylistItemAvailable
description: El evento CurrentPlaylistItemAvailable tiene lugar cuando la lista de reproducción actual está disponible. | Evento Player.CurrentPlaylistItemAvailable
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Evento CurrentPlaylistItemAvailable Reproductor de Windows Media
- Evento CurrentPlaylistItemAvailable Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , CurrentPlaylistItemAvailable
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070999"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Evento Player.CurrentPlaylistItemAvailable

El **evento CurrentPlaylistItemAvailable** tiene lugar cuando la lista de reproducción actual está disponible.

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

El nombre de la lista de reproducción actual se puede usar para recuperar el objeto **Playlist** correspondiente mediante *PlaylistCollection*. **Método getByName.**

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

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





