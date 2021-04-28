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
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095413"
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
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




