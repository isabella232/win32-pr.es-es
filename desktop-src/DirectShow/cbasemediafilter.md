---
description: La clase CBaseMediaFilter implementa la interfaz IMediaFilter.
ms.assetid: 45c8973b-d0b3-4aeb-96e7-be47f8d7f4a7
title: Clase CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e594fd941fffecc836af26bd3d70cced82ddcaa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670669"
---
# <a name="cbasemediafilter-class"></a><span data-ttu-id="4d6f4-103">Clase CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="4d6f4-103">CBaseMediaFilter class</span></span>

![cbasemediafilter](images/filter05.png)

<span data-ttu-id="4d6f4-105">La `CBaseMediaFilter` clase implementa la interfaz [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) .</span><span class="sxs-lookup"><span data-stu-id="4d6f4-105">The `CBaseMediaFilter` class implements the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface.</span></span> <span data-ttu-id="4d6f4-106">Use esta clase para distribuidores de complementos u otros objetos que necesiten admitir **IMediaFilter** sin admitir la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="4d6f4-106">Use this class for plug-in distributors or other objects that need to support **IMediaFilter** without supporting the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="4d6f4-107">No utilice esta clase para los filtros.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-107">Do not use this class for filters.</span></span> <span data-ttu-id="4d6f4-108">En su lugar, use la clase [**CBaseFilter**](cbasefilter.md) o una clase base derivada de **CBaseFilter**.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-108">Instead, use the [**CBaseFilter**](cbasefilter.md) class, or a base class derived from **CBaseFilter**.</span></span>



| <span data-ttu-id="4d6f4-109">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="4d6f4-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="4d6f4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d6f4-110">Description</span></span>                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="4d6f4-111">**\_Estado m**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-111">**m\_State**</span></span>](cbasemediafilter-m-state.md)                     | <span data-ttu-id="4d6f4-112">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-112">Current state of the object.</span></span>                                 |
| [<span data-ttu-id="4d6f4-113">**m \_ pClock**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-113">**m\_pClock**</span></span>](cbasemediafilter-m-pclock.md)                   | <span data-ttu-id="4d6f4-114">Puntero al reloj de referencia del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-114">Pointer to the object's reference clock.</span></span>                     |
| [<span data-ttu-id="4d6f4-115">**m \_ tStart**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-115">**m\_tStart**</span></span>](cbasemediafilter-m-tstart.md)                   | <span data-ttu-id="4d6f4-116">Tiempo de referencia que corresponde al tiempo de secuencia 0.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-116">Reference time that corresponds to stream time 0.</span></span>            |
| [<span data-ttu-id="4d6f4-117">**CLSID de m \_**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-117">**m\_clsid**</span></span>](cbasemediafilter-m-clsid.md)                     | <span data-ttu-id="4d6f4-118">Identificador de clase (CLSID) del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-118">Class identifier (CLSID) of the object.</span></span>                      |
| [<span data-ttu-id="4d6f4-119">**m \_ Plock**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-119">**m\_pLock**</span></span>](cbasemediafilter-m-plock.md)                     | <span data-ttu-id="4d6f4-120">Puntero a una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-120">Pointer to a critical section.</span></span>                               |
| <span data-ttu-id="4d6f4-121">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="4d6f4-121">Public Methods</span></span>                                                   | <span data-ttu-id="4d6f4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d6f4-122">Description</span></span>                                                  |
| [<span data-ttu-id="4d6f4-123">**CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-123">**CBaseMediaFilter**</span></span>](cbasemediafilter-cbasemediafilter.md)    | <span data-ttu-id="4d6f4-124">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-124">Constructor method.</span></span>                                          |
| [<span data-ttu-id="4d6f4-125">**~ CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-125">**~ CBaseMediaFilter**</span></span>](cbasemediafilter--cbasemediafilter.md) | <span data-ttu-id="4d6f4-126">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-126">Destructor method.</span></span> <span data-ttu-id="4d6f4-127">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-127">Virtual.</span></span>                                  |
| [<span data-ttu-id="4d6f4-128">**StreamTime**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-128">**StreamTime**</span></span>](cbasemediafilter-streamtime.md)                | <span data-ttu-id="4d6f4-129">Recupera la hora de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-129">Retrieves the current stream time.</span></span> <span data-ttu-id="4d6f4-130">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-130">Virtual.</span></span>                  |
| [<span data-ttu-id="4d6f4-131">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-131">**IsActive**</span></span>](cbasemediafilter-isactive.md)                    | <span data-ttu-id="4d6f4-132">Determina si el objeto está activo (en ejecución o en pausa).</span><span class="sxs-lookup"><span data-stu-id="4d6f4-132">Determines whether the object is active (running or paused).</span></span> |
| <span data-ttu-id="4d6f4-133">Métodos IPersist</span><span class="sxs-lookup"><span data-stu-id="4d6f4-133">IPersist Methods</span></span>                                                 | <span data-ttu-id="4d6f4-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d6f4-134">Description</span></span>                                                  |
| [<span data-ttu-id="4d6f4-135">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-135">**GetClassID**</span></span>](cbasemediafilter-getclassid.md)                | <span data-ttu-id="4d6f4-136">Recupera el identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-136">Retrieves the class identifier.</span></span>                              |
| <span data-ttu-id="4d6f4-137">Métodos IMediaFilter</span><span class="sxs-lookup"><span data-stu-id="4d6f4-137">IMediaFilter Methods</span></span>                                             | <span data-ttu-id="4d6f4-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d6f4-138">Description</span></span>                                                  |
| [<span data-ttu-id="4d6f4-139">**GetState**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-139">**GetState**</span></span>](cbasemediafilter-getstate.md)                    | <span data-ttu-id="4d6f4-140">Recupera el estado del objeto (en ejecución, detenido o en pausa).</span><span class="sxs-lookup"><span data-stu-id="4d6f4-140">Retrieves the object's state (running, stopped, or paused).</span></span>  |
| [<span data-ttu-id="4d6f4-141">**SetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-141">**SetSyncSource**</span></span>](cbasemediafilter-setsyncsource.md)          | <span data-ttu-id="4d6f4-142">Establece un reloj de referencia para el objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-142">Sets a reference clock for the object.</span></span>                       |
| [<span data-ttu-id="4d6f4-143">**GetSyncSource**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-143">**GetSyncSource**</span></span>](cbasemediafilter-getsyncsource.md)          | <span data-ttu-id="4d6f4-144">Recupera el reloj de referencia que usa el objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-144">Retrieves the reference clock that the object is using.</span></span>      |
| [<span data-ttu-id="4d6f4-145">**Stop**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-145">**Stop**</span></span>](cbasemediafilter-stop.md)                            | <span data-ttu-id="4d6f4-146">Detiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-146">Stops the object.</span></span>                                            |
| [<span data-ttu-id="4d6f4-147">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-147">**Pause**</span></span>](cbasemediafilter-pause.md)                          | <span data-ttu-id="4d6f4-148">Pausa el objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-148">Pauses the object.</span></span>                                           |
| [<span data-ttu-id="4d6f4-149">**Ejecutar**</span><span class="sxs-lookup"><span data-stu-id="4d6f4-149">**Run**</span></span>](cbasemediafilter-run.md)                              | <span data-ttu-id="4d6f4-150">Ejecuta el objeto.</span><span class="sxs-lookup"><span data-stu-id="4d6f4-150">Runs the object.</span></span>                                             |



 

## <a name="requirements"></a><span data-ttu-id="4d6f4-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d6f4-151">Requirements</span></span>



| <span data-ttu-id="4d6f4-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d6f4-152">Requirement</span></span> | <span data-ttu-id="4d6f4-153">Value</span><span class="sxs-lookup"><span data-stu-id="4d6f4-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d6f4-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d6f4-154">Header</span></span><br/>  | <dl> <span data-ttu-id="4d6f4-155"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d6f4-155"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4d6f4-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d6f4-156">Library</span></span><br/> | <dl> <span data-ttu-id="4d6f4-157"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4d6f4-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




