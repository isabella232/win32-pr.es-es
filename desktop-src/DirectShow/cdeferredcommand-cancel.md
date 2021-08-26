---
description: El método Cancel cancela una solicitud CDeferredCommand::Invoke previamente en cola.
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Método CDeferredCommand.Cancel (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa7e957fe97e06c6fb14fe3a9048048e351ac1baf4ff8f4dae25b3cf5863776e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043715"
---
# <a name="cdeferredcommandcancel-method"></a>Método CDeferredCommand.Cancel

El `Cancel` método cancela una solicitud [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) previamente en cola.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E \_ ALREADY \_ CANCELLED si m **\_ pQueue** es **NULL.** Devuelve un **valor HRESULT** de [**CCmdQueue::Remove**](ccmdqueue-remove.md) si la llamada genera un error. Devuelve S \_ OK si se realiza correctamente.

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IDeferredCommand::Cancel.**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDeferredCommand (clase)**](cdeferredcommand.md)
</dt> </dl>

 

 




