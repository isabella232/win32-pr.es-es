---
title: Evento Player.PositionChange
description: El evento PositionChange tiene lugar cuando se ha cambiado la posición actual del elemento multimedia.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Evento PositionChange Reproductor de Windows Media
- Evento PositionChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media , evento PositionChange
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
ms.openlocfilehash: 0156cab32f4a11ec239e7bdfe2b2896a59c44f986f1f1d51b49619e86e6ab4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862405"
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

Number (**double**) que especifica la posición anterior.

</dd> <dt>

*newPosition* 
</dt> <dd>

**Number** (**double**) que especifica la nueva posición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este evento no se genera rutinariamente durante la reproducción. Solo se produce cuando algo cambia activamente la posición actual del elemento multimedia de reproducción, como el usuario que mueve el identificador de búsqueda o el código que especifica un valor para *Controles*. **currentPosition**.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





