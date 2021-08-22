---
description: El método FreeSamples libera todos los ejemplos pendientes.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Método COutputQueue.FreeSamples (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2cc87047d6dc48494fc225b5a0b4c4ad7bcb69f0f7341580f8c48c1440470bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954164"
---
# <a name="coutputqueuefreesamples-method"></a>Método COutputQueue.FreeSamples

El `FreeSamples` método libera todos los ejemplos pendientes.

## <a name="syntax"></a>Sintaxis


```C++
void FreeSamples();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método quita los ejemplos pendientes de la cola y de la matriz de ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




