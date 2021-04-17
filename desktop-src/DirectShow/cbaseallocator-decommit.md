---
description: El método de anulación de confirmación anula el asignador. Este método implementa el método IMemAllocator::D ecommit.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Método CBaseAllocator. decommit (Amfilter. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660619"
---
# <a name="cbaseallocatordecommit-method"></a>CBaseAllocator. decommit (método)

El `Decommit` método anula la confirmación del asignador. Este método implementa el método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Después de llamar a este método, se producirá un error en las llamadas al método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) . A medida que se publican los ejemplos, se devuelven a la lista de disponibilidad. Cuando se devuelve la última muestra, el asignador llama al método [**CBaseAllocator:: Free**](cbaseallocator-free.md) , que libera la memoria asignada. (En la clase base, **Free** es un método virtual puro).

Además, este método libera todos los subprocesos que están bloqueados en llamadas a **getBuffer** . Se produce un error en las llamadas a **getBuffer** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




