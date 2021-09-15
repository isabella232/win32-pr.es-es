---
description: 'Evento InkOverlay.CursorInRange: se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.'
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Evento InkOverlay.CursorInRange (Msorganut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1b48cba731720072aae88aa59b80c569a4aa07b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360279"
---
# <a name="inkoverlaycursorinrange-event"></a>Evento InkOverlay.CursorInRange

Se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.

## <a name="syntax"></a>Sintaxis


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorInRange.**](inkcollector-cursorinrange.md)

</dd> <dt>

*NewCursor* \[ En\]
</dt> <dd>

Si es la primera vez que este recopilador de entrada de lápiz entra en contacto con el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorInRange.**](inkcollector-cursorinrange.md)

</dd> <dt>

*ButtonsState* \[ En\]
</dt> <dd>

Estado de los botones del cursor que generó el [**evento CursorInRange.**](inkcollector-cursorinrange.md)

Para obtener más información sobre la estructura VARIANT, vea [Using the COM Library](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de \_ DISPID ICECursorInRange.

El [**evento CursorInRange**](inkcollector-cursorinrange.md) se desencadena incluso cuando está en modo de selección o borrado, no solo cuando está en modo de lápiz. Esto requiere que supervise el modo de edición (que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Evento CursorOutOfRange**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




