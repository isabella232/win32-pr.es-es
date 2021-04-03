---
description: Se produce cuando se cambia el tamaño del control InkPicture (cuando cambian los valores de la propiedad width o height).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: Evento InkPicture. Resize (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083110"
---
# <a name="inkpictureresize-event"></a>InkPicture. Resize (evento)

Se produce cuando se cambia el tamaño del control [InkPicture](inkpicture-control-reference.md) (cuando cambian los valores de la propiedad width o height).

## <a name="syntax"></a>Sintaxis


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Left* 
</dt> <dd>

Número de píxeles desde el lado izquierdo de la ventana que contiene el control en el lado izquierdo del control.

</dd> <dt>

*Top* (Principales) 
</dt> <dd>

Número de píxeles desde la parte superior de la ventana que contiene el control hasta la parte superior del control.

</dd> <dt>

*Right* 
</dt> <dd>

Número de píxeles desde el lado izquierdo de la ventana que contiene el control que se encuentra a la derecha del control.

</dd> <dt>

*Bottom* 
</dt> <dd>

Número de píxeles desde la parte superior de la ventana que contiene el control hasta la parte inferior del control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El nuevo ancho del control en píxeles será igual a la diferencia entre los parámetros *derecho* e *izquierdo* . Del mismo modo, el nuevo alto será igual a la diferencia entre la *parte inferior* y *superior*.

Este método de evento se define en la interfaz **\_ IInkPictureEvents** . La interfaz **\_ IInkPictureEvents** implementa la interfaz IDispatch con un identificador de **DISPID \_ IPEResize**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




