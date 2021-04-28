---
description: 'Evento InkPicture.CursorDown: se produce cuando la punta del cursor se pone en contacto con la superficie de la tableta de digitalización.'
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture.CursorDown (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4b6128589ba2d0b87d4369e8bb58aa66eabf23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116703"
---
# <a name="inkpicturecursordown-event"></a>Evento InkPicture.CursorDown

Se produce cuando la punta del cursor se pone en contacto con la superficie de la tableta de digitalización.

## <a name="syntax"></a>Sintaxis


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorDown.**

</dd> <dt>

*Trazo* \[ En\]
</dt> <dd>

Objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se inició cuando el objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) hizo que se iniciara el evento **CursorDown.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Estos métodos de evento se definen en las **\_ interfaces IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents.** Las **\_ interfaces IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** implementan la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de \_ DISPID ICECursorDown.

Use este evento con cuidado porque podría tener un efecto adverso en el rendimiento de la entrada de lápiz si se ejecuta demasiado código en los controladores de eventos. Para mejorar el rendimiento de la entrada de lápiz en tiempo real, oculte o muestre el cursor del mouse en los controladores de eventos [**MouseDown**](inkpicture-mousedown.md) y [**MouseUp.**](inkpicture-mouseup.md)

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

[**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

