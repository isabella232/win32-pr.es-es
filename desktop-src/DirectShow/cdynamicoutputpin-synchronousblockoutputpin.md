---
description: El método SynchronousBlockOutputPin bloquea el PIN; no devuelve ningún resultado hasta que se bloquea el PIN.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Método CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671688"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a>CDynamicOutputPin. SynchronousBlockOutputPin, método

El `SynchronousBlockOutputPin` método bloquea el PIN; no vuelve hasta que no se bloquea el PIN.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                    | Descripción                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                           | Correcto.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ PIN \_ ya \_ bloqueados**</dt> </dl>                   | El PIN ya está bloqueado en otro subproceso.<br/>     |
| <dl> <dt>**\_ \_ el PIN VFW \_ ya está \_ bloqueado \_ en \_ este \_ subproceso**</dt> </dl> | El PIN ya está bloqueado en el subproceso que realiza la llamada.<br/> |



 

## <a name="remarks"></a>Observaciones

No llame a este método desde el subproceso de streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




