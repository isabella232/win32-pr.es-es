---
description: 'Evento InkOverlay.CursorOutOfRange: se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.'
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: Evento InkOverlay.CursorOutOfRange (Msorganut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a30bfde1e96edfa286e9afeac147dc141c4942
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360277"
---
# <a name="inkoverlaycursoroutofrange-event"></a>Evento InkOverlay.CursorOutOfRange

Se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.

## <a name="syntax"></a>Sintaxis


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorOutOfRange.**](inkcollector-cursoroutofrange.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICECursorOutOfRange.

El [**evento CursorOutOfRange**](inkcollector-cursoroutofrange.md) se desencadena incluso cuando está en modo de selección o borrado, no solo cuando está en modo de entrada manuscrita. Esto requiere que supervise el modo de edición (que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

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

[**Evento CursorInRange**](inkcollector-cursorinrange.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




