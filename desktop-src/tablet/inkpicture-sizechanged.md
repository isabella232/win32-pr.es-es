---
description: Se produce después de cambiar el tamaño del control InkPicture, en concreto, después de que cambie el valor de la propiedad width o height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: Evento InkPicture. SizeChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002882"
---
# <a name="inkpicturesizechanged-event"></a>Evento InkPicture. SizeChanged

Se produce después de cambiar el tamaño del control [InkPicture](inkpicture-control-reference.md) , en concreto, después de que cambie el valor de la propiedad [**width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) o [**height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .

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

*Izquierda* \[ de\]
</dt> <dd>

Coordenada x del lado izquierdo del control [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

*Parte superior* \[ de\]
</dt> <dd>

Coordenada y de la parte superior del control [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

*Derecha* \[ de\]
</dt> <dd>

Coordenada x del lado derecho del control [InkPicture](inkpicture-control-reference.md) .

</dd> <dt>

*Inferior* \[ de\]
</dt> <dd>

Coordenada y de la parte inferior del control [InkPicture](inkpicture-control-reference.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en la interfaz **\_ IInkPictureEvents** . La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPESizeChanged.

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

 

