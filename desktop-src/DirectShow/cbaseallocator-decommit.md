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
ms.openlocfilehash: 614986a912f08d918d4fbbaf6b3eeeb0d3b2c3eabc47748351934a08b8280cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017553"
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

## <a name="remarks"></a>Comentarios

Después de llamar a este método, se producirá un error en las llamadas al método [**CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md) A medida que se liberan los ejemplos, se devuelven a la lista gratuita. Cuando se devuelve el último ejemplo, el asignador llama al método [**CBaseAllocator::Free,**](cbaseallocator-free.md) que libera la memoria asignada. (En la clase base, **Free es** un método virtual puro).

Además, este método libera todos los subprocesos que están bloqueados en **las llamadas a GetBuffer.** Se producirá un error **en las llamadas a GetBuffer.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




