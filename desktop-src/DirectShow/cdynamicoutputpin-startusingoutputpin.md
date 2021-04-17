---
description: El método StartUsingOutputPin obtiene acceso al pin para una operación de streaming.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Método CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661201"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>CDynamicOutputPin. StartUsingOutputPin, método

El `StartUsingOutputPin` método obtiene acceso al pin para una operación de streaming.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                                               |
| <dl> <dt>**E \_ inesperado**</dt> </dl>          | error inesperado.<br/>                                      |
| <dl> <dt>**Estado de VFW \_ E \_ \_ cambiado**</dt> </dl> | Se detuvo el filtro o el PIN comenzó a vaciarse.<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método antes de llamar a cualquier método que entregue datos a la clavija de entrada conectada o que cambie el tipo de medio de la conexión. Por ejemplo, esta regla se aplica a los siguientes métodos:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Después, llame al método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) para liberar el acceso al código PIN.

Si el PIN está bloqueado, `StartUsingOutputPin` espera a que el PIN se desbloquee. Si el filtro se detiene mientras el método está esperando, el método devuelve inmediatamente \_ el \_ Estado VFW E \_ cambiado. El PIN mantiene un recuento del número de veces que se ha `StartUsingOutputPin` llamado sin una llamada correspondiente a **StopUsingOutputPin**. Si otro subproceso intenta bloquear el PIN mientras este recuento es distinto de cero, el PIN establece su estado de bloqueo en "pendiente". El PIN se bloquea una vez completadas todas las operaciones de streaming, en la llamada final a **StopUsingOutputPin**.

No conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) cuando llame a este método. De lo contrario, si el PIN está bloqueado, nunca se puede desbloquear, lo que produce un interbloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




