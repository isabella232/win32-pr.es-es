---
description: Se produce cuando el puntero del mouse se encuentra sobre el control InkPicture y se presiona un botón del mouse.
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: Evento InkPicture. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e4459f5c304b3350f9cbad6aba69418bd24844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277786"
---
# <a name="inkpicturemousedown-event"></a>Evento InkPicture. MouseDown

Se produce cuando el puntero del mouse se encuentra sobre el control [InkPicture](inkpicture-control-reference.md) y se presiona un botón del mouse.

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

*Botón* \[ de de\]
</dt> <dd>

Botón que se presionó.

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Estado de la tecla Mayús.

</dd> <dt>

*PX* \[ de\]
</dt> <dd>

La coordenada x, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*py* \[ de\]
</dt> <dd>

La coordenada y, en píxeles, del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** para cancelar este evento para el control primario; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Los parámetros pX y pY se encuentran en píxeles, y no las unidades HIMETRIC asociadas con el sistema de coordenadas de espacio de tinta. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no es compatible con el lápiz y ese tipo de aplicación solo hace referencia a píxeles.

 

> [!Caution]  
> Algunos controles dependen de una relación específica entre los eventos **MouseDown**, [**MouseMove**](inkpicture-mousemove.md)y [**MouseUp**](inkpicture-mouseup.md) . La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

Este método de evento se define en la interfaz **\_ IInkPictureEvents** . La interfaz **\_ IInkPictureEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IPEMouseDown.

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

 

