---
description: 'Evento InkCollector.CursorInRange: se produce cuando un cursor entra en el intervalo de detección físico (proximidad) del contexto de la tableta.'
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: Evento InkCollector.CursorInRange (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9b7cd6204b2dbb29f9a46e48ecb12569e1301f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110293"
---
# <a name="inkcollectorcursorinrange-event"></a>Evento InkCollector.CursorInRange

Se produce cuando un cursor entra en el intervalo de detección físico (proximidad) del contexto de la tableta.

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

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange.**

</dd> <dt>

*NewCursor* \[ En\]
</dt> <dd>

**VARIANT \_ TRUE** para indicar que es la primera vez que este recopilador de entrada de lápiz entra en contacto con el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange.** en caso contrario, **VARIANT \_ FALSE**.

</dd> <dt>

*ButtonsState* \[ En\]
</dt> <dd>

Estado de los botones del cursor que generó el **evento CursorInRange.**

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

El método de evento TThis se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ \_ DE DISPID ICECursorInRange.

El **evento CursorInRange** se desencadena incluso en el modo de selección o borrado, no solo cuando está en modo de entrada manuscrita. Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

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

[**Evento CursorOutOfRange**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState (enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




