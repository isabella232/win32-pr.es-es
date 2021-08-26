---
description: Se produce cuando se agrega un trazo al objeto InkDisp.
ms.assetid: 46bbdb98-524f-4b4b-95c0-005e71d672f1
title: Evento InkDisp.InkAdded (Msdisput.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a6260660817d38795978371e99b241e3b5b2a88de2d9f2b6d3da678f117b522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939145"
---
# <a name="inkdispinkadded-event"></a>Evento InkDisp.InkAdded

Se produce cuando se agrega un trazo al [**objeto InkDisp.**](inkdisp-class.md)

## <a name="syntax"></a>Sintaxis


```C++
void InkAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StrokeIds* \[ En\]
</dt> <dd>

Matriz de enteros de información de identificador de trazo para todos los trazos que se han agregado cuando se produce este evento.

Para obtener más información sobre la estructura VARIANT, vea [Using the COM Library](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Si usa el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) (donde [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) es igual a [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) y [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) es igual a [**StrokeErase)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)y pasa el borrador sobre un trazo, se obtiene la siguiente secuencia de eventos:

-   [**InkDeleted**](inkdisp-inkdeleted.md)
-   **InkAdded**
-   [**InkDeleted**](inkdisp-inkdeleted.md)

Los eventos **InkAdded y** [**InkDeleted**](inkdisp-inkdeleted.md) adicionales se producen porque el código subyacente agrega un trazo interno e invisible para realizar el seguimiento del borrador.

Este método de evento se define en la \_ interfaz IInkEvents. La \_ interfaz IInkEvents implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IEInkAdded.

El **evento InkAdded** se desencadena incluso cuando se está en modo de selección o borrado, no solo al insertar la entrada de lápiz. Esto requiere que supervise el modo de edición (que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkDisp (clase)**](inkdisp-class.md)
</dt> <dt>

[**Propiedad EditingMode \[ InkOverlay (clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**Clase InkOverlay de la propiedad EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**InkDeleted (evento)**](inkdisp-inkdeleted.md)
</dt> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[Referencia del control InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

