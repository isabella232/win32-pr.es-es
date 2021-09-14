---
description: Se produce cuando se elimina un trazo del objeto InkDisp.
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: Evento InkDisp.InkDeleted (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251870"
---
# <a name="inkdispinkdeleted-event"></a>Evento InkDisp.InkDeleted

Se produce cuando se elimina un trazo del [**objeto InkDisp.**](inkdisp-class.md)

## <a name="syntax"></a>Sintaxis


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StrokeIds* \[ En\]
</dt> <dd>

Especifica la matriz de enteros de información de identificador de trazo para todos los trazos que se han eliminado cuando se produce este evento.

Para obtener más información sobre la estructura VARIANT, vea [Using the COM Library](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Si usa el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) (donde [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) es igual a [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) y [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) es igual a [**StrokeErase)**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)y pasa el borrador sobre un trazo, se obtiene la siguiente secuencia de eventos:

-   **InkDeleted**
-   [**InkAdded**](inkdisp-inkadded.md)
-   **InkDeleted**

Los eventos [**InkAdded y**](inkdisp-inkadded.md) **InkDeleted** adicionales se producen porque el código subyacente agrega un trazo interno e invisible para realizar el seguimiento del borrador.

Este método de evento se define en la \_ interfaz IInkEvents. La \_ interfaz IInkEvents implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IEInkDeleted.

El **evento InkDeleted** se desencadena incluso cuando está en modo de selección o borrado, no solo al insertar la entrada de lápiz. Esto requiere que supervise el modo de edición (que es responsable de la configuración) y que tenga en cuenta el modo antes de interpretar el evento. La ventaja de este requisito es una mayor libertad para innovar en la plataforma a través de un mayor conocimiento de los eventos de la plataforma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InkDisp (clase)**](inkdisp-class.md)
</dt> <dt>

[**Propiedad EditingMode \[ InkOverlay (clase)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**Clase InkOverlay de la propiedad EraserMode \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**InkAdded (Evento)**](inkdisp-inkadded.md)
</dt> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[Referencia del control InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

