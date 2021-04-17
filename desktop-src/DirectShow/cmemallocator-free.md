---
description: Se llama al método Free durante una operación de desconfirmación.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Método CMemAllocator. Free (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681152"
---
# <a name="cmemallocatorfree-method"></a><span data-ttu-id="fe750-103">Método CMemAllocator. Free</span><span class="sxs-lookup"><span data-stu-id="fe750-103">CMemAllocator.Free method</span></span>

<span data-ttu-id="fe750-104">`Free`Se llama al método durante una operación de desconfirmación.</span><span class="sxs-lookup"><span data-stu-id="fe750-104">The `Free` method is called during a decommit operation.</span></span> <span data-ttu-id="fe750-105">Este método implementa el método [**CBaseAllocator:: Free**](cbaseallocator-free.md) virtual puro, pero no hace nada.</span><span class="sxs-lookup"><span data-stu-id="fe750-105">This method implements the pure virtual [**CBaseAllocator::Free**](cbaseallocator-free.md) method, but does nothing.</span></span> <span data-ttu-id="fe750-106">La memoria del búfer no se libera realmente hasta que se destruye el objeto **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="fe750-106">The buffer memory is not actually released until the **CMemAllocator** object is destroyed.</span></span> <span data-ttu-id="fe750-107">El método de destructor llama a [**CMemAllocator:: ReallyFree**](cmemallocator-reallyfree.md) para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="fe750-107">The destructor method calls [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) to release the memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe750-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe750-108">Syntax</span></span>


```C++
void Free();
```



## <a name="parameters"></a><span data-ttu-id="fe750-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe750-109">Parameters</span></span>

<span data-ttu-id="fe750-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fe750-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe750-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe750-111">Return value</span></span>

<span data-ttu-id="fe750-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fe750-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe750-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe750-113">Requirements</span></span>



| <span data-ttu-id="fe750-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe750-114">Requirement</span></span> | <span data-ttu-id="fe750-115">Value</span><span class="sxs-lookup"><span data-stu-id="fe750-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe750-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe750-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fe750-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe750-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fe750-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe750-118">Library</span></span><br/> | <dl> <span data-ttu-id="fe750-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fe750-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe750-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe750-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe750-121">**Clase CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="fe750-121">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




