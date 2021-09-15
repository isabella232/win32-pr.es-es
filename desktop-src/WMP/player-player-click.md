---
title: Evento Player.Click
description: El evento Click tiene lugar cuando el usuario hace clic en un botón del mouse.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Haga clic en event Reproductor de Windows Media
- Haga clic en event Reproductor de Windows Media , Player (Clase)
- Clase de reproductor Reproductor de Windows Media evento , Click
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359269"
---
# <a name="playerclick-event"></a>Evento Player.Click

El **evento Click** tiene lugar cuando el usuario hace clic en un botón del mouse.

## <a name="syntax"></a>Sintaxis


```JScript
Player.Click(
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

**Number** (**int**) que especifica un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas.

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

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media, y se puede acceder a un método de un archivo JScript importado o pasarlo con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

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

 

 





