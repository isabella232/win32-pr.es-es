---
description: 'El método Alloc asigna memoria a los búferes. Este método invalida el método CBaseAllocator:: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Método CImageAllocator. Alloc (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660822"
---
# <a name="cimageallocatoralloc-method"></a><span data-ttu-id="f5f98-104">CImageAllocator. Alloc (método)</span><span class="sxs-lookup"><span data-stu-id="f5f98-104">CImageAllocator.Alloc method</span></span>

<span data-ttu-id="f5f98-105">El `Alloc` método asigna memoria a los búferes.</span><span class="sxs-lookup"><span data-stu-id="f5f98-105">The `Alloc` method allocates memory for the buffers.</span></span> <span data-ttu-id="f5f98-106">Este método invalida el método [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f98-106">This method overrides the [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f98-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5f98-107">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="f5f98-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5f98-108">Parameters</span></span>

<span data-ttu-id="f5f98-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f5f98-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5f98-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5f98-110">Return value</span></span>

<span data-ttu-id="f5f98-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5f98-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f5f98-112">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="f5f98-112">Possible values include the following.</span></span>



| <span data-ttu-id="f5f98-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f5f98-113">Return code</span></span>                                                                                   | <span data-ttu-id="f5f98-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5f98-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="f5f98-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f5f98-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f5f98-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="f5f98-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="f5f98-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f5f98-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f5f98-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="f5f98-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5f98-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5f98-119">Remarks</span></span>

<span data-ttu-id="f5f98-120">El método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) llama a este método cuando el filtro confirma el asignador.</span><span class="sxs-lookup"><span data-stu-id="f5f98-120">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method, when the filter commits the allocator.</span></span>

<span data-ttu-id="f5f98-121">Este método crea una lista de ejemplos de medios, que se implementan como objetos [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f98-121">This method creates a list of media samples, which are implemented as [**CImageSample**](cimagesample.md) objects.</span></span> <span data-ttu-id="f5f98-122">Cada ejemplo contiene un mapa de bits independiente del dispositivo GDI mediante la función **CreateDIBSection** de GDI.</span><span class="sxs-lookup"><span data-stu-id="f5f98-122">Each sample contains a GDI device-independent bitmap, using the GDI **CreateDIBSection** function.</span></span>

<span data-ttu-id="f5f98-123">Internamente, este método llama a [**CImageAllocator:: CreateDIB**](cimageallocator-createdib.md) para crear cada DIB y [**CImageAllocator:: CreateImageSample**](cimageallocator-createimagesample.md) para crear cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f5f98-123">Internally this method calls [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) to create each DIB, and [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) to create each sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f98-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5f98-124">Requirements</span></span>



| <span data-ttu-id="f5f98-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f98-125">Requirement</span></span> | <span data-ttu-id="f5f98-126">Value</span><span class="sxs-lookup"><span data-stu-id="f5f98-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f98-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5f98-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f5f98-128"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5f98-128"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5f98-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5f98-129">Library</span></span><br/> | <dl> <span data-ttu-id="f5f98-130"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f5f98-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5f98-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5f98-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f98-132">**Clase CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="f5f98-132">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




