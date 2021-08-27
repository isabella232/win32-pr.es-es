---
description: Matriz de ejemplos de tamaño COutputQueue::m \_ lBatchSize.
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: COutputQueue::m_ppSamples miembro (Outputq.h)
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
ms.openlocfilehash: d0b27a356727fc317eb1818ecd548d944e3c4b2ace9cc11e0834bf1cf551c9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103155"
---
# <a name="coutputqueuem_ppsamples-member"></a>Miembro COutputQueue::m \_ ppSamples

Matriz de ejemplos de tamaño [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Sintaxis


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Comentarios

El subproceso de trabajo extrae ejemplos de la cola y los coloca en esta matriz. Pasa la matriz al [**método IMemInputPin::ReceiveMultiple.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) Si el objeto no usa un subproceso de trabajo, el objeto coloca ejemplos directamente en esta matriz. La variable [**miembro COutputQueue::m \_ List**](coutputqueue-m-list.md) contiene la cola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




