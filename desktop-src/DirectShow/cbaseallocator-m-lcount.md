---
description: Número de búferes que se van a proporcionar.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Miembro CBaseAllocator:: m_lCount (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660878"
---
# <a name="cbaseallocatorm_lcount-member"></a><span data-ttu-id="f6e6b-103">Miembro lCount CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="f6e6b-103">CBaseAllocator::m\_lCount member</span></span>

<span data-ttu-id="f6e6b-104">Número de búferes que se van a proporcionar.</span><span class="sxs-lookup"><span data-stu-id="f6e6b-104">Number of buffers to provide.</span></span> <span data-ttu-id="f6e6b-105">El método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) establece este valor.</span><span class="sxs-lookup"><span data-stu-id="f6e6b-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets this value.</span></span> <span data-ttu-id="f6e6b-106">Los búferes no se asignan hasta que se llama al método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="f6e6b-106">The buffers are not allocated until the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method is called.</span></span> <span data-ttu-id="f6e6b-107">La variable miembro [**CBaseAllocator:: m \_ lAllocated**](cbaseallocator-m-lallocated.md) especifica el número actual de búferes asignados.</span><span class="sxs-lookup"><span data-stu-id="f6e6b-107">The current number of allocated buffers is specified by the [**CBaseAllocator::m\_lAllocated**](cbaseallocator-m-lallocated.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e6b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6e6b-108">Syntax</span></span>


```C++
long m_lCount;
```



## <a name="requirements"></a><span data-ttu-id="f6e6b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6e6b-109">Requirements</span></span>



| <span data-ttu-id="f6e6b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6e6b-110">Requirement</span></span> | <span data-ttu-id="f6e6b-111">Value</span><span class="sxs-lookup"><span data-stu-id="f6e6b-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e6b-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6e6b-112">Header</span></span><br/>  | <dl> <span data-ttu-id="f6e6b-113"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6e6b-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f6e6b-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6e6b-114">Library</span></span><br/> | <dl> <span data-ttu-id="f6e6b-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f6e6b-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6e6b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6e6b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e6b-117">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="f6e6b-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




