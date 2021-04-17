---
description: Marca que indica si hay una operación de desconfirmación en curso.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Miembro CBaseAllocator:: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670629"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a><span data-ttu-id="d3324-103">Miembro bDecommitInProgress CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="d3324-103">CBaseAllocator::m\_bDecommitInProgress member</span></span>

<span data-ttu-id="d3324-104">Marca que indica si hay una operación de desconfirmación en curso.</span><span class="sxs-lookup"><span data-stu-id="d3324-104">Flag indicating whether a decommit operation is in progress.</span></span> <span data-ttu-id="d3324-105">El valor es **true** una vez que se llama al método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , pero antes de que se liberen todos los búferes.</span><span class="sxs-lookup"><span data-stu-id="d3324-105">The value is **TRUE** after the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method is called, but before all the buffers have been released.</span></span> <span data-ttu-id="d3324-106">Si el valor es **true**, se produce un error en el método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d3324-106">If the value is **TRUE**, the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method fails.</span></span> <span data-ttu-id="d3324-107">Además, el asignador no debe eliminarse a sí mismo mientras que el valor es **true**.</span><span class="sxs-lookup"><span data-stu-id="d3324-107">Also, the allocator should not deleted itself while the value is **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3324-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3324-108">Syntax</span></span>


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a><span data-ttu-id="d3324-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3324-109">Requirements</span></span>



| <span data-ttu-id="d3324-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3324-110">Requirement</span></span> | <span data-ttu-id="d3324-111">Value</span><span class="sxs-lookup"><span data-stu-id="d3324-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3324-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3324-112">Header</span></span><br/>  | <dl> <span data-ttu-id="d3324-113"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3324-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d3324-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3324-114">Library</span></span><br/> | <dl> <span data-ttu-id="d3324-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d3324-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3324-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3324-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3324-117">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="d3324-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




