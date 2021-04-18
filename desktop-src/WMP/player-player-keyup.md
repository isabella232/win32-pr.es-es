---
title: Evento Player. KeyUp
description: El evento KeyUp se produce cuando se suelta una tecla. | Evento Player. KeyUp
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Media Player de eventos KeyUp de Windows
- Evento KeyUp Windows Media Player, clase Player
- Clase de reproductor Windows Media Player, evento KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690185"
---
# <a name="playerkeyup-event"></a>Evento Player. KeyUp

El evento **KeyUp** se produce cuando se suelta una tecla.

## <a name="syntax"></a>Sintaxis


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Número** (**int**) que especifica qué tecla física se presiona. Para ver los valores posibles, consulte el [evento Player. KeyDown](player-player-keydown.md).

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento Shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





