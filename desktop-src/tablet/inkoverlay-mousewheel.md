---
description: 'Evento InkOverlay.MouseWheel: se produce cuando la rueda del mouse se mueve mientras el objeto InkCollector o InkOverlay tiene el foco.'
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Evento InkOverlay.MouseWheel (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468dbdac09fd40144768e8342791d5712a570bcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256653"
---
# <a name="inkoverlaymousewheel-event"></a>Evento InkOverlay.MouseWheel

Se produce cuando la rueda del mouse se mueve mientras el [**objeto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) tiene el foco.

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

Botón del mouse que se presionó.

</dd> <dt>

*Mayús* \[ En\]
</dt> <dd>

Estado de la tecla MAYÚS.

</dd> <dt>

*Delta* \[ En\]
</dt> <dd>

Recuento con firma del número de detents que ha girado la rueda del mouse. Un paso es una muesca de la rueda del mouse.

</dd> <dt>

*x* \[ en\]
</dt> <dd>

Coordenada x, en píxeles, de un clic del mouse.

</dd> <dt>

*y* \[ en\]
</dt> <dd>

Coordenada y, en píxeles, de un clic del mouse.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

Si el evento se debe cancelar para el control primario. El valor predeterminado es **FALSE,** que especifica que no se debe cancelar el evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Las propiedades *pX* y *pY* están en píxeles y no las unidades HIMETRIC asociadas al espacio de entrada de lápiz. Esto se debe a que este evento reemplaza el evento de mouse relacionado de una aplicación sin conocimiento de lápiz y este tipo de aplicación solo entiende píxeles.

 

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador de \_ DISPID \_ IPEMouseWheel.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**InkMouseButton (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[**InkShiftKeyModifierFlags (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




