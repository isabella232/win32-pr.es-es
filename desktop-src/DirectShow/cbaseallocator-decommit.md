---
description: El método Decommit desasigna el asignador. Este método implementa el método IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Método CBaseAllocator.Decommit (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172017"
---
# <a name="cbaseallocatordecommit-method"></a>CBaseAllocator.Decommit (método)

El `Decommit` método desasigna el asignador. Este método implementa el [**método IMemAllocator::D ecommit.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Después de llamar a este método, se producirá un error en las llamadas al método [**CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md) A medida que se liberan los ejemplos, se devuelven a la lista gratuita. Cuando se devuelve el último ejemplo, el asignador llama al método [**CBaseAllocator::Free,**](cbaseallocator-free.md) que libera la memoria asignada. (En la clase base, **Free es** un método virtual puro).

Además, este método libera los subprocesos que están bloqueados en **las llamadas a GetBuffer.** Se producirá un error **en las llamadas a GetBuffer.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




