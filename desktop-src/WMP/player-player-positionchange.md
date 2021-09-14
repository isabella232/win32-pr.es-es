---
title: Evento Player.PositionChange
description: El evento PositionChange tiene lugar cuando se ha cambiado la posición actual del elemento multimedia.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Evento PositionChange Reproductor de Windows Media
- Evento PositionChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , PositionChange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068361"
---
# <a name="playerpositionchange-event"></a>Evento Player.PositionChange

El **evento PositionChange** tiene lugar cuando se ha cambiado la posición actual del elemento multimedia.

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

Number (**double**) especificando la posición antigua.

</dd> <dt>

*newPosition* 
</dt> <dd>

**Number** (**double**) especificando la nueva posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este evento no se genera rutinariamente durante la reproducción. Solo se produce cuando algo cambia activamente la posición actual del elemento multimedia en reproducción, como el usuario que mueve el identificador de búsqueda o el código que especifica un valor para *Controles*. **currentPosition**.

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
</dt> </dl>

 

 





