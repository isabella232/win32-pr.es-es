---
description: 'Evento InkPicture.CursorInRange: se produce cuando un cursor entra en el intervalo de detección física (proximidad) del contexto de la tableta.'
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: Evento InkPicture.CursorInRange (Msiguaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05d703022e8d97df0d8d74a73e20af3d91b8531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086583"
---
# <a name="inkpicturecursorinrange-event"></a>Evento InkPicture.CursorInRange

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

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange.**

</dd> <dt>

*NewCursor* \[ En\]
</dt> <dd>

**VARIANT \_ TRUE** si es la primera vez que este recopilador de entrada de lápiz entra en contacto con el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorInRange;** de lo contrario, **VARIANT \_ FALSE**.

</dd> <dt>

*ButtonsState* \[ En\]
</dt> <dd>

Estado de los botones del cursor que generó el **evento CursorInRange.**

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** interfaz de solo distribución (dispinterfaces) con un identificador DE DISPID \_ ICECursorInRange.

El **evento CursorInRange** se desencadena incluso cuando está en modo de selección o borrado, no solo cuando está en modo de lápiz. Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento CursorOutOfRange**](inkpicture-cursoroutofrange.md)
</dt> <dt>

[**InkCursorButtonState (Enumeración)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




