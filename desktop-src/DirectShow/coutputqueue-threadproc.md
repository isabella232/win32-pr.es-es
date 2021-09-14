---
description: El método ThreadProc recupera ejemplos de la cola y los entrega al pin de entrada.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Método COutputQueue.ThreadProc (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062430"
---
# <a name="coutputqueuethreadproc-method"></a>Método COutputQueue.ThreadProc

El `ThreadProc` método recupera ejemplos de la cola y los entrega al pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Observaciones

El [**método COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) llama a este método, que implementa el bucle de subproceso principal. Dentro del bucle , el método realiza los pasos siguientes:

1.  Recupera un ejemplo para la cola.
2.  Si el ejemplo es un mensaje de control, el subproceso ejecuta la acción de control. De lo contrario, coloca el ejemplo en la [**matriz COutputQueue::m \_ ppSamples.**](coutputqueue-m-ppsamples.md)
3.  Cuando la matriz está llena (o si [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) es **FALSE),** el subproceso llama al método [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) para entregar los ejemplos.
4.  Si no hay ejemplos en cola, el subproceso espera en el semáforo [**COutputQueue::m \_ hSem.**](coutputqueue-m-hsem.md)

El subproceso finaliza cuando la variable miembro [**COutputQueue::m \_ bTerminate**](coutputqueue-m-bterminate.md) se convierte en **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




