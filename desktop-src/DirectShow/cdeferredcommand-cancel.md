---
description: 'El método CANCEL cancela una solicitud CDeferredCommand:: Invoke previamente en cola.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Método CDeferredCommand. Cancel (Ctlutil. h)
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
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661299"
---
# <a name="cdeferredcommandcancel-method"></a>CDeferredCommand. Cancel (método)

El `Cancel` método cancela una solicitud [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) previamente en cola.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve VFW \_ E \_ ya \_ cancelado si **m \_ pQueue** es **null**. Devuelve un **valor HRESULT** de [**CCmdQueue:: Remove**](ccmdqueue-remove.md) si la llamada genera un error. Devuelve S \_ correcto si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IDeferredCommand:: CANCEL**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




