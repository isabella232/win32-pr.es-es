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
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062432"
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

## <a name="remarks"></a>Observaciones

Si la variable miembro [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) es **TRUE,** el objeto rellena la matriz [**COutputQueue::m \_ ppSamples**](coutputqueue-m-ppsamples.md) antes de entregar un lote de ejemplos. Llame a este método para entregar un lote parcial. Por ejemplo, el [**método COutputQueue::EOS**](coutputqueue-eos.md) llama a para serializar los `SendAnyway` mensajes de fin de secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




