---
title: Evento Player. OpenPlaylistSwitch
description: El evento OpenPlaylistSwitch se produce cuando comienza a reproducirse un título en un DVD. | Evento Player. OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Media Player OpenPlaylistSwitch de eventos de Windows
- Evento OpenPlaylistSwitch de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento OpenPlaylistSwitch
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708662"
---
# <a name="playeropenplaylistswitch-event"></a>Evento Player. OpenPlaylistSwitch

El evento **OpenPlaylistSwitch** se produce cuando comienza a reproducirse un título en un DVD.

## <a name="syntax"></a>Sintaxis


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItem* 
</dt> <dd>

Objeto de **lista de reproducción** que representa el título.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





