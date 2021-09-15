---
description: 'Evento InkOverlay.CursorDown: se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.'
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: Evento InkOverlay.CursorDown (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ed26c672aadc9fa19f6a6426fed7339752448d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360280"
---
# <a name="inkoverlaycursordown-event"></a>Evento InkOverlay.CursorDown

Se produce cuando la punta del cursor se pone en contacto con la superficie digitalizadora de la tableta.

## <a name="syntax"></a>Sintaxis


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorDown.**](inkcollector-cursordown.md)

</dd> <dt>

*Trazo* \[ En\]
</dt> <dd>

Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) hizo que se iniciara el evento [**CursorDown.**](inkcollector-cursordown.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents. Las \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents e IInkPictureEvents implementan la interfaz IDispatch con un identificador \_ [](/windows/win32/api/oaidl/nn-oaidl-idispatch) \_ DEPID ICECursorDown.

Use este evento con cuidado porque podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos. Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkcollector-mousedown.md) y [**MouseUp.**](inkcollector-mouseup.md)

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

[**Evento CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

