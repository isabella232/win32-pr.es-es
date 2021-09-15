---
description: Se produce cuando el puntero del mouse está sobre el control InkPicture y se presiona un botón del mouse.
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: Evento InkPicture.MouseDown (Ms mouseut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e4459f5c304b3350f9cbad6aba69418bd24844
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466548"
---
# <a name="inkpicturemousedown-event"></a>Evento InkPicture.MouseDown

Se produce cuando el puntero del mouse está sobre el control [InkPicture](inkpicture-control-reference.md) y se presiona un botón del mouse.

## <a name="syntax"></a>Sintaxis


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
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

*pX* \[ En\]
</dt> <dd>

Coordenada x, en píxeles, del [**objeto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*pY* \[ En\]
</dt> <dd>

Coordenada y, en píxeles, del [**objeto IInkCursor.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar este evento para el control primario; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Los parámetros pX y pY están en píxeles, y no las unidades HIMETRIC asociadas al sistema de coordenadas del espacio de entrada de lápiz. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no es consciente del lápiz y ese tipo de aplicación solo hace referencia a píxeles.

 

> [!Caution]  
> Algunos controles se basan en una relación específica entre **los eventos MouseDown**, [**MouseMove**](inkpicture-mousemove.md)y [**MouseUp.**](inkpicture-mouseup.md) La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

Este método de evento se define en la **\_ interfaz IInkPictureEvents.** La **\_ interfaz IInkPictureEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de \_ DISPID IPEMouseDown.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

