---
description: 'Evento InkCollector.CursorButtonUp: se produce cuando InkCollector detecta un botón de cursor que está encendido.'
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: Evento InkCollector.CursorButtonUp (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936b050c64d07a6957039278f0455bc71d77dbdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110313"
---
# <a name="inkcollectorcursorbuttonup-event"></a>Evento InkCollector.CursorButtonUp

Se produce cuando [**InkCollector detecta**](inkcollector-class.md) un botón de cursor que está encendido.

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

Objeto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el **evento CursorButtonUp.**

</dd> <dt>

*Botón* \[ En\]
</dt> <dd>

Botón que se ha liberado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Un botón de una punta de lápiz está arriba cuando el usuario completa un trazo y eleva el lápiz del digitalizador. Un botón de un cilindro está en marcha cuando no se presiona el botón.

Cuando suelte el botón derecho del mouse, recibirá dos eventos **CursorButtonUp:** uno para el botón derecho hacia arriba y otro para el botón izquierdo hacia arriba.

Este método de evento se define en las interfaces de solo distribución \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICECursorButtonUp.

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

[**Evento CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton (Interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




