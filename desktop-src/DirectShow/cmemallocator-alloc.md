---
description: 'Método CMemAllocator.Alloc: el método Alloc asigna memoria para los búferes.'
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Método CMemAllocator.Alloc (Amfilter.h)
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
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099043"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="e8084-103">Método CMemAllocator.Alloc</span><span class="sxs-lookup"><span data-stu-id="e8084-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="e8084-104">El `Alloc` método asigna memoria para los búferes.</span><span class="sxs-lookup"><span data-stu-id="e8084-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8084-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8084-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="e8084-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8084-106">Parameters</span></span>

<span data-ttu-id="e8084-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e8084-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8084-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8084-108">Return value</span></span>

<span data-ttu-id="e8084-109">Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8084-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e8084-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e8084-110">Return code</span></span>                                                                                       | <span data-ttu-id="e8084-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8084-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e8084-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8084-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="e8084-113">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e8084-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="e8084-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e8084-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="e8084-115">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="e8084-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="e8084-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="e8084-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="e8084-117">No se han establecido los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="e8084-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8084-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e8084-118">Remarks</span></span>

<span data-ttu-id="e8084-119">El método [**CBaseAllocator::Commit**](cbaseallocator-commit.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="e8084-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="e8084-120">Asigna un bloque contiguo de memoria suficiente para los requisitos de búfer especificados en el [**método CMemAllocator::SetProperties.**](cmemallocator-setproperties.md)</span><span class="sxs-lookup"><span data-stu-id="e8084-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8084-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8084-121">Requirements</span></span>



| <span data-ttu-id="e8084-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8084-122">Requirement</span></span> | <span data-ttu-id="e8084-123">Value</span><span class="sxs-lookup"><span data-stu-id="e8084-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8084-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8084-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e8084-125"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8084-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8084-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8084-126">Library</span></span><br/> | <dl> <span data-ttu-id="e8084-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e8084-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8084-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8084-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8084-129">**CMemAllocator (clase)**</span><span class="sxs-lookup"><span data-stu-id="e8084-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




