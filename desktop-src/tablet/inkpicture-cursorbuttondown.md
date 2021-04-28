---
description: 'Evento InkPicture.CursorButtonDown: se produce cuando la clase InkCollector detecta un botón de cursor que está apagado.'
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: Evento InkPicture.CursorButtonDown (Msyecciónut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2017cd7dc2291bdb29aa01df3d94f20211b7cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116783"
---
# <a name="inkpicturecursorbuttondown-event"></a>Evento InkPicture.CursorButtonDown

Se produce cuando [**la clase InkCollector**](inkcollector-class.md) detecta un botón de cursor que está apagado.

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

Un botón de una punta de lápiz está abajo cuando el usuario baja el lápiz al digitalizador y comienza a realizar el seguimiento de un trazo. Un botón de un cilindro está apagado cuando se presiona el botón.

Al presionar el botón derecho del mouse, se reciben dos eventos **CursorButtonDown:** uno para el botón derecho presionado y otro para el botón izquierdo presionado.

Este método de evento se define en **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** interfaz de solo distribución (dispinterfaces) con un identificador DE DISPID \_ ICECursorButtonDown.

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

[**Evento CursorDown**](inkpicture-cursordown.md)
</dt> <dt>

[**Evento CursorButtonUp**](inkpicture-cursorbuttonup.md)
</dt> <dt>

[**IInkCursor (interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkCursorButton (Interfaz)**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




