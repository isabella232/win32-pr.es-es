---
description: 'Evento InkOverlay.MouseDown: se produce cuando el puntero del mouse está sobre el objeto InkCollector o InkOverlay y se presiona un botón del mouse.'
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Evento InkOverlay.MouseDown (Ms mouseut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b0d605dd36f4cae410de2514542aa15818d4604e4484352c68dac54b40b1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219271"
---
# <a name="inkoverlaymousedown-event"></a>Evento InkOverlay.MouseDown

Se produce cuando el puntero del mouse está sobre el objeto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) y se presiona un botón del mouse.

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

Botón del mouse que se presionó.

</dd> <dt>

*Mayús* \[ En\]
</dt> <dd>

Estado de la tecla MAYÚS.

</dd> <dt>

*pX* \[ En\]
</dt> <dd>

Coordenada X, en píxeles, de un clic del mouse.

</dd> <dt>

*pY* \[ En\]
</dt> <dd>

Coordenada Y, en píxeles, de un clic del mouse.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar el evento para el control primario; en caso contrario, **VARIANT \_ FALSE**. El valor predeterminado es **VARIANT \_ FALSE**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y [**MouseUp.**](inkcollector-mouseup.md)

> [!Note]  
> Las propiedades pX y pY están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.

 

> [!Note]  
> Algunos controles se basan en una relación específica entre [**los eventos MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md)y [**MouseUp.**](inkcollector-mouseup.md) La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IPEMouseDown.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**InkMouseButton (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[**Evento MouseUp**](inkcollector-mouseup.md)
</dt> </dl>

 

 




