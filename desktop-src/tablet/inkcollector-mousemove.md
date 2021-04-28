---
description: 'Evento InkCollector.MouseMove: se produce cuando el puntero del mouse se mueve sobre el objeto InkCollector o InkOverlay.'
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector.MouseMove (Ms mouseut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110163"
---
# <a name="inkcollectormousemove-event"></a>Evento InkCollector.MouseMove

Se produce cuando el puntero del mouse se mueve sobre el objeto [**InkCollector**](inkcollector-class.md) [**o InkOverlay.**](inkoverlay-class.md)

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

> [!Note]  
> Las propiedades *pX* y *pY* están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.

 

> [!Note]  
> Algunos controles se basan en una relación específica entre [**los eventos MouseDown,**](inkcollector-mousedown.md) **MouseMove** y [**MouseUp.**](inkcollector-mouseup.md) La cancelación de algunos de estos eventos puede tener resultados imprevistos.

 

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ IPEMouseMove.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[**InkMouseButton (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




