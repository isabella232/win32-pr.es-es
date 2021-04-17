---
description: La clase CTransInPlaceInputPin implementa un PIN de entrada usado por la clase CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Clase CTransInPlaceInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679250"
---
# <a name="ctransinplaceinputpin-class"></a><span data-ttu-id="e697d-103">Clase CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="e697d-103">CTransInPlaceInputPin class</span></span>

![jerarquía de clases ctransinplaceinputpin](images/tsip01.png)

<span data-ttu-id="e697d-105">La `CTransInPlaceInputPin` clase implementa un PIN de entrada usado por la clase [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="e697d-105">The `CTransInPlaceInputPin` class implements an input pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="e697d-106">Normalmente, no es necesario derivar de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e697d-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="e697d-107">Si lo hace, debe invalidar el método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro para crear instancias de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e697d-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="e697d-108">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="e697d-108">Protected Member Variables</span></span>                                                          | <span data-ttu-id="e697d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e697d-109">Description</span></span>                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="e697d-110">**m \_ bReadOnly**</span><span class="sxs-lookup"><span data-stu-id="e697d-110">**m\_bReadOnly**</span></span>](ctransinplaceinputpin-m-breadonly.md)                           | <span data-ttu-id="e697d-111">Marca que especifica si el flujo de entrada es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e697d-111">Flag that specifies whether the input stream is read-only.</span></span> |
| [<span data-ttu-id="e697d-112">**m \_ pTIPFilter**</span><span class="sxs-lookup"><span data-stu-id="e697d-112">**m\_pTIPFilter**</span></span>](ctransinplaceinputpin-m-ptipfilter.md)                         | <span data-ttu-id="e697d-113">Puntero al filtro que creó este pin.</span><span class="sxs-lookup"><span data-stu-id="e697d-113">Pointer to the filter that created this pin.</span></span>               |
| <span data-ttu-id="e697d-114">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="e697d-114">Public Methods</span></span>                                                                      | <span data-ttu-id="e697d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e697d-115">Description</span></span>                                                |
| [<span data-ttu-id="e697d-116">**CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="e697d-116">**CTransInPlaceInputPin**</span></span>](ctransinplaceinputpin-ctransinplaceinputpin.md)        | <span data-ttu-id="e697d-117">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="e697d-117">Constructor method.</span></span>                                        |
| [<span data-ttu-id="e697d-118">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="e697d-118">**CheckMediaType**</span></span>](ctransinplaceinputpin-checkmediatype.md)                      | <span data-ttu-id="e697d-119">Determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="e697d-119">Determines if the pin accepts a specific media type.</span></span>       |
| [<span data-ttu-id="e697d-120">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="e697d-120">**PeekAllocator**</span></span>](ctransinplaceinputpin-peekallocator.md)                        | <span data-ttu-id="e697d-121">Recupera un puntero al asignador del PIN.</span><span class="sxs-lookup"><span data-stu-id="e697d-121">Retrieves a pointer to the pin's allocator.</span></span>                |
| [<span data-ttu-id="e697d-122">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="e697d-122">**ReadOnly**</span></span>](ctransinplaceinputpin-readonly.md)                                  | <span data-ttu-id="e697d-123">Indica si el flujo de entrada es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e697d-123">Indicates whether the input stream is read-only.</span></span>           |
| <span data-ttu-id="e697d-124">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="e697d-124">IPin Methods</span></span>                                                                        | <span data-ttu-id="e697d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e697d-125">Description</span></span>                                                |
| [<span data-ttu-id="e697d-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="e697d-126">**EnumMediaTypes**</span></span>](ctransinplaceinputpin-enummediatypes.md)                      | <span data-ttu-id="e697d-127">Enumera los tipos de medios preferidos del PIN.</span><span class="sxs-lookup"><span data-stu-id="e697d-127">Enumerates the pin's preferred media types.</span></span>                |
| <span data-ttu-id="e697d-128">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="e697d-128">IMemInputPin Methods</span></span>                                                                | <span data-ttu-id="e697d-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e697d-129">Description</span></span>                                                |
| [<span data-ttu-id="e697d-130">**GetAllocator**</span><span class="sxs-lookup"><span data-stu-id="e697d-130">**GetAllocator**</span></span>](ctransinplaceinputpin-getallocator.md)                          | <span data-ttu-id="e697d-131">Recupera el asignador de memoria propuesto por este pin.</span><span class="sxs-lookup"><span data-stu-id="e697d-131">Retrieves the memory allocator proposed by this pin.</span></span>       |
| [<span data-ttu-id="e697d-132">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="e697d-132">**NotifyAllocator**</span></span>](ctransinplaceinputpin-notifyallocator.md)                    | <span data-ttu-id="e697d-133">Especifica un asignador para la conexión.</span><span class="sxs-lookup"><span data-stu-id="e697d-133">Specifies an allocator for the connection.</span></span>                 |
| [<span data-ttu-id="e697d-134">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="e697d-134">**GetAllocatorRequirements**</span></span>](ctransinplaceinputpin--getallocatorrequirements.md) | <span data-ttu-id="e697d-135">Recupera las propiedades de asignador solicitadas por el código PIN.</span><span class="sxs-lookup"><span data-stu-id="e697d-135">Retrieves the allocator properties requested by the pin.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="e697d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e697d-136">Requirements</span></span>



| <span data-ttu-id="e697d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e697d-137">Requirement</span></span> | <span data-ttu-id="e697d-138">Value</span><span class="sxs-lookup"><span data-stu-id="e697d-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e697d-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e697d-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e697d-140"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e697d-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e697d-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e697d-141">Library</span></span><br/> | <dl> <span data-ttu-id="e697d-142"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e697d-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




