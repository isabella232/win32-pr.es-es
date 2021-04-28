---
description: 'Evento InkPicture.CursorOutOfRange: se produce cuando el cursor sale del intervalo de detección físico (proximidad) del contexto de la tableta.'
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: Evento InkPicture.CursorOutOfRange (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d80584eafb7f1e5222316507f08bd73efb12fae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086573"
---
# <a name="inkpicturecursoroutofrange-event"></a>Evento InkPicture.CursorOutOfRange

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

Objeto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorOutOfRange.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío (dispinterfaces) **\_ de IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador DE DISPID \_ ICECursorOutOfRange.

El **evento CursorOutOfRange** se desencadena incluso cuando está en modo de selección o borrado, no solo cuando está en modo de entrada manuscrita. Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

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

[**Evento CursorInRange**](inkpicture-cursorinrange.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




