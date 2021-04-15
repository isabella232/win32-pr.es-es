---
title: Player. PositionChange (evento)
description: El evento PositionChange se produce cuando se ha cambiado la posición actual del elemento multimedia.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Media Player de eventos de PositionChange en Windows
- Evento PositionChange Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708830"
---
# <a name="playerpositionchange-event"></a>Player. PositionChange (evento)

El evento **PositionChange** se produce cuando se ha cambiado la posición actual del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*oldPosition* 
</dt> <dd>

Número (**Double**) que especifica la posición anterior.

</dd> <dt>

*newPosition* 
</dt> <dd>

**Número** (**Double**) que especifica la nueva posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este evento no se genera rutinariamente durante la reproducción. Solo se produce cuando algo cambia activamente la posición actual del elemento multimedia de reproducción, como el usuario que mueve el identificador de búsqueda o el código que especifica un valor para *los controles*. **currentPosition**.

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
</dt> </dl>

 

 





