---
description: 'Método CBaseAllocator.Alloc: el método Alloc asigna memoria para los búferes.'
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Método CBaseAllocator.Alloc (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096373"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="9456d-103">Método CBaseAllocator.Alloc</span><span class="sxs-lookup"><span data-stu-id="9456d-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="9456d-104">El `Alloc` método asigna memoria para los búferes.</span><span class="sxs-lookup"><span data-stu-id="9456d-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9456d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9456d-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="9456d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9456d-106">Parameters</span></span>

<span data-ttu-id="9456d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9456d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9456d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9456d-108">Return value</span></span>

<span data-ttu-id="9456d-109">Devuelve uno de los siguientes **valores HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9456d-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="9456d-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9456d-110">Return code</span></span>                                                                                       | <span data-ttu-id="9456d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9456d-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="9456d-112"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="9456d-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="9456d-113">Los requisitos de búfer no han cambiado.</span><span class="sxs-lookup"><span data-stu-id="9456d-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="9456d-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9456d-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="9456d-115">Los requisitos del búfer han cambiado.</span><span class="sxs-lookup"><span data-stu-id="9456d-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="9456d-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="9456d-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="9456d-117">No se han establecido los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="9456d-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="9456d-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9456d-118">Remarks</span></span>

<span data-ttu-id="9456d-119">El método [**CBaseAllocator::Commit**](cbaseallocator-commit.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="9456d-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="9456d-120">En la clase base, este método no asigna ninguna memoria.</span><span class="sxs-lookup"><span data-stu-id="9456d-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="9456d-121">Devuelve un error si no se han establecido los requisitos del búfer, S FALSE si los requisitos no han cambiado y S OK si los requisitos \_ \_ han cambiado.</span><span class="sxs-lookup"><span data-stu-id="9456d-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="9456d-122">Una clase derivada debe invalidar este método para realizar la asignación de memoria real.</span><span class="sxs-lookup"><span data-stu-id="9456d-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="9456d-123">Normalmente, la clase derivada realizará los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="9456d-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="9456d-124">Llame a la implementación de la clase base para determinar si la memoria realmente necesita asignarse.</span><span class="sxs-lookup"><span data-stu-id="9456d-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="9456d-125">Asigne memoria.</span><span class="sxs-lookup"><span data-stu-id="9456d-125">Allocate memory.</span></span>
3.  <span data-ttu-id="9456d-126">Cree [**objetos CMediaSample**](cmediasample.md) que contengan fragmentos de memoria del paso 2.</span><span class="sxs-lookup"><span data-stu-id="9456d-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="9456d-127">Agregue cada **objeto CMediaSample** a la lista de ejemplos gratuitos [**(CBaseAllocator::m \_ lFree).**](cbaseallocator-m-lfree.md)</span><span class="sxs-lookup"><span data-stu-id="9456d-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="9456d-128">Para obtener un ejemplo, [**vea CMemAllocator::Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="9456d-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9456d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9456d-129">Requirements</span></span>



| <span data-ttu-id="9456d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9456d-130">Requirement</span></span> | <span data-ttu-id="9456d-131">Value</span><span class="sxs-lookup"><span data-stu-id="9456d-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9456d-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9456d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="9456d-133"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9456d-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9456d-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9456d-134">Library</span></span><br/> | <dl> <span data-ttu-id="9456d-135"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9456d-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9456d-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9456d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9456d-137">**CBaseAllocator (clase)**</span><span class="sxs-lookup"><span data-stu-id="9456d-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




