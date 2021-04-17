---
description: Implementa un asignador que admite la interfaz IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Clase CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670992"
---
# <a name="cmemallocator-class"></a><span data-ttu-id="93be9-103">Clase CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="93be9-103">CMemAllocator class</span></span>

![jerarquía de clases cmemallocator](images/filter10.png)

<span data-ttu-id="93be9-105">Implementa un asignador que admite la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="93be9-105">Implements an allocator that supports the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="93be9-106">Esta clase se deriva de [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="93be9-106">This class derives from [**CBaseAllocator**](cbaseallocator.md).</span></span> <span data-ttu-id="93be9-107">Para obtener más información acerca de los asignadores, consulte la documentación de [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="93be9-107">For more information about allocators, refer to the documentation for [**CBaseAllocator**](cbaseallocator.md).</span></span>



| <span data-ttu-id="93be9-108">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="93be9-108">Protected Member Variables</span></span>                              | <span data-ttu-id="93be9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="93be9-109">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="93be9-110">**m \_ pBuffer**</span><span class="sxs-lookup"><span data-stu-id="93be9-110">**m\_pBuffer**</span></span>](cmemallocator-m-pbuffer.md)           | <span data-ttu-id="93be9-111">Puntero al bloque de memoria que contiene los búferes.</span><span class="sxs-lookup"><span data-stu-id="93be9-111">Pointer to the memory block that contains the buffers.</span></span>                   |
| <span data-ttu-id="93be9-112">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="93be9-112">Protected Methods</span></span>                                       | <span data-ttu-id="93be9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="93be9-113">Description</span></span>                                                              |
| [<span data-ttu-id="93be9-114">**Gratuito**</span><span class="sxs-lookup"><span data-stu-id="93be9-114">**Free**</span></span>](cmemallocator-free.md)                      | <span data-ttu-id="93be9-115">Método placeholder; se llama durante una operación de desconfirmación.</span><span class="sxs-lookup"><span data-stu-id="93be9-115">Placeholder method; called during a decommit operation.</span></span>                  |
| [<span data-ttu-id="93be9-116">**ReallyFree**</span><span class="sxs-lookup"><span data-stu-id="93be9-116">**ReallyFree**</span></span>](cmemallocator-reallyfree.md)          | <span data-ttu-id="93be9-117">Libera la memoria de los búferes.</span><span class="sxs-lookup"><span data-stu-id="93be9-117">Releases the memory for the buffers.</span></span>                                     |
| [<span data-ttu-id="93be9-118">**Alloc**</span><span class="sxs-lookup"><span data-stu-id="93be9-118">**Alloc**</span></span>](cmemallocator-alloc.md)                    | <span data-ttu-id="93be9-119">Asigna memoria a los búferes.</span><span class="sxs-lookup"><span data-stu-id="93be9-119">Allocates memory for the buffers.</span></span>                                        |
| <span data-ttu-id="93be9-120">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="93be9-120">Public Methods</span></span>                                          | <span data-ttu-id="93be9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="93be9-121">Description</span></span>                                                              |
| [<span data-ttu-id="93be9-122">**CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="93be9-122">**CMemAllocator**</span></span>](cmemallocator-cmemallocator.md)    | <span data-ttu-id="93be9-123">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="93be9-123">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="93be9-124">**~ CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="93be9-124">**~ CMemAllocator**</span></span>](cmemallocator--cmemallocator.md) | <span data-ttu-id="93be9-125">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="93be9-125">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="93be9-126">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="93be9-126">**CreateInstance**</span></span>](cmemallocator-createinstance.md)  | <span data-ttu-id="93be9-127">Crea una nueva instancia de la clase **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="93be9-127">Creates a new instance of the **CMemAllocator** class.</span></span>                   |
| <span data-ttu-id="93be9-128">Métodos IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="93be9-128">IMemAllocator Methods</span></span>                                   | <span data-ttu-id="93be9-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="93be9-129">Description</span></span>                                                              |
| [<span data-ttu-id="93be9-130">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="93be9-130">**SetProperties**</span></span>](cmemallocator-setproperties.md)    | <span data-ttu-id="93be9-131">Especifica el número de búferes que se van a asignar y el tamaño de cada búfer.</span><span class="sxs-lookup"><span data-stu-id="93be9-131">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="93be9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93be9-132">Requirements</span></span>



| <span data-ttu-id="93be9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="93be9-133">Requirement</span></span> | <span data-ttu-id="93be9-134">Value</span><span class="sxs-lookup"><span data-stu-id="93be9-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93be9-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93be9-135">Header</span></span><br/>  | <dl> <span data-ttu-id="93be9-136"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93be9-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="93be9-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93be9-137">Library</span></span><br/> | <dl> <span data-ttu-id="93be9-138"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="93be9-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93be9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="93be9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93be9-140">Proporcionar un asignador personalizado</span><span class="sxs-lookup"><span data-stu-id="93be9-140">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
</dt> </dl>

 

 




