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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246801"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Destructor CMemAllocator.~CMemAllocator

Método destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Observaciones

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

 

 




