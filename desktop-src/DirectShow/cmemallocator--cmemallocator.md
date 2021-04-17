---
description: Método de destructor.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: CMemAllocator. ~ CMemAllocator (Amfilter. h)
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670759"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>CMemAllocator. ~ CMemAllocator (destructor)

Método de destructor.

## <a name="syntax"></a>Sintaxis


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Observaciones

Este método invalida el destructor de clase base para llamar a [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) y [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




