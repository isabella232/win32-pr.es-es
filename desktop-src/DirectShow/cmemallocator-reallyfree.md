---
description: El método ReallyFree libera la memoria de los búferes.
ms.assetid: c5c5d09f-b4f2-4a06-9309-3b2a8b8f8f1f
title: Método CMemAllocator. ReallyFree (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.ReallyFree
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 187807658c8e15ddf530ca6687d860fe826f4208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680354"
---
# <a name="cmemallocatorreallyfree-method"></a><span data-ttu-id="97b53-103">CMemAllocator. ReallyFree, método</span><span class="sxs-lookup"><span data-stu-id="97b53-103">CMemAllocator.ReallyFree method</span></span>

<span data-ttu-id="97b53-104">El `ReallyFree` método libera la memoria de los búferes.</span><span class="sxs-lookup"><span data-stu-id="97b53-104">The `ReallyFree` method releases the memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="97b53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97b53-105">Syntax</span></span>


```C++
void ReallyFree();
```



## <a name="parameters"></a><span data-ttu-id="97b53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97b53-106">Parameters</span></span>

<span data-ttu-id="97b53-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="97b53-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97b53-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97b53-108">Return value</span></span>

<span data-ttu-id="97b53-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="97b53-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="97b53-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97b53-110">Remarks</span></span>

<span data-ttu-id="97b53-111">La clase [**CMemAllocator**](cmemallocator.md) contiene memoria hasta que se elimina el objeto.</span><span class="sxs-lookup"><span data-stu-id="97b53-111">The [**CMemAllocator**](cmemallocator.md) class holds memory until the object is deleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="97b53-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97b53-112">Requirements</span></span>



| <span data-ttu-id="97b53-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="97b53-113">Requirement</span></span> | <span data-ttu-id="97b53-114">Value</span><span class="sxs-lookup"><span data-stu-id="97b53-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97b53-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97b53-115">Header</span></span><br/>  | <dl> <span data-ttu-id="97b53-116"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97b53-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="97b53-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97b53-117">Library</span></span><br/> | <dl> <span data-ttu-id="97b53-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="97b53-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b53-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="97b53-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b53-120">**Clase CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="97b53-120">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




