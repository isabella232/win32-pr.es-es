---
description: Se produce cuando la rueda del mouse se mueve mientras el control InkPicture tiene el foco.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: Evento InkPicture.MouseWheel (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e139604b4fbfd3293203d82b44be15fa36c090e72f40cfedc8ce0641b75b27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938995"
---
# <a name="inkpicturemousewheel-event"></a>Evento InkPicture.MouseWheel

Se produce cuando la rueda del mouse se mueve mientras el control [InkPicture](inkpicture-control-reference.md) tiene el foco.

## <a name="syntax"></a>Sintaxis


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Botón* \[ En\]
</dt> <dd>

Botón que se presionó.

</dd> <dt>

*Mayús* \[ En\]
</dt> <dd>

Estado de la tecla MAYÚS.

</dd> <dt>

*Delta* \[ En\]
</dt> <dd>

Distancia a la que se ha girado la rueda del mouse.

</dd> <dt>

*x* \[ en\]
</dt> <dd>

Coordenada x, en píxeles, del [**objeto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*y* \[ en\]
</dt> <dd>

Coordenada y, en píxeles, del [**objeto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

VARIANT \_ TRUE para cancelar el evento **MouseWheel** del control primario; de lo contrario, VARIANT \_ FALSE.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Los parámetros *x* e *y están* en píxeles y no las unidades HIMETRIC asociadas al sistema de coordenadas del espacio de entrada de lápiz. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no es consciente del lápiz y ese tipo de aplicación solo hace referencia a píxeles.

 

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de \_ DISPID IPEMouseWheel.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

