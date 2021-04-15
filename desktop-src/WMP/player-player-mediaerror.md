---
title: Evento Player. MediaError
description: El evento MediaError se produce cuando el objeto multimedia tiene una condición de error.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Media Player MediaError de eventos de Windows
- Evento MediaError de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709007"
---
# <a name="playermediaerror-event"></a>Evento Player. MediaError

El evento **MediaError** se produce cuando el objeto **multimedia** tiene una condición de error.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaObject* 
</dt> <dd>

Objeto **multimedia** que tiene una condición de error.

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

 

 





