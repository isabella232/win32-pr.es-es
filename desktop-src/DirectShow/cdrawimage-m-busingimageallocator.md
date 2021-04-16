---
description: La \_ variable miembro m bUsingImageAllocator indica si el asignador de la conexión de PIN es un objeto CImageAllocator. Si el valor es TRUE, el asignador es un objeto CImageAllocator (o se deriva de esa clase).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Miembro CDrawImage:: m_bUsingImageAllocator (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e08d1e8217f42c6855759cefeef40e56949156fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671316"
---
# <a name="cdrawimagem_busingimageallocator-member"></a><span data-ttu-id="30b9c-104">Miembro bUsingImageAllocator CDrawImage:: m \_</span><span class="sxs-lookup"><span data-stu-id="30b9c-104">CDrawImage::m\_bUsingImageAllocator member</span></span>

<span data-ttu-id="30b9c-105">La `m_bUsingImageAllocator` variable miembro indica si el asignador de la conexión de PIN es un objeto **CImageAllocator** .</span><span class="sxs-lookup"><span data-stu-id="30b9c-105">The `m_bUsingImageAllocator` member variable indicates whether the allocator for the pin connection is a **CImageAllocator** object.</span></span> <span data-ttu-id="30b9c-106">Si el valor es **true**, el asignador es un objeto **CImageAllocator** (o se deriva de esa clase).</span><span class="sxs-lookup"><span data-stu-id="30b9c-106">If the value is **TRUE**, the allocator is a **CImageAllocator** object (or is derived from that class).</span></span>

## <a name="syntax"></a><span data-ttu-id="30b9c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30b9c-107">Syntax</span></span>


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a><span data-ttu-id="30b9c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30b9c-108">Remarks</span></span>

<span data-ttu-id="30b9c-109">Cuando el valor es **true**, el objeto **CDrawImage** puede usar las funciones **bitblt** y **StretchBlt** de GDI para representar la imagen, en lugar de las funciones **SetDIBitsToDevice** y **StretchDIBits** más lentas.</span><span class="sxs-lookup"><span data-stu-id="30b9c-109">When the value is **TRUE**, the **CDrawImage** object can use the GDI **BitBlt** and **StretchBlt** functions to render the image, rather than the slower **SetDIBitsToDevice** and **StretchDIBits** functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b9c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b9c-110">Requirements</span></span>



| <span data-ttu-id="30b9c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="30b9c-111">Requirement</span></span> | <span data-ttu-id="30b9c-112">Value</span><span class="sxs-lookup"><span data-stu-id="30b9c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b9c-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30b9c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="30b9c-114"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30b9c-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30b9c-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30b9c-115">Library</span></span><br/> | <dl> <span data-ttu-id="30b9c-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="30b9c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b9c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="30b9c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b9c-118">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="30b9c-118">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="30b9c-119">**CDrawImage::NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="30b9c-119">**CDrawImage::NotifyAllocator**</span></span>](cdrawimage-notifyallocator.md)
</dt> <dt>

[<span data-ttu-id="30b9c-120">**CDrawImage::UsingImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="30b9c-120">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




