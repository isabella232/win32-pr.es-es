---
description: 'Marca que indica si la devolución de llamada de versión está habilitada. Esta marca se establece en el método de constructor. Si el valor es FALSE, al llamar al método CBaseAllocator:: SetNotify, se desencadena una aserción (en las compilaciones de depuración).'
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Miembro CBaseAllocator:: m_fEnableReleaseCallback (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671749"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a><span data-ttu-id="5a06e-105">Miembro fEnableReleaseCallback CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="5a06e-105">CBaseAllocator::m\_fEnableReleaseCallback member</span></span>

<span data-ttu-id="5a06e-106">Marca que indica si la devolución de llamada de versión está habilitada.</span><span class="sxs-lookup"><span data-stu-id="5a06e-106">Flag indicating whether the release callback is enabled.</span></span> <span data-ttu-id="5a06e-107">Esta marca se establece en el método de constructor.</span><span class="sxs-lookup"><span data-stu-id="5a06e-107">This flag is set in the constructor method.</span></span> <span data-ttu-id="5a06e-108">Si el valor es **false**, al llamar al método [**CBaseAllocator:: SetNotify**](cbaseallocator-setnotify.md) , se desencadena una aserción (en las compilaciones de depuración).</span><span class="sxs-lookup"><span data-stu-id="5a06e-108">If the value is **FALSE**, calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method causes an assertion to fire (in debug builds).</span></span>

## <a name="syntax"></a><span data-ttu-id="5a06e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a06e-109">Syntax</span></span>


```C++
BOOL m_fEnableReleaseCallback;
```



## <a name="requirements"></a><span data-ttu-id="5a06e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a06e-110">Requirements</span></span>



| <span data-ttu-id="5a06e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a06e-111">Requirement</span></span> | <span data-ttu-id="5a06e-112">Value</span><span class="sxs-lookup"><span data-stu-id="5a06e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a06e-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a06e-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5a06e-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a06e-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a06e-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a06e-115">Library</span></span><br/> | <dl> <span data-ttu-id="5a06e-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5a06e-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a06e-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a06e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a06e-118">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="5a06e-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




