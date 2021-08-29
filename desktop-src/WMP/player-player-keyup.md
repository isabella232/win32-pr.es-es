---
title: Evento Player.KeyUp
description: El evento KeyUp tiene lugar cuando se libera una clave. | Evento Player.KeyUp
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Evento KeyUp Reproductor de Windows Media
- Evento KeyUp Reproductor de Windows Media , clase Player
- Player class Reproductor de Windows Media , KeyUp event
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
ms.openlocfilehash: 46134b675f06e0d9febcfa29ec31f8939aac606028342cd829e92e757465c49a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134797"
---
# <a name="playerkeyup-event"></a>Evento Player.KeyUp

El **evento KeyUp** tiene lugar cuando se libera una clave.

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

**Number** (**int**) que especifica la tecla física que se presiona. Para obtener los valores posibles, [vea Player.KeyDown Event](player-player-keydown.md).

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





