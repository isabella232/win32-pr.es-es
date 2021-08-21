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
ms.openlocfilehash: 89b87bd4e706e5270b49ca94d1c86a6c5a5326fd3efccb1dcc45b9681e6e2fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017563"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Destructor CBaseAllocator.~CBaseAllocator

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Comentarios

Llame siempre al [**método CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir el objeto. El destructor de clase base no puede llamar **a Decommit**, porque ese método llama al método virtual [**puro CBaseAllocator::Free**](cbaseallocator-free.md). Las clases derivadas deben invalidar este destructor y llamar **a Decommit**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




