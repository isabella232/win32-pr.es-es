---
description: 'Método COutputQueue.EndFlush: el método EndFlush finaliza una operación de vaciado.'
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Método COutputQueue.EndFlush (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099013"
---
# <a name="coutputqueueendflush-method"></a>Método COutputQueue.EndFlush

El `EndFlush` método finaliza una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
void EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si el objeto usa un subproceso, este método espera el evento [**COutputQueue::m \_ evFlushComplete.**](coutputqueue-m-evflushcomplete.md) El subproceso señala este evento después de liberar los ejemplos pendientes. Si el objeto no usa un subproceso, este método llama al [**método COutputQueue::FreeSamples.**](coutputqueue-freesamples.md) A `EndFlush` continuación, el método [**llama al método IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el pin de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




