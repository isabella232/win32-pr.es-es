---
description: Se produce cuando el puntero del mouse se mueve sobre el control InkPicture.
ms.assetid: b4c703da-0e4a-4d4c-9a6c-0e002344fb2f
title: Evento InkPicture. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5540831594674dd279fc14e822d6b3240b014c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277396"
---
# <a name="inkpicturemousemove-event"></a>Evento InkPicture. MouseMove

Se produce cuando el puntero del mouse se mueve sobre el control [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Sintaxis


```C++
void MouseMove(
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
> Los parámetros *PX* y *py* se encuentran en píxeles, y no las unidades HIMETRIC asociadas con el sistema de coordenadas de espacio de tinta. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no es compatible con el lápiz y ese tipo de aplicación solo hace referencia a píxeles.

 

> [!Caution]  
> Algunos controles dependen de una relación específica entre los eventos [**MouseDown**](inkpicture-mousedown.md), **MouseMove** y [**MouseUp**](inkpicture-mouseup.md) . La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

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

 

