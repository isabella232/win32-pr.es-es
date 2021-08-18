---
title: Evento Player.DoubleClick
description: El evento DoubleClick tiene lugar cuando el usuario hace doble clic en un botón del mouse.
ms.assetid: e2055cff-e4b0-49e3-a93a-7084789b6842
keywords:
- Evento DoubleClick Reproductor de Windows Media
- Evento DoubleClick Reproductor de Windows Media , clase Player
- Clase de reproductor Reproductor de Windows Media evento , DoubleClick
topic_type:
- apiref
api_name:
- Player.DoubleClick
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8e6a21c46a8b1c5d7960d70233e38333f9ff2052826bb68d573d4b2f0cd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995925"
---
# <a name="playerdoubleclick-event"></a>Evento Player.DoubleClick

El **evento DoubleClick** tiene lugar cuando el usuario hace doble clic en un botón del mouse.

## <a name="syntax"></a>Sintaxis


```JScript
Player.DoubleClick(
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

**Number** (**int**) que especifica un campo de bits con bits correspondientes al botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, lo que indica el botón que produjo el evento.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

</dd> <dt>

*Fx* 
</dt> <dd>

**Number** (**long**) que especifica la coordenada x del puntero del mouse con respecto a la esquina superior izquierda del control.

</dd> <dt>

*Fy* 
</dt> <dd>

**Number** (**long**) que especifica la coordenada y del puntero del mouse con respecto a la esquina superior izquierda del control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

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

 

 





