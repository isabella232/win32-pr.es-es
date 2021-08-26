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
ms.openlocfilehash: 674528b6da53b7835e437afac9a0564f91785b2f9a13f132e87a6763b80881c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057465"
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

## <a name="remarks"></a>Comentarios

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

 

 




