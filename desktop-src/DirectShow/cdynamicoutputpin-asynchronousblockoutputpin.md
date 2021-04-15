---
description: El método AsynchronousBlockOutputPin bloquea el código PIN. El método puede devolver antes de que se bloquee el PIN.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Método CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661362"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>CDynamicOutputPin. AsynchronousBlockOutputPin, método

El `AsynchronousBlockOutputPin` método bloquea el código PIN. El método puede devolver antes de que se bloquee el PIN.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hNotifyCallerPinBlockedEvent* 
</dt> <dd>

Identificador para un evento. El evento se señala cuando el PIN de salida está bloqueado o si el autor de la llamada cancela la operación de bloqueo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                    | Descripción                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                                           | Correcto.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ PIN \_ ya \_ bloqueados**</dt> </dl>                   | El PIN ya está bloqueado en otro subproceso.<br/>     |
| <dl> <dt>**\_ \_ el PIN VFW \_ ya está \_ bloqueado \_ en \_ este \_ subproceso**</dt> </dl> | El PIN ya está bloqueado en el subproceso que realiza la llamada.<br/> |



 

## <a name="remarks"></a>Observaciones

No llame a este método desde el subproceso de streaming.

Si no hay ningún subproceso de transmisión por secuencias que esté usando el PIN, este método bloqueará inmediatamente el código PIN. De lo contrario, establece el estado del PIN en "pendiente" y devuelve. Cuando se completa la operación de streaming, el subproceso de streaming llama al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , que bloquea el PIN e indica el evento **hNotifyCallerPinBlockedEvent** . Para cancelar un bloque pendiente, llame al método [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




