---
description: Marca que indica si los requisitos de búfer han cambiado.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Miembro CBaseAllocator:: m_bChanged (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671449"
---
# <a name="cbaseallocatorm_bchanged-member"></a><span data-ttu-id="ab1d9-103">Miembro bChanged CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="ab1d9-103">CBaseAllocator::m\_bChanged member</span></span>

<span data-ttu-id="ab1d9-104">Marca que indica si los requisitos de búfer han cambiado.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-104">Flag indicating whether the buffer requirements have changed.</span></span> <span data-ttu-id="ab1d9-105">El método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) establece el valor en **true**.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-105">The [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method sets the value to **TRUE**.</span></span> <span data-ttu-id="ab1d9-106">En una clase derivada, el método virtual puro [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) debe volver a establecer el valor en **false**.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-106">In a derived class, the pure virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) should set the value back to **FALSE**.</span></span> <span data-ttu-id="ab1d9-107">Una vez que se han asignado los búferes, no es necesario volver a asignarlos, mientras que *m \_ BChanged* es **false**.</span><span class="sxs-lookup"><span data-stu-id="ab1d9-107">Once buffers have been allocated, there is no need to re-allocate them while *m\_bChanged* is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1d9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab1d9-108">Syntax</span></span>


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a><span data-ttu-id="ab1d9-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab1d9-109">Requirements</span></span>



| <span data-ttu-id="ab1d9-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab1d9-110">Requirement</span></span> | <span data-ttu-id="ab1d9-111">Value</span><span class="sxs-lookup"><span data-stu-id="ab1d9-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1d9-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab1d9-112">Header</span></span><br/>  | <dl> <span data-ttu-id="ab1d9-113"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab1d9-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab1d9-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab1d9-114">Library</span></span><br/> | <dl> <span data-ttu-id="ab1d9-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab1d9-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab1d9-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab1d9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1d9-117">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="ab1d9-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




