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
# <a name="cbaseallocatorcbaseallocator-destructor"></a><span data-ttu-id="5fe3d-103">Destructor CBaseAllocator.~CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="5fe3d-103">CBaseAllocator.~CBaseAllocator destructor</span></span>

<span data-ttu-id="5fe3d-104">Método destructor.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fe3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fe3d-105">Syntax</span></span>


```C++
~CBaseAllocator();
```



## <a name="remarks"></a><span data-ttu-id="5fe3d-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5fe3d-106">Remarks</span></span>

<span data-ttu-id="5fe3d-107">Llame siempre al [**método CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) antes de destruir el objeto.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-107">Always call the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method before destroying the object.</span></span> <span data-ttu-id="5fe3d-108">El destructor de clase base no puede llamar **a Decommit**, porque ese método llama al método virtual puro [**CBaseAllocator::Free**](cbaseallocator-free.md).</span><span class="sxs-lookup"><span data-stu-id="5fe3d-108">The base-class destructor cannot call **Decommit**, because that method calls the pure virtual method [**CBaseAllocator::Free**](cbaseallocator-free.md).</span></span> <span data-ttu-id="5fe3d-109">Las clases derivadas deben invalidar este destructor y llamar **a Decommit**.</span><span class="sxs-lookup"><span data-stu-id="5fe3d-109">Derived classes should override this destructor and call **Decommit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fe3d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fe3d-110">Requirements</span></span>



| <span data-ttu-id="5fe3d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fe3d-111">Requirement</span></span> | <span data-ttu-id="5fe3d-112">Value</span><span class="sxs-lookup"><span data-stu-id="5fe3d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fe3d-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fe3d-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5fe3d-114"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fe3d-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5fe3d-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fe3d-115">Library</span></span><br/> | <dl> <span data-ttu-id="5fe3d-116"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5fe3d-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fe3d-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5fe3d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fe3d-118">**CBaseAllocator (clase)**</span><span class="sxs-lookup"><span data-stu-id="5fe3d-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




