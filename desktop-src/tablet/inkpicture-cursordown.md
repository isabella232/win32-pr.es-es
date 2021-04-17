---
description: Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture. CursorDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546555"
---
# <a name="inkpicturecursordown-event"></a>Evento InkPicture. CursorDown

Se produce cuando la sugerencia del cursor se pone en contacto con la superficie de la tableta de la digitalización.

## <a name="syntax"></a>Sintaxis


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ de de\]
</dt> <dd>

El objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el evento **CursorDown** .

</dd> <dt>

*Trazo* \[ de de\]
</dt> <dd>

El objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) provocó que se activara el evento **CursorDown** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Estos métodos de evento se definen en las interfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** . Las interfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** y **\_ IInkPictureEvents** implementan la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ ICECursorDown.

Utilice este evento con precaución, ya que podría tener un efecto adverso en el rendimiento de las entradas manuscritas si se ejecuta demasiado código en los controladores de eventos. Para mejorar el rendimiento del lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp**](inkpicture-mouseup.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Interfaz IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Interfaz IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

