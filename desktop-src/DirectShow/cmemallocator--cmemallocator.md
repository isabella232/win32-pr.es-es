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
# <a name="cmemallocatorcmemallocator-destructor"></a><span data-ttu-id="dbcf2-103">CMemAllocator. ~ CMemAllocator (destructor)</span><span class="sxs-lookup"><span data-stu-id="dbcf2-103">CMemAllocator.~CMemAllocator destructor</span></span>

<span data-ttu-id="dbcf2-104">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="dbcf2-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcf2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbcf2-105">Syntax</span></span>


```C++
~CMemAllocator();
```



## <a name="remarks"></a><span data-ttu-id="dbcf2-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbcf2-106">Remarks</span></span>

<span data-ttu-id="dbcf2-107">Este método invalida el destructor de clase base para llamar a [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) y [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf2-107">This method overrides the base-class destructor to call [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) and [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbcf2-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbcf2-108">Requirements</span></span>



| <span data-ttu-id="dbcf2-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbcf2-109">Requirement</span></span> | <span data-ttu-id="dbcf2-110">Value</span><span class="sxs-lookup"><span data-stu-id="dbcf2-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbcf2-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbcf2-111">Header</span></span><br/>  | <dl> <span data-ttu-id="dbcf2-112"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbcf2-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dbcf2-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbcf2-113">Library</span></span><br/> | <dl> <span data-ttu-id="dbcf2-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dbcf2-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbcf2-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbcf2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbcf2-116">**Clase CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="dbcf2-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




