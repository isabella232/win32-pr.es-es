---
description: El método EndFlush finaliza una operación de vaciado.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Método COutputQueue. EndFlush (Outputq. h)
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
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671215"
---
# <a name="coutputqueueendflush-method"></a>COutputQueue. EndFlush, método

El `EndFlush` método finaliza una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
void EndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el objeto utiliza un subproceso, este método espera el evento [**COutputQueue:: m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) . El subproceso señala este evento después de liberar cualquier ejemplo pendiente. Si el objeto no utiliza un subproceso, este método llama al método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) . Después, el `EndFlush` método llama al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el PIN de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




