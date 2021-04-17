---
description: Método de destructor.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator. ~ CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660117"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>CBaseAllocator. ~ CBaseAllocator (destructor)

Método de destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Observaciones

Llame siempre al método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir el objeto. El destructor de clase base no puede llamar a **commit**, porque ese método llama al método virtual puro [**CBaseAllocator:: Free**](cbaseallocator-free.md). Las clases derivadas deben invalidar este destructor y llamar a **commit**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




