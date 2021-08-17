---
description: 'Evento InkCollector.Stroke: se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.'
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: Evento InkCollector.Stroke (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3ba434e90d1caca0651429be10a11a27accfff327d22f7aa73dc71b7b145ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220798"
---
# <a name="inkcollectorstroke-event"></a>Evento InkCollector.Stroke

Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.

## <a name="syntax"></a>Sintaxis


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento Stroke.**

</dd> <dt>

*Trazo* \[ En\]
</dt> <dd>

Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE** para cancelar el evento; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ de DISPID \_ ICEStroke.

El **evento Stroke** se desencadena cuando se está en el modo de selección o borrado, no solo al insertar entrada manuscrita. Esto requiere que supervise el modo de edición (del que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

> [!Note]  
> El **evento Stroke** se produce cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) Cuando el usuario empieza a dibujar por primera vez un trazo, se agrega inmediatamente a la colección InkStrokes. sin embargo, el **evento Stroke** no se produce hasta que se completa el trazo. Por lo tanto, pueden existir trazos en la colección InkStrokes que el controlador de eventos **Stroke** no ha visto.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[**Colección StrokesAdded Event \[ InkStrokes\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**StrokesDeleted \[ (clase InkOverlay)\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

