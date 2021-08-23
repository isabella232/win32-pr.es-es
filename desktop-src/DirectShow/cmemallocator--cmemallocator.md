---
description: 'Destructor CMemAllocator.~CMemAllocator: método Destructor.'
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Destructor CMemAllocator.~CMemAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588b370fc56f6af547ead19c7a52758a3851dd7e46d88b90f8f621ed6002d6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954384"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Destructor CMemAllocator.~CMemAllocator

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Comentarios

Este método invalida el destructor de clase base para llamar a [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) y [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




