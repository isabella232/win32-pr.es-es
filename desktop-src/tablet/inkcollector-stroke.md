---
description: Se produce cuando el usuario dibuja un nuevo trazo en cualquier tableta.
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: InkCollector. Stroke (evento) (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e75ee7f3e8129fdab52e62178fe4b8a322807fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696246"
---
# <a name="inkcollectorstroke-event"></a>InkCollector. Stroke (evento)

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

*Cursor* \[ de de\]
</dt> <dd>

El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **Stroke** .

</dd> <dt>

*Trazo* \[ de de\]
</dt> <dd>

Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado.

</dd> <dt>

*Cancelar* \[ in, out\]
</dt> <dd>

**Variante \_ TRUE** para cancelar el evento; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en las \_ \_ interfaces de \_ solo distribución (dispinterfaces) IInkCollectorEvents, IInkOverlayEvents y IINKPICTUREEVENTS con el identificador DISPID \_ ICEStroke.

El evento **Stroke** se desencadena cuando se está en modo de selección o borrado, no solo cuando se inserta una entrada manuscrita. Esto requiere que supervise el modo de edición (que es responsable de establecer) y que sea consciente del modo antes de interpretar el evento. La ventaja de este requisito es mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de plataforma.

> [!Note]  
> El evento **Stroke** se activa cuando el usuario termina de dibujar un trazo, no cuando se agrega un trazo a la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Cuando el usuario comienza a dibujar un trazo por primera vez, se agrega inmediatamente a la colección InkStrokes; sin embargo, el evento **Stroke** no se activa hasta que se completa el trazo. Por lo tanto, los trazos pueden existir en la colección InkStrokes que el controlador de eventos **Stroke** no ha encontrado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkCollector (clase)**](inkcollector-class.md)
</dt> <dt>

[**Colección InkStrokes de eventos StrokesAdded \[\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**StrokesDeleted Event \[ InkOverlay (clase)\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**Interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

