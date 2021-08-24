---
description: El método SendAnyway entrega los ejemplos pendientes.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Método COutputQueue.SendAnyway (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4aed3cdd37c50f20b48922c8c711266a111680506813ab4572800abbca971343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831765"
---
# <a name="coutputqueuesendanyway-method"></a>Método COutputQueue.SendAnyway

El `SendAnyway` método entrega los ejemplos pendientes.

## <a name="syntax"></a>Sintaxis


```C++
void SendAnyway();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la variable miembro [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) es **TRUE,** el objeto rellena la matriz [**COutputQueue::m \_ ppSamples**](coutputqueue-m-ppsamples.md) antes de entregar un lote de ejemplos. Llame a este método para entregar un lote parcial. Por ejemplo, el [**método COutputQueue::EOS**](coutputqueue-eos.md) llama a para serializar los `SendAnyway` mensajes de fin de secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




