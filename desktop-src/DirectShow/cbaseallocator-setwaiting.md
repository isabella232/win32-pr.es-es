---
description: El método SetWaiting incrementa el número de subprocesos en espera.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Método CBaseAllocator. SetWaiting (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661125"
---
# <a name="cbaseallocatorsetwaiting-method"></a>CBaseAllocator. SetWaiting, método

El `SetWaiting` método incrementa el recuento de subprocesos en espera.

## <a name="syntax"></a>Sintaxis


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método incrementa la variable miembro [**CBaseAllocator:: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) . Si un subproceso está bloqueado en el método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) , el asignador llama a `SetWaiting` y, a continuación, espera a que se Señalice el semáforo [**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md) . El método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) señala el semáforo y establece *m \_ lWaiting* en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




