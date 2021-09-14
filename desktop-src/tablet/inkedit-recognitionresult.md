---
description: Se produce cuando el control InkEdit obtiene los resultados manualmente de una llamada al método InkEdit::Recognize o automáticamente después de que se activa el tiempo de espera de reconocimiento.
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Evento InkEdit.RecognitionResult (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256683"
---
# <a name="inkeditrecognitionresult-event"></a>Evento InkEdit.RecognitionResult

Se produce cuando el control [InkEdit](inkedit-control-reference.md) obtiene los resultados manualmente de una llamada al método [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o automáticamente después de que se activa el tiempo de espera de reconocimiento.

## <a name="syntax"></a>Sintaxis


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RecognitionResult* \[ En\]
</dt> <dd>

Objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) que contiene el resultado del reconocimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Este método de evento se define en la **\_ interfaz IInkEditEvents.** La **\_ interfaz IInkEditEvents** implementa la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificador de DISPID \_ IeeRecognitionResult.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Inked.h (también requiere \_ i.c con entrada manuscrita)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Método Recognize \[ InkEdit (control)\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

