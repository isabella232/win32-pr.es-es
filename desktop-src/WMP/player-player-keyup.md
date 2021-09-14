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
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070982"
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

## <a name="remarks"></a>Observaciones

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

 

 





