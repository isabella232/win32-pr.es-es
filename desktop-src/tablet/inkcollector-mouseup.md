---
description: 'Evento InkCollector.MouseUp: se produce cuando el puntero del mouse está sobre el objeto InkCollector o InkOverlay y se libera un botón del mouse.'
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: Evento InkCollector.MouseUp (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5cf3e746c3fbac19b2dc83fd707fd9c0e9e175ba66e94d545a29eafca78ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032103"
---
# <a name="inkcollectormouseup-event"></a>Evento InkCollector.MouseUp

Se produce cuando el puntero del mouse está sobre el [**objeto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) y se libera un botón del mouse.

## <a name="syntax"></a>Sintaxis


```C++
void MouseUp(
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

Botón del mouse que se ha liberado.

</dd> <dt>

*Mayús* \[ En\]
</dt> <dd>

Estado de la tecla MAYÚS.

</dd> <dt>

*pX* \[ En\]
</dt> <dd>

Coordenada x, en píxeles, de un clic del mouse.

</dd> <dt>

*pY* \[ En\]
</dt> <dd>

Coordenada y, en píxeles, de un clic del mouse.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar el evento del control primario; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y **MouseUp.**

> [!Note]  
> Las propiedades *pX* y *pY están* en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.

 

> [!Note]  
> Algunos controles se basan en una relación específica entre [**los eventos MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md)y **MouseUp.** La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IPEMouseUp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[**InkMouseButton (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




