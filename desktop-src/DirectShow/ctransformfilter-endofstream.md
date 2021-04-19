---
description: El método EndOfStream notifica al filtro que no se esperan datos adicionales del PIN de entrada.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Método CTransformFilter. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660431"
---
# <a name="ctransformfilterendofstream-method"></a>CTransformFilter. EndOfStream, método

El `EndOfStream` método notifica al filtro que no se esperan datos adicionales del PIN de entrada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT** .

## <a name="remarks"></a>Observaciones

El método [**CTransformInputPin:: EndOfStream**](ctransforminputpin-endofstream.md) del PIN de entrada llama a este método. Este método entrega la notificación de final de secuencia de nivel inferior. Si la clase derivada utiliza un subproceso de trabajo para proporcionar ejemplos de medios, debe invalidar este método y poner en cola la notificación de final de secuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




