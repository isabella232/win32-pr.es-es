---
description: El método NotifySample libera todos los subprocesos que están esperando ejemplos.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Método CBaseAllocator.NotifySample (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070136"
---
# <a name="cbaseallocatornotifysample-method"></a>Método CBaseAllocator.NotifySample

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

Cuando hay subprocesos que esperan ejemplos, el valor de [**CBaseAllocator::m \_ lWaiting**](cbaseallocator-m-lwaiting.md) es mayor que cero. Si *m \_ lWaiting* es mayor que cero, este método llama a la función **ReleaseSemaphore** en el semáforo [**CBaseAllocator::m \_ hSem,**](cbaseallocator-m-hsem.md) activando los subprocesos en espera. También restablece *m \_ lWaiting* a cero.

Se llama a este método desde el método [**CBaseAllocator::ReleaseBuffer,**](cbaseallocator-releasebuffer.md) cuando se devuelve un ejemplo a la lista libre; y desde [**el método CBaseAllocator::D ecommit,**](cbaseallocator-decommit.md) cuando se desasigna el asignador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




