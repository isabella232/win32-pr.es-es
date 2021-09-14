---
description: Matriz de ejemplos de tamaño COutputQueue::m \_ lBatchSize.
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: Miembro COutputQueue::m_ppSamples (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062449"
---
# <a name="coutputqueuem_ppsamples-member"></a>Miembro COutputQueue::m \_ ppSamples

Matriz de ejemplos de tamaño [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Sintaxis


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Observaciones

El subproceso de trabajo extrae ejemplos de la cola y los coloca en esta matriz. Pasa la matriz al [**método IMemInputPin::ReceiveMultiple.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) Si el objeto no usa un subproceso de trabajo, el objeto coloca ejemplos directamente en esta matriz. La variable [**miembro COutputQueue::m \_ List**](coutputqueue-m-list.md) contiene la cola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




