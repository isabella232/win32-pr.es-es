---
title: Evento Player.OpenPlaylistSwitch
description: El evento OpenPlaylistSwitch tiene lugar cuando comienza a reproducirse un título de un DVD. | Evento Player.OpenPlaylistSwitch
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Evento OpenPlaylistSwitch Reproductor de Windows Media
- Evento OpenPlaylistSwitch Reproductor de Windows Media clase , Player
- Clase player Reproductor de Windows Media evento , OpenPlaylistSwitch
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
ms.openlocfilehash: 5610c4e5a4870b1ad5dc5d12d9d8c315dce630578d5af01f8f428b1af47884e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118835152"
---
# <a name="playeropenplaylistswitch-event"></a>Evento Player.OpenPlaylistSwitch

El **evento OpenPlaylistSwitch** tiene lugar cuando comienza a reproducirse un título de un DVD.

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

**Objeto de** lista de reproducción que representa el título.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





