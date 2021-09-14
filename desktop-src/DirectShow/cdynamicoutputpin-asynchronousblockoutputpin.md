---
description: El método AsynchronousBlockOutputPin bloquea el pin. El método puede devolver antes de que se bloquee el pin.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Método CDynamicOutputPin.AsynchronousBlockOutputPin (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061264"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>Método CDynamicOutputPin.AsynchronousBlockOutputPin

El `AsynchronousBlockOutputPin` método bloquea el pin. El método puede devolver antes de que se bloquee el pin.

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

Identificador para un evento. El evento se señala cuando se bloquea el pin de salida o si el autor de la llamada cancela la operación de bloqueo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                    | Descripción                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Correcto.<br/>                                      |
| <dl> <dt>**EL PIN \_ DE VFW E \_ YA \_ ESTÁ \_ BLOQUEADO**</dt> </dl>                   | El pin ya está bloqueado en otro subproceso.<br/>     |
| <dl> <dt>**EL PIN \_ DE VFW E \_ YA ESTÁ BLOQUEADO EN ESTE \_ \_ \_ \_ \_ SUBPROCESO**</dt> </dl> | El pin ya está bloqueado en el subproceso que realiza la llamada.<br/> |



 

## <a name="remarks"></a>Observaciones

No llame a este método desde el subproceso de streaming.

Si ningún subproceso de streaming usa el pin, este método bloquea inmediatamente el pin. De lo contrario, establece el estado de la marca en "pendiente" y devuelve . Cuando se completa la operación de streaming, el subproceso de streaming llama al método [**CDynamicOutputPin::StopUsingOutputPin,**](cdynamicoutputpin-stopusingoutputpin.md) que bloquea el pin y señala el evento **hNotifyCallerPinBlockedEvent.** Para cancelar un bloque pendiente, llame al [**método CDynamicOutputPin::UnblockOutputPin.**](cdynamicoutputpin-unblockoutputpin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




