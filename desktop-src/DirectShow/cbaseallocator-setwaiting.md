---
description: El método SetWaiting incrementa el recuento de subprocesos en espera.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Método CBaseAllocator.SetWaiting (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070133"
---
# <a name="cbaseallocatorsetwaiting-method"></a>CBaseAllocator.SetWaiting (método)

El `SetWaiting` método incrementa el número de subprocesos en espera.

## <a name="syntax"></a>Sintaxis


```C++
void SetWaiting();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método incrementa la variable [**miembro CBaseAllocator::m \_ lWaiting.**](cbaseallocator-m-lwaiting.md) Si un subproceso está bloqueado en el método [**CBaseAllocator::GetBuffer,**](cbaseallocator-getbuffer.md) el asignador llama a y espera a que se señale el `SetWaiting` semáforo de [**CBaseAllocator::m \_ hSem.**](cbaseallocator-m-hsem.md) El [**método CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) señala el semáforo y establece *m \_ lWaiting* de nuevo en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




