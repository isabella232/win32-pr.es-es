---
description: Se produce cuando el puntero del mouse se encuentra sobre el objeto InkCollector o InkOverlay y se presiona un botón del mouse.
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Evento InkOverlay. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c011de55543bee08aeda1a8a986b597523ad805d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706958"
---
# <a name="inkoverlaymousedown-event"></a>Evento InkOverlay. MouseDown

Se produce cuando el puntero del mouse se encuentra sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) y se presiona un botón del mouse.

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

Botón del mouse que se presionó.

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Estado de la tecla Mayús.

</dd> <dt>

*PX* \[ de\]
</dt> <dd>

Coordenada X, en píxeles, de un clic del mouse.

</dd> <dt>

*py* \[ de\]
</dt> <dd>

Coordenada Y, en píxeles, de un clic del mouse.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** para cancelar el evento del control primario; de lo contrario, **Variant \_ false**. El valor predeterminado es **Variant \_ false**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para mejorar el rendimiento del lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y [**MouseUp**](inkcollector-mouseup.md) .

> [!Note]  
> Las propiedades pX y pY se encuentran en píxeles, y no las unidades HIMETRIC asociadas al espacio de la tinta. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación que no tiene en cuenta el lápiz y este tipo de aplicación solo entiende píxeles.

 

> [!Note]  
> Algunos controles dependen de una relación específica entre los eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)y [**MouseUp**](inkcollector-mouseup.md) . La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ IPEMouseDown.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Enumeración InkMouseButton**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**Enumeración InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**MouseUp (evento)**](inkcollector-mouseup.md)
</dt> </dl>

 

 




