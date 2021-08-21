---
description: Se produce cuando se agregan uno o varios objetos IInkStrokeDisp a la colección InkStrokes.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: Evento InkPicture.StrokesAdded (Ms inkut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5f9418289ac996b2c2248c2cf1696e7d45b4548dbafa4dff9494e76cbedc30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717408"
---
# <a name="inkpicturestrokesadded-event"></a>Evento InkPicture.StrokesAdded

Se produce cuando se agregan uno o [**varios objetos IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) a la [colección InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

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

Este método de evento se define en la **\_ interfaz IInkStrokesEvents.** La **\_ interfaz IInkStrokesEvents** implementa la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de \_ DISPID SEStrokesAdded.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

