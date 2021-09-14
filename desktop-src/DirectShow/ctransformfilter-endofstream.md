---
description: El método EndOfStream notifica al filtro que no se espera ningún dato adicional del pin de entrada.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Método CTransformFilter.EndOfStream (Transfrm.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973836"
---
# <a name="ctransformfilterendofstream-method"></a>Método CTransformFilter.EndOfStream

El método notifica al filtro que no se espera ningún `EndOfStream` dato adicional del pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Observaciones

El método [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) del pin de entrada llama a este método. Este método entrega la notificación de fin de flujo de bajada. Si la clase derivada usa un subproceso de trabajo para entregar ejemplos multimedia, debe invalidar este método y poner en cola la notificación de fin de flujo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




