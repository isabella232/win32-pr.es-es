---
description: El método Alloc asigna memoria a los búferes.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Método CMemAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670758"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="9c8cf-103">CMemAllocator. Alloc (método)</span><span class="sxs-lookup"><span data-stu-id="9c8cf-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="9c8cf-104">El `Alloc` método asigna memoria a los búferes.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c8cf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c8cf-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="9c8cf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c8cf-106">Parameters</span></span>

<span data-ttu-id="9c8cf-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9c8cf-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c8cf-108">Return value</span></span>

<span data-ttu-id="9c8cf-109">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9c8cf-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9c8cf-110">Return code</span></span>                                                                                       | <span data-ttu-id="9c8cf-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c8cf-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9c8cf-112"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cf-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="9c8cf-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="9c8cf-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cf-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="9c8cf-115">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="9c8cf-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cf-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="9c8cf-117">No se establecieron los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9c8cf-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c8cf-118">Remarks</span></span>

<span data-ttu-id="9c8cf-119">El método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="9c8cf-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="9c8cf-120">Asigna un bloque de memoria contiguo suficiente para los requisitos de búfer proporcionados en el método [**CMemAllocator:: SetProperties**](cmemallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="9c8cf-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c8cf-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c8cf-121">Requirements</span></span>



| <span data-ttu-id="9c8cf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c8cf-122">Requirement</span></span> | <span data-ttu-id="9c8cf-123">Value</span><span class="sxs-lookup"><span data-stu-id="9c8cf-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c8cf-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c8cf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9c8cf-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cf-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9c8cf-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c8cf-126">Library</span></span><br/> | <dl> <span data-ttu-id="9c8cf-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9c8cf-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c8cf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c8cf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c8cf-129">**Clase CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="9c8cf-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




