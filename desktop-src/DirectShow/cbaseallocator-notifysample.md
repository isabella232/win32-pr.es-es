---
description: El método NotifySample libera todos los subprocesos que están esperando ejemplos.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Método CBaseAllocator. NotifySample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671475"
---
# <a name="cbaseallocatornotifysample-method"></a>CBaseAllocator. NotifySample, método

El `NotifySample` método libera todos los subprocesos que están esperando ejemplos.

## <a name="syntax"></a>Sintaxis


```C++
void NotifySample();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando hay subprocesos en espera de ejemplos, el valor de [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) es mayor que cero. Si *m \_ lWaiting* es mayor que cero, este método llama a la función **ReleaseSemaphore (** en el semáforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) , activando los subprocesos en espera. También restablece *m \_ lWaiting* en cero.

Se llama a este método desde el método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , cuando se devuelve un ejemplo a la lista libre. y del método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , cuando se desconfirma el asignador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




