---
description: 'Destructor CBaseAllocator.~CBaseAllocator: método Destructor.'
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Destructor CBaseAllocator.~CBaseAllocator (Amfilter.h)
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
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096423"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Destructor CBaseAllocator.~CBaseAllocator

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Comentarios

Llame siempre al [**método CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir el objeto. El destructor de clase base no puede llamar **a Decommit**, porque ese método llama al método virtual puro [**CBaseAllocator::Free**](cbaseallocator-free.md). Las clases derivadas deben invalidar este destructor y llamar **a Decommit**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




