---
description: Se produce cuando se agregan uno o varios trazos a la colección InkStrokes.
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: Evento InkStrokes.StrokesAdded (Msgulaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d2491f643e67c09ac34079412bb9676655713bbfd7ec836d8df7f92799a12a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041885"
---
# <a name="inkstrokesstrokesadded-event"></a>Evento InkStrokes.StrokesAdded

Se produce cuando se agregan uno o varios trazos a la [colección InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

## <a name="syntax"></a>Sintaxis


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StrokeIds* \[ En\]
</dt> <dd>

Matriz de enteros de identificadores para cada [**objeto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) agregado cuando se produce este evento.

Para obtener más información sobre la estructura VARIANT, vea [Usar la biblioteca COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este método de evento se define en la \_ interfaz IInkEvents. La \_ interfaz IInkEvents implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ SEStrokesAdded.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Agregar colección \[ InkStrokes de método\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)
</dt> <dt>

[**InkDisp (clase)**](inkdisp-class.md)
</dt> </dl>

 

