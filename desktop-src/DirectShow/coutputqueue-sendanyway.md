---
description: El método SendAnyway entrega cualquier ejemplo pendiente.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Método COutputQueue. SendAnyway (Outputq. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678972"
---
# <a name="coutputqueuesendanyway-method"></a>COutputQueue. SendAnyway, método

El `SendAnyway` método entrega cualquier ejemplo pendiente.

## <a name="syntax"></a>Sintaxis


```C++
void SendAnyway();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la variable miembro [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) es **true**, el objeto rellena la matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) antes de entregar un lote de muestras. Llame a este método para proporcionar un lote parcial. Por ejemplo, el método [**COutputQueue:: EOS**](coutputqueue-eos.md) llama `SendAnyway` a para serializar los mensajes de fin de secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




