---
description: 'Evento InkOverlay.CursorButtonUp: se produce cuando InkCollector detecta un botón de cursor que está encendido.'
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Evento InkOverlay.CursorButtonUp (Ms cursorut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e94fb9c1727e0c8fce13f3696397462fdf590c076627df869dcafd177190c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220855"
---
# <a name="inkoverlaycursorbuttonup-event"></a>Evento InkOverlay.CursorButtonUp

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

Objeto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que generó el [**evento CursorButtonUp.**](inkcollector-cursorbuttonup.md)

</dd> <dt>

*Botón* \[ En\]
</dt> <dd>

Botón que se ha liberado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Un botón de una punta de lápiz está arriba cuando el usuario completa un trazo y eleva el lápiz del digitalizador. Un botón de un cilindro está en marcha cuando no se presiona el botón.

Cuando suelte el botón derecho del mouse, recibirá dos eventos [**CursorButtonUp:**](inkcollector-cursorbuttonup.md) uno para el botón derecho hacia arriba y otro para el botón izquierdo hacia arriba.

Este método de evento se define en las interfaces de solo envío \_ \_ (dispinterfaces) de IInkCollectorEvents, IInkOverlayEvents e IInkPictureEvents con un identificador \_ DE DISPID \_ ICECursorButtonUp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InkOverlay (clase)**](inkoverlay-class.md)
</dt> <dt>

[**Evento CursorButtonDown**](inkcollector-cursorbuttondown.md)
</dt> <dt>

[**Evento CursorDown**](inkcollector-cursordown.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




