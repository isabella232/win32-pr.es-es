---
description: 'Evento InkPicture.CursorButtonUp: se produce cuando InkCollector detecta un botón de cursor que está en marcha.'
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: Evento InkPicture.CursorButtonUp (Msplaceut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639d0cbd89e2ca44d8855b6508c5284f59a7c654
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086663"
---
# <a name="inkpicturecursorbuttonup-event"></a>Evento InkPicture.CursorButtonUp

Se produce cuando [**InkCollector detecta**](inkcollector-class.md) un botón de cursor que está en marcha.

## <a name="syntax"></a>Sintaxis


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cursor* \[ En\]
</dt> <dd>

Objeto [**IInkCursor Interface que**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) generó el evento **CursorButtonUp.**

</dd> <dt>

*Botón* \[ En\]
</dt> <dd>

Botón que se ha liberado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Un botón de una punta de lápiz está arriba cuando el usuario completa un trazo y eleva el lápiz del digitalizador. Un botón de un menú está en marcha cuando no se presiona el botón.

Cuando se suelta el botón derecho del mouse, se reciben dos eventos **CursorButtonUp:** uno para el botón derecho hacia arriba y otro para el botón izquierdo hacia arriba.

Este método de evento se define en las **\_ interfaces IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** con un identificador de \_ DISPID ICECursorButtonUp.

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

[**Evento CursorButtonDown**](inkpicture-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorDown**](inkpicture-cursordown.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




