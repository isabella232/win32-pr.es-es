---
description: El método StartUsingOutputPin obtiene acceso al pin para una operación de streaming.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Método CDynamicOutputPin.StartUsingOutputPin (Amfilter.h)
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
ms.openlocfilehash: 4438c6670b0535711c453e64496ffd4b21263acab728e090024f9e1e01427969
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749455"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a>Método CDynamicOutputPin.StartUsingOutputPin

El `StartUsingOutputPin` método obtiene acceso al pin para una operación de streaming.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                                               |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>          | error inesperado.<br/>                                      |
| <dl> <dt>**CAMBIO DEL \_ ESTADO DE VFW E \_ \_**</dt> </dl> | El filtro se detuvo o el pin ha empezado a vaciarse.<br/> |



 

## <a name="remarks"></a>Comentarios

Llame a este método antes de llamar a cualquier método que entregue datos al pin de entrada conectado o que cambie el tipo de medio de la conexión. Por ejemplo, esta regla se aplica a los métodos siguientes:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Después, llame al [**método CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) para liberar el acceso al pin.

Si el pin está bloqueado, `StartUsingOutputPin` espera a que se desbloquee. Si el filtro se detiene mientras el método está esperando, el método devuelve inmediatamente VFW \_ E \_ STATE \_ CHANGED. El pin mantiene un recuento de cuántas veces se ha llamado sin una llamada correspondiente `StartUsingOutputPin` a **StopUsingOutputPin**. Si otro subproceso intenta bloquear el pin mientras este recuento es distinto de cero, el pin establece su estado de bloqueo en "pending". El pin se bloquea una vez completadas todas las operaciones de streaming, en la llamada final a **StopUsingOutputPin**.

No mantenga la sección [**crítica CDynamicOutputPin::m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) cuando llame a este método. De lo contrario, si el pin está bloqueado, nunca se podrá desbloquear, lo que provocará un interbloqueo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




