---
title: Evento Player.MouseMove
description: El evento MouseMove tiene lugar cuando se mueve el puntero del mouse. | Evento Player.MouseMove
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Evento MouseMove Reproductor de Windows Media
- Evento MouseMove Reproductor de Windows Media , clase Player
- Player class Reproductor de Windows Media , MouseMove event
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb864e2a8bf686bd39f2d44ba8f5558516d72034f606579a79c76a5d86ab3990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338110"
---
# <a name="playermousemove-event"></a>Evento Player.MouseMove

El **evento MouseMove** tiene lugar cuando se mueve el puntero del mouse.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nButton* 
</dt> <dd>

**Number** (**int**) especificando un campo de bits con bits correspondientes al botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunos, todos o ninguno de los botones.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

</dd> <dt>

*Fx* 
</dt> <dd>

**Number** **(long)** que especifica la coordenada x del puntero del mouse con respecto a la esquina superior izquierda del control.

</dd> <dt>

*Fy* 
</dt> <dd>

**Number** **(long)** que especifica la coordenada y del puntero del mouse con respecto a la esquina superior izquierda del control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





