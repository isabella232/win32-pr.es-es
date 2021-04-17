---
title: Evento Player. MouseUp
description: El evento MouseUp se produce cuando el usuario suelta un botón del mouse. | Evento Player. MouseUp
ms.assetid: 0f209fc4-2aad-46b1-84ba-2bfbecbe2930
keywords:
- Media Player de eventos MouseUp de Windows
- MouseUp eventos de Windows Media Player, clase Player
- Clase player Windows Media Player, evento MouseUp
topic_type:
- apiref
api_name:
- Player.MouseUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50883ed8e5ea5696bd3aef1c5170959814de3026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708663"
---
# <a name="playermouseup-event"></a>Evento Player. MouseUp

El evento **MouseUp** se produce cuando el usuario suelta un botón del mouse.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MouseUp(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nbotón* 
</dt> <dd>

**Número** (**int**) que especifica un campo de bits con bits correspondientes al botón izquierdo (bit 0), botón derecho (bit 1) y botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, que indica el botón que causó el evento.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Número** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla Ctrl (bit 1) y la tecla Alt (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento Shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

</dd> <dt>

*Efectos* 
</dt> <dd>

**Número** (**largo**) que especifica la coordenada x del puntero del mouse en relación con la esquina superior izquierda del control.

</dd> <dt>

*fY* 
</dt> <dd>

**Número** (**largo**) que especifica la coordenada y del puntero del mouse en relación con la esquina superior izquierda del control.

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

 

 





