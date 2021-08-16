---
description: 'Evento InkOverlay.CursorInRange: se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.'
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Evento InkOverlay.CursorInRange (Msorganut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bcf773a3fcb0b23d26912b6b338c1741c0d9d3e5bded84759cafc1f15506c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220768"
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

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de \_ DISPID ICECursorInRange.

El [**evento CursorInRange**](inkcollector-cursorinrange.md) se desencadena incluso cuando está en modo de selección o borrado, no solo cuando está en modo de lápiz. Esto requiere que supervise el modo de edición (que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
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

 

 




