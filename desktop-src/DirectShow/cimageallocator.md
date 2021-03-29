---
description: La clase CImageAllocator implementa un asignador que administra mapas de bits independientes del dispositivo GDI (DIB). Esta clase se deriva de la clase CBaseAllocator. Crea ejemplos de medios que se implementan mediante la clase CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Clase CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679087"
---
# <a name="cimageallocator-class"></a><span data-ttu-id="5e307-105">Clase CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="5e307-105">CImageAllocator class</span></span>

![jerarquía de clases cimageallocator](images/wutil04.png)

<span data-ttu-id="5e307-107">La `CImageAllocator` clase implementa un asignador que administra los mapas de bits independientes del dispositivo GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="5e307-107">The `CImageAllocator` class implements an allocator that manages GDI device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="5e307-108">Esta clase se deriva de la clase [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="5e307-108">This class derives from the [**CBaseAllocator**](cbaseallocator.md) class.</span></span> <span data-ttu-id="5e307-109">Crea ejemplos de medios que se implementan mediante la clase [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="5e307-109">It creates media samples that are implemented using the [**CImageSample**](cimagesample.md) class.</span></span>

<span data-ttu-id="5e307-110">Dos clavijas conectadas comparten un asignador, pero siempre pertenece a uno de los filtros de la conexión.</span><span class="sxs-lookup"><span data-stu-id="5e307-110">An allocator is shared by two connected pins, but is always owned by one of the filters in the connection.</span></span> <span data-ttu-id="5e307-111">Un filtro que utiliza `CImageAllocator` debe realizar un seguimiento de si el asignador se proporcionó por sí solo o por el otro filtro.</span><span class="sxs-lookup"><span data-stu-id="5e307-111">A filter that uses `CImageAllocator` must keep track of whether the allocator was provided by itself or by the other filter.</span></span> <span data-ttu-id="5e307-112">Si el asignador se proporcionó por sí solo, el filtro propietario puede basarse en el hecho de que todos los ejemplos de medios del asignador son objetos **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="5e307-112">If the allocator was provided by itself, the owning filter can rely on the fact that all media samples from the allocator are **CImageSample** objects.</span></span> <span data-ttu-id="5e307-113">Por tanto, puede usar el objeto **CImageSample** para obtener información sobre el DIB, que se almacena en una estructura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="5e307-113">It can therefore use the **CImageSample** object to obtain information about the DIB, which is stored in a [**DIBDATA**](dibdata.md) structure.</span></span>

<span data-ttu-id="5e307-114">El filtro propietario debe llamar a **NotifyMediaType** cada vez que cambie el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="5e307-114">The owning filter should call **NotifyMediaType** whenever the media type changes.</span></span>



| <span data-ttu-id="5e307-115">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="5e307-115">Protected Member Variables</span></span>                                     | <span data-ttu-id="5e307-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e307-116">Description</span></span>                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="5e307-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="5e307-117">**m\_pFilter**</span></span>](cimageallocator-m-pfilter.md)                | <span data-ttu-id="5e307-118">Puntero al filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="5e307-118">Pointer to the owning filter.</span></span>                                            |
| [<span data-ttu-id="5e307-119">**m \_ pMediaType**</span><span class="sxs-lookup"><span data-stu-id="5e307-119">**m\_pMediaType**</span></span>](cimageallocator-m-pmediatype.md)          | <span data-ttu-id="5e307-120">Puntero al tipo de medio actual.</span><span class="sxs-lookup"><span data-stu-id="5e307-120">Pointer to the current media type.</span></span>                                       |
| <span data-ttu-id="5e307-121">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="5e307-121">Protected Methods</span></span>                                              | <span data-ttu-id="5e307-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e307-122">Description</span></span>                                                              |
| [<span data-ttu-id="5e307-123">**Alloc**</span><span class="sxs-lookup"><span data-stu-id="5e307-123">**Alloc**</span></span>](cimageallocator-alloc.md)                         | <span data-ttu-id="5e307-124">Asigna memoria a los búferes.</span><span class="sxs-lookup"><span data-stu-id="5e307-124">Allocates memory for the buffers.</span></span>                                        |
| [<span data-ttu-id="5e307-125">**CheckSizes**</span><span class="sxs-lookup"><span data-stu-id="5e307-125">**CheckSizes**</span></span>](cimageallocator-checksizes.md)               | <span data-ttu-id="5e307-126">Comprueba las propiedades del asignador con el tipo de medio actual.</span><span class="sxs-lookup"><span data-stu-id="5e307-126">Checks allocator properties against the current media type.</span></span>              |
| [<span data-ttu-id="5e307-127">**CreateDIB**</span><span class="sxs-lookup"><span data-stu-id="5e307-127">**CreateDIB**</span></span>](cimageallocator-createdib.md)                 | <span data-ttu-id="5e307-128">Crea un DIB.</span><span class="sxs-lookup"><span data-stu-id="5e307-128">Creates a DIB.</span></span>                                                           |
| [<span data-ttu-id="5e307-129">**CreateImageSample**</span><span class="sxs-lookup"><span data-stu-id="5e307-129">**CreateImageSample**</span></span>](cimageallocator-createimagesample.md) | <span data-ttu-id="5e307-130">Crea un ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="5e307-130">Creates a media sample.</span></span> <span data-ttu-id="5e307-131">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="5e307-131">Virtual.</span></span>                                         |
| [<span data-ttu-id="5e307-132">**Gratuito**</span><span class="sxs-lookup"><span data-stu-id="5e307-132">**Free**</span></span>](cimageallocator-free.md)                           | <span data-ttu-id="5e307-133">Libera toda la memoria del búfer.</span><span class="sxs-lookup"><span data-stu-id="5e307-133">Releases all of the buffer memory.</span></span>                                       |
| <span data-ttu-id="5e307-134">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="5e307-134">Public Methods</span></span>                                                 | <span data-ttu-id="5e307-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e307-135">Description</span></span>                                                              |
| [<span data-ttu-id="5e307-136">**CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="5e307-136">**CImageAllocator**</span></span>](cimageallocator-cimageallocator.md)     | <span data-ttu-id="5e307-137">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="5e307-137">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="5e307-138">**NotifyMediaType**</span><span class="sxs-lookup"><span data-stu-id="5e307-138">**NotifyMediaType**</span></span>](cimageallocator-notifymediatype.md)     | <span data-ttu-id="5e307-139">Informa al objeto del tipo de medio actual.</span><span class="sxs-lookup"><span data-stu-id="5e307-139">Informs the object of the current media type.</span></span>                            |
| <span data-ttu-id="5e307-140">Métodos IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="5e307-140">IMemAllocator Methods</span></span>                                          | <span data-ttu-id="5e307-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e307-141">Description</span></span>                                                              |
| [<span data-ttu-id="5e307-142">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="5e307-142">**SetProperties**</span></span>](cimageallocator-setproperties.md)         | <span data-ttu-id="5e307-143">Especifica el número de búferes que se van a asignar y el tamaño de cada búfer.</span><span class="sxs-lookup"><span data-stu-id="5e307-143">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5e307-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e307-144">Requirements</span></span>



| <span data-ttu-id="5e307-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e307-145">Requirement</span></span> | <span data-ttu-id="5e307-146">Value</span><span class="sxs-lookup"><span data-stu-id="5e307-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e307-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e307-147">Header</span></span><br/>  | <dl> <span data-ttu-id="5e307-148"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e307-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5e307-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e307-149">Library</span></span><br/> | <dl> <span data-ttu-id="5e307-150"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5e307-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e307-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e307-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e307-152">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="5e307-152">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




