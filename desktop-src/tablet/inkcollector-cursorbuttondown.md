---
description: 'Evento InkCollector.CursorButtonDown: se produce cuando la clase InkCollector detecta un botón de cursor que está fuera de servicio.'
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Evento InkCollector.CursorButtonDown (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110333"
---
# <a name="inkcollectorcursorbuttondown-event"></a>Evento InkCollector.CursorButtonDown

Se produce cuando [**la clase InkCollector**](inkcollector-class.md) detecta un botón de cursor que está fuera de servicio.

## <a name="syntax"></a>Sintaxis


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorButtonDown.**

</dd> <dt>

*Botón* \[ En\]
</dt> <dd>

Botón que se presionó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Un botón de una punta de lápiz está abajo cuando el usuario baja el lápiz al digitalizador y comienza a realizar el seguimiento de un trazo. Un botón de un menú está apagado cuando se presiona el botón.

Al presionar el botón derecho del mouse, recibe dos eventos **CursorButtonDown:** uno para el botón derecho presionado y otro para el botón izquierdo presionado.

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE \_ DISPID ICECursorButtonDown.

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

[**Evento CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkcollector-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




