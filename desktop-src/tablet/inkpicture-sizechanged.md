---
description: Se produce después de cambiar el tamaño del control InkPicture, en concreto, después de que cambie el valor de la propiedad Width o Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture.SizeChanged (Msalterut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4473bf580e1683c8d410cd1f2cdbaf271302485f51556b68c4fae7a5d6b99ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032043"
---
# <a name="inkpicturesizechanged-event"></a>Evento InkPicture.SizeChanged

Se produce después de cambiar el tamaño del control [InkPicture,](inkpicture-control-reference.md) en concreto, después de que cambie el valor de la propiedad [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**Height.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)

## <a name="syntax"></a>Sintaxis


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Izquierda* \[ En\]
</dt> <dd>

Coordenada x del lado izquierdo del control [InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*Parte superior* \[ En\]
</dt> <dd>

Coordenada y de la parte superior del control [InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*Derecho* \[ En\]
</dt> <dd>

Coordenada x del lado derecho del control [InkPicture.](inkpicture-control-reference.md)

</dd> <dt>

*Inferior* \[ En\]
</dt> <dd>

Coordenada y de la parte inferior del control [InkPicture.](inkpicture-control-reference.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPESizeChanged.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

